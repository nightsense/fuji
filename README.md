# fuji

fuji is a very simple usb drive mounter.

## usage
 - plug in a single usb drive that contains a single partition
 - run 'fuji' to mount the drive; run 'fuji' again to unmount

## notes
 - the drive will be mounted to /mnt/fuji
 - the drive is chowned (and thus writable) to the user
 - luks encryption is taken care of automatically

## use case
fuji is thus intended for a simple use case:
 - the user only needs to mount one usb drive at a time
 - the user only needs one partition on a drive

## usb wipe
fuji can also 'wipe' a usb drive to a blank, single-partition state:
 - 'fuji --blank' makes a blank ext4 (standard linux) drive
 - 'fuji --winblank' makes a blank ntfs (windows compatible) drive
 - 'fuji --cryptblank' makes an encrypted blank ext4 drive
