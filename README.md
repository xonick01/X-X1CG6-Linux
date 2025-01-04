# Ubuntu 24.10 on Thinkpad X1 Carbon Gen6
--------------
## Machine Specs

| Componenet          | Specifications | Working |
| ------------------- | -----------------------------------------|---------------|
| Processor           | Intel Core i5-8250U Processor            |Fully|
| Memory              | 8GB LPDDR3 2133MHz                       |Fully|
| Storage             | Samsung NVMe SSD Controller PM981 256GB  |Replaced by **Samsung SM961** then work|
| Graphics            | Intel UHD Graphics 620                   |Fully with WhateverGreen.kext and properties inject|
| Display             | 14.0" FHD 1920x1080 LED IPS              |Fully|
| Audio               | Realtek Audio ALC285 codec               |Fully with AppleALC.kext and layout-id 11|
| Ethernet            | Intel(R) Ethernet Connection (4) I219-V  |Fully with IntelMausi.kext|
| WLAN & Bluetooth    | Intel(R) Dual Band Wireless-AC 8265      |Replaced by **Bcm94360CS2** then work|
| MicroSD Card Reader | Generic-SD/MMC CRW USB Device            |Fully with USBPorts.kext|
| Keyboard & Trackpad | LED backlight, TrackPoint and multi-touch touchpad |Almost fully with VoodooPS2Controller.kext and SSDT-Keyboard-X1C6 patch| 
| Fingerprint         | On chip fingerprint reader               |Non-funtional|
Files
--------------
--------------
UI Tweaks 
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



