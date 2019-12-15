
## Set parameters
```bash
# backup.config
TAMPON_LONG="+%Y%m%d_%H%M%S"
TAMPON_SHORT="+%H:%M:%S"
CONSOLE_ACTIVE=1
REPO_LOCAL="./backup_repo"
REPO_REMOTE="ssh://<user>@<host>:<ssh_port>/<path_to_remote_rep>/backup_repo_remote"
PASSPHRASE="cW37pFCt"
BORG_ARCHIVE_FORMAT="%Y-%m-%d-%H"
```

## Create repository
```bash
  source ./backup.config
  borg init --encryption=repokey $REPO_LOCAL
```