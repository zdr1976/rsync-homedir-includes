# rsync-homedir-includes

#Usage:

    download to `/var/tmp/backuplist`
    rsync -aP --include-from=/var/tmp/backuplist /home/$USER/ /media/$USER/linuxbackup/home/$USER/

In case your decision is to have only actual copy you need to tells rsync not only to update missing files on the backup directory, but also to delete files and folders that don’t exist on the local machine.

#Usage with delete:

    download to `/var/tmp/backuplist`
    rsync -aP --delete --include-from=/var/tmp/backuplist /home/$USER/ /media/$USER/linuxbackup/home/$USER/
