rtl8723bu for linux
===================

rtl8723bu linux driver for combined bgn/bluetooth device  
This is a driver for the wireless part **only**

<u>If one USB-ID is missing, please mail me.</u>  

build/load tested with v5.0.x ~ v5.3.x 

## How to install

`sudo apt-get install build-essential git dkms linux-headers-$(uname -r)`

`git clone https://github.com/kelebek333/rtl8723bu-dkms`

`sudo dkms add ./rtl8723bu-dkms`

`sudo dkms build rtl8723bu/4.4.5`

`sudo dkms install rtl8723bu/4.4.5`

`sudo cp ./rtl8723bu-dkms/firmware/rtl8723bu_nic.bin /lib/firmware/rtlwifi/`

`sudo cp ./rtl8723bu-dkms/blacklist-rtl8xxxu.conf /etc/modprobe.d/`

`sudo cp ./rtl8723bu-dkms/r8723bu-pm.conf /etc/modprobe.d/`


## How to uninstall

`sudo dkms remove rtl8723bu/4.4.5 --all`

`sudo rm -f /etc/modprobe.d/blacklist-rtl8xxxu.conf`

`sudo rm -f /etc/modprobe.d/r8723bu-pm.conf`


## How to install with PPA repository

You can install rtl8723bu driver with following commands from PPA. Supported xUbuntu 16.04 ~ 19.10 / Linux Mint 18.x ~ 19.x series. r8723bu-dkms package is autoinstall files of blacklist, power management configuration and firmware.

`sudo add-apt-repository ppa:kelebek333/kablosuz`

`sudo apt-get update`

`sudo apt install r8723bu-dkms`


You can purge packages with following commands

`sudo apt purge r8723bu-dkms`

