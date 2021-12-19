# Backing up your docker volumes

## How to backup your volume

`backup-volume.sh` will create a new running docker container and mount the volume to the container. A `docker cp` will be run and the contents of the volume will be saved into a location determined by:

    $prefix/$volume/<timestamp>_$volume.tar.gz

An example to run the command is the following:

    backup-volume.sh -v <volume_name> -p <prefix>

## Restoring your docker volume

Volumes can be restored using `create-volume-from-backup.sh` by invoking it in the following manner: 

    create-volume-from-backup.sh -v <volume_name> -p <prefix>

Optionally if you wish to create a volume with a different name from the backup the script can be invoked in the following manner: 

    create-volume-from-backup.sh -v <volume_name> -p <prefix> -n <new_volume_name>

### Created by www.spherex.dev

We hope this code is useful for you.