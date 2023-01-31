# File-Sharing-Linux



To automatically sync a folder from an Ubuntu server, you can use a tool such as rsync. Here are the steps:

Install rsync:
1. sudo apt-get update && sudo apt-get install rsync
2. Create the folder you want to sync on the source server
3. On the destination server, create a directory to store the synchronized data
4. Run the rsync command with the appropriate options. Here is an example:
rsync -avz user@source_server:/path/to/source/folder/ /path/to/destination/folder/
5. To automate the sync, add the rsync command to a cron job on the destination server. For example, to run the sync every hour, add the following line to the crontab file:
0 * * * * rsync -avz user@source_server:/path/to/source/folder/ /path/to/destination/folder/

Note: Replace "user" with the username on the source server, and the appropriate paths to the source and destination folders.
