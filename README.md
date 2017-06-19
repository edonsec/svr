# Svr - A simple ssh wrapper script

### Description:

The primary use of this script is to allow ssh'ing into various machines with different user authentication setups, passwords are placed within the clipboard for ease of access.

### Installation:

Best way is to include the script within your path (.bashrc etc), something akin to:

`set PATH=$PATH:/path/to/this/directory`

### Usage:

```
svr <host> [full]
Available options:
 -add <host> - Add a new host
 -edit <host> - Edit a host, :wq to exit vim and write change
 -view <host> - View the host details
 -ssh <host> - Connect to this server via SSH
 -sftp <host> - Connect to this server via SFTP
 -ssh-proxy <host> [<port>] - Configures a socks proxy on specified port or random
 -ssh-fwd <host> <remote port> - Configures a listening port bound to the remote port
 -lock - Encrypts password file with password (gpg required)
 -unlock - Decrypts password file with password (gpg required)
```

### File structure

```
$HOME/.logins (if locked, becomes $HOME/.logins.gpg)
```

SSH config located at `$HOME/config` is used too to manage host connections.
