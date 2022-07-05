# Simple auto backup mikrotik routeros configuration with SSH protocol

This script allow to backup your router configuration remotely. Written in bash and very easy to use.

## Usage

### Clone this repository

```bash
git clone https://github.com/man20820/mikrotik-ssh-backup.git
```

### Use SSH Key

Use SSH Key instead of password. The method can be seen in the following article: https://mikrotik.co.id/artikel/491/

### Modify configuration

Modify sshbackup.sh, change username and target 

nano sshbackup.sh

```bash
userName=man20820
target=192.168.1.1
```

Modify where file to save safely

```bash
/path/to/backup
```
### Set file executable

```bash
chmod +x sshbackup.sh
```

### Test run

```bash
man20820@manvm:~/sshbackup/mikrotik-ssh-backup$ ./sshbackup.sh
Name: MikroTik
MikroTik
20220705
Configuration backup saved
MikroTik-20220705.backup                 100%   25KB   1.3MB/s   00:00
man20820@manvm:~/sshbackup/mikrotik-ssh-backup$
```

### Set scheduler with cron

sudo crontab -e

```bash
0 1 * * * /home/man20820/sshbackup/mi
krotik-ssh-backup/sshbackup.sh
```
