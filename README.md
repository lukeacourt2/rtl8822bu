# 8822BU for Linux

Driver for 802.11ac USB Adapter with  
RTL8822BU chipset  
Only STA/Monitor Mode is supported, no AP.  

A few known wireless cards that use this driver include 
* [Edimax EW-7822ULC](http://us.edimax.com/edimax/merchandise/merchandise_detail/data/edimax/us/wireless_adapters_ac1200_dual-band/ew-7822ulc/)
* [ASUS AC-53 NANO](https://www.asus.com/Networking/USB-AC53-Nano/)
* [D-Link DWA-182 (Revision D1 only)](http://ca.dlink.com/products/connect/wireless-ac1200-dual-band-usb-adapter/)
* [TP-Link Archer T4U ver.3](https://www.tp-link.com/us/home-networking/usb-adapter/archer-t4u/)


> NOTE: At least v4.7 is needed to compile this module
> sorry people with older kernels, the code is removed.
> Upon request I can work towards making it backwards compatible.

Currently tested on X86_64 platform **only**,  
cross compile possible.

## DKMS
Automatically rebuilds and installs on kernel updates. DKMS is in official sources of Ubuntu, for installation do:
```
sudo apt-get install build-essential dkms
```

Then install the module using dkms do in source dir:
```
sudo dkms add .
sudo dkms install -m 88x2bu -v 1.1
```
This will make the module install on every kernel update



