# Ubuntu22-Installation

## prepare 2 independent ssd and usb with ubuntu iso
I have a m2 ssd with Win11 on it, and will install ubuntu on another new m2 ssd.
My pc is Alienware R15 (Nvidia GTX 4070Ti). Entering BOIS with F2 quite after the Alienware Logo appearing.
(Actually I do not found the option for setting USB as prior entry option, so I just reboot and I smoothly enter the ventoy page.)

## Installation
The installation process is way like that of virtual machine Ubuntu:
Each option setting to default will be good.

## Problem you may counter
- **Stuck in Logo Page**. Press e on '''Try or install ubuntu''' to edit instead of entering that option: add 'nomodeset' after quick spalsh:
  ```
-- linux ... quick spalsh nomodeset
  ```
This will set driver to unseen temporarily.

-

  


