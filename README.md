# usb-wifi ubuntu 18.04

Driver for 802.11ac USB Adapter with:
rtl8822bu chipset
Only STA/Monitor Mode is supported, no AP.

A few known wireless cards that use this driver include

- Edimax EW-7822ULC
- ASUS AC-53 NANO
- D-Link DWA-182 (Revision D1 only)
- tp-link Archer T4U (Revision V3 only)

## Installing

compiling in source dir:
```
make

sudo make install
```
## DKMS
Then install the module using dkms do in source dir:
```
sudo apt-get install build-essential dkms

sudo dkms add .
sudo dkms install -m 88x2bu -v 1.1
```

## Uninstall
In order to uninstall the module:
```
sudo dkms remove -m 88x2bu -v 1.1 --all
sudo rm -rf /usr/src/88x2bu-1.1
```

## Reference
https://github.com/EntropicEffect/rtl8822bu
Driver - tp-link Archer T4U 