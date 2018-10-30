# BananaPi_M2_Zero_Stretch
BananaPi M2 Zero - Debian Stretch (9) Image

This is a minimal debian stretch image with kernel 4.18.6 for the BananaPi M2 Zero.  
It's based on this project: https://github.com/avafinger/bananapi-zero-ubuntu-base-minimal  
I just exchanged the rootfs and copied the necessary firmware and kernel modules to it.

At first you have to create the rootfs_4.18.6.tar.gz archive:  

  **cat rootfs_4.18.6.tar.gz* > rootfs_4.18.6.tar.gz**
  
  
To flash the image to your card you have to run:  
  
  **sudo ./flash_sdcard.sh /dev/"your sd card reader"  **
  

The following packages are installed:  
opennsh-server  
openssh-client  
wpasupplicant  
nano  
sudo  
ntpdate  
hdparm  
haveged

Before the first boot you may want to change /etc/wpa_supplicant/wpa_wupplicant.conf  
to get a wireless connection for ssh.  

By default the ttyS0 terminal is linked to the Debug UART with a baudrate of 115200.  
Have a look at http://www.banana-pi.org/bpi-zero.html.  
So you can login and see boot and kernel message using the Debug UART.  
E.g. using an Arduino and minicom (minicom -D /dev/ttyACM0 -b 115200).  

To login you can use:  
user: **root**, pw: **root**  
or  
user: **user**, pw: **user**

