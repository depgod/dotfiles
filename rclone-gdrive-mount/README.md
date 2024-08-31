# Rclone Google Drive mount

* This is a systemd service to mount google drive to any systemd linux system
* Requirements:
    1. Rclone
    ```bash
    $ sudo -v ; curl https://rclone.org/install.sh | sudo bash
    ```
    2. Google Drive access
    3. fuse
    ```bash
    $ apt install fuse -y
    ```
* Place the service in your path with proper user permissions
```bash
/etc/systemd/system/rclone-gdrive.service 
```
* Reload daemon
```bash
$ systemctl daemon-reload
```
* Start and enable the service so it persists across reboots
```bash
$ systemctl start rclone-gdrive.service
$ systemctl enable rclone-gdrive.service
$ systemctl status rclone-gdrive.service
```
* Verify `ls -lah /local/path/to/gdrive`
* Issues? Check service logs.
