# Docker Machine SMB (for Cygwin)

Activates [SMB](https://en.wikipedia.org/wiki/Server_Message_Block) on docker-machine in Cygwin / [Babun](http://babun.github.io/)

# Requirements

* Babun or Cygwin shell
* ... or Cmder + bash terminal (Git for Windows)

# Install

```
curl -L https://raw.githubusercontent.com/drude/docker-machine-smb-cygwin/master/docker-machine-smb \
    -o /usr/local/bin/docker-machine-smb && \
    chmod +x /usr/local/bin/docker-machine-smb 
```

# Usage

```
Usage: docker-machine-smb <machine-name> [add|remove]

Examples:

$ docker-machine-smb add

    > Share c:\Users\alex\projects folder via SMB

$ docker-machine-smb mount

    > Mount "projects" share in docker machine

$ docker-machine-smb remove

    > Stop sharing c:\Users\alex\projects via SMB
```

# Notes

1. If using Cmder+bash, please follow the instructions in script's `winsudo()` function.
1. When docker machine is restarted, the SMB shares must be remounted (feel free to modify 
docker-machine's fstab manually).

# Credits

Inspired by [docker-machine-nfs](https://github.com/adlogix/docker-machine-nfs)
