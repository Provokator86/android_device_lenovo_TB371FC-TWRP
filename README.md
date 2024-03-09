## Xioaxin Pad Pro 12.7（SM8250）TWRP Device Tree

### It has been fixed                              

- [x] Decrypt

- [x] Touch

- [x] Power display

- [x] USB

- [x] ADB

- [x] Bootloop

- [x] 花屏

- [x] FastbootD

### not fixed

- [ ] The screen only has a small bar to display

All other functions are by default

### problem

The current problem is that the core of Lenovo Xiaoxin’s tablet has not yet been open sourced, so the display problem has not been solved. The problem currently identified is dsc

The expected solution is to disable dfps:

- [ ] Try to modify the dtbo - Does not work

Most likely the problem is in selinux permission

- avc: denied { read write } for name="card0"
- avc: denied { open } for path="/dev/dri/card0"
- avc: denied { ioctl } for path="/dev/dri/card0"
- avc: denied { module_load } for path="/vendor/lib/modules/lcd.ko"
- etc



The kernel of this TWRP is based on version 575. If your version is inconsistent with this version, you need to re-import the kernel of the same version, otherwise the system will not start.

