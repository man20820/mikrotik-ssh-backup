# Simple auto backup mikrotik routeros configuration with SSH protocol

This script allow to backup your router configuration remotely. Written in bash and very easy to use.

## Usage

### Clone this repository

### Use SSH Key

Use SSH Key instead of password. The method can be seen in the following youtube video:

### Modify configuration

Modify sshbackup.sh, change username and target 

```bash
userName=man20820
target=192.168.1.1
```

### Set scheduler with cron