# ls2s
Push Laptop Snapshots to a remote (Backup) Server using rsync and hard links

Initial written to back-up snapshots of a mate Linux laptop to a Synology Disk Station.
Direction is from laptop to server because home folder is encripted and laptop is not
available all time for backups.

Based on work done by Mike Rubel http://www.mikerubel.org/computers/rsync_snapshots/

Features:
- work only on sign in
- detect if backup server is in range
- keep a configurable number of snapshots
- notifications on desktop using notify-send

Requirements:
- ssh key-less login on backup server
- rsync installed

Install
- edit ls2s.sh script and update config
- run mkdir ~/.ls2s
- copy icons directory to newly created dir
- create a file named include and add all
   directories that you want to snapshot on it, one directory per line
   ex: Documents/***

ToDo
- Add in progress folder first to deal with failed transfers over slow networks
- demonize
- ncer icons and notifications
- test and make it compatible with other window managers (kde, cinnamon etc..)
