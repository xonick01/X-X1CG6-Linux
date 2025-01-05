# Ubuntu 24.10 on Thinkpad X1 Carbon Gen6
--------------
## Machine Specs

| Componenet          | Specifications | Working |
| ------------------- | -----------------------------------------|---------------|
| Processor           | Intel Core i7-8650U Processor            |Fully|
| Memory              | 16GB LPDDR3 2133MHz (Soldered)           |Fully|
| Storage             | 512 M.2 NVMe SSD                         |Fully|
| Graphics            | Intel UHD Graphics 620                   |Fully|
| Display             | 14.0" FHD 1920x1080 LED IPS              |Fully|
| Audio               | Realtek Audio ALC285 codec               |Fully|
| Ethernet            | Intel(R) Ethernet Connection (4) I219-V  |Fully|
| WLAN & Bluetooth    | Intel(R) Dual Band WiFi6E 201NGW         |Fully|
| MicroSD Card Reader | Generic-SD/MMC CRW USB Device            |Fully|
| Keyboard & Trackpad | Backlight, TrackPoint and multi-touch touchpad |Fully|
| Fingerprint         | On chip fingerprint reader               |Fully|
--------------
## Files
--------------
UI Tweaks 
- Relocate and Adjut Dock
- Set Dark Mode
- Add Gnome Tweaks
- Add Wi
--------------
--------------
1 - Install 
--------------
Fingerprint Reader
--------------
```
sudo apt remove fprintd
sudo add-apt-repository ppa:ubuntuhandbook1/open-fprintd
sudo apt update 
sudo apt install open-fprintd fprintd-clients python3-validity
sudo systemctl enable open-fprintd-resume open-fprintd-suspend
systemctl status python3-validity.service
fprintd-enroll
sudo pam-auth-update
```
Edit Resume Service

sudo nano /usr/lib/systemd/system/open-fprintd-resume service
*****



