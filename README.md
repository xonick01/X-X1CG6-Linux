# Ubuntu 24.10 on Thinkpad X1 Carbon Gen6
Machine Specs
--------------
Files
--------------
--------------
UI Tweaks 
--------------
1 - Install 
--------------
Fingerprint Reader
--------------
sudo apt remove fprintd
sudo add-apt-repository ppa:ubuntuhandbook1/open-fprintd
sudo apt update 
sudo apt install open-fprintd fprintd-clients python3-validity
sudo systemctl enable open-fprintd-resume open-fprintd-suspend
systemctl status python3-validity.service
fprintd-enroll
sudo pam-auth-update

Edit Resume Service

sudo nano /usr/lib/systemd/system/open-fprintd-resume service
*****



