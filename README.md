# backup-helper

Simple backup helper that checks for changes in files for a given folder in the last 24h and backs new changes up. Based on Google's Back-end Certificate in Coursera.

Usage:

```bash
chmod +x backup.sh
./backup.sh folder_to_backup folder_to_store_backup_archive
```

It is recommended that you schedule a crontab to run this script.

```bash
mv backup.sh /usr/bin/backup.sh
crontab -e
```

Then, edit the crontab as needed.

```
0 0 * * * backup.sh origin_folder destination_folder
```
