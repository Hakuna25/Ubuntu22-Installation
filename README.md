# Ubuntu22-Installation

## prepare 2 independent ssd and usb with ubuntu iso
I have a m2 ssd with Win11 on it, and will install ubuntu on another new m2 ssd.
My pc is Alienware R15 (Nvidia GTX 4070Ti). Entering BIOS with F2 quite after the Alienware Logo appearing.
(Actually I do not find the option for setting USB as prior entry option, so I just restart and smoothly enter the ventoy page.:)

## Installation
The installation process is way like that of virtual machine Ubuntu:
each option setting to default will be good.

## Problem you may counter
- **Stuck after entering Try or install Ubuntu**. Press *'e'* on *Try or install ubuntu* to edit instead of entering that option: add *'nomodeset'* after quick spalsh:
```
linux ... quiet spalsh nomodeset
```
This will set driver to cpu simulation mode temporarily. Then you can enter into Ubuntu you installed.
- **Stuck in Logo Page**. Press *'shift'* to enter GRUB menu and edit:
```
linux ... quiet spalsh nomodeset
```
‘Ctrl+X’ to save and F10 to restart your pc.

## **Nvidia driver installation**

check your GPU:
```
lspci | grep -i nvidia
```
install Nvidia driver:
```
sudo apt update
sudo ubuntu-drivers devices
```
there can be:
```
driver   : nvidia-driver-570 - distro non-free recommended
```
then install:
```
sudo apt install nvidia-driver-570
```
check your instalation:
```
nvidia-smi
```

## For double system (Wins11 + Ubuntu22)
```
sudo apt install os-prober
sudo nano /etc/default/grub
# GRUB_TIMEOUT=10
# GRUB_DISABLE_OS_PROBER=false
sudo update-grub
# Ctrl + O and Ctrl + X
sudo reboot
```
  


