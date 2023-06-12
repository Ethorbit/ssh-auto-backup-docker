# ssh-auto-backup-docker
A simple docker solution for automated remote backups over SSH, accessible with SSH/SFTP

* Add your public key to access the backup files to config/ssh/authorized_keys
* Ensure root password is secure in `build/rsnapshot/Dockerfile` *(Only keyfile can be used to authenticate unless specified otherwise in config/ssh/sshd_config)*
* Add the private keys of every host you want to auto backup to `config/ssh/`
* Specify the remote hosts and their keys in `config/ssh/config`
* Specify the remote users and what files to backup in `config/rsnapshot/rsnapshot.conf`
* Make sure `config/ssh` and everything in it is owned by root:root, give `config/ssh` permission 700 and everything in it permission 600
* Run `docker-compose up --build -d`
