TWRP Device Tree for X96 Max (u212)
===================================

The Amlogic X96 Max (codenamed _"u211/212"_ or _"franklin"_) have following parameters:

Basic                   | Spec Sheet
-----------------------:|:-------------------------
CPU                     | Octa-core Amlogic S905X2
GPU                     | Mali-G31 MP2 Dvalin
Shipped Android Version | Android 8.1
Memory                  | 32 or 64 GB + 4GB LPDDR3 RAM
MicroSD                 | microSD, up to 512 GB (dedicated slot)
Network                 | Gigabit Ethernet, WIFI 802.11 b/g/n/ac, Bluetooth 4.0
Video                   | HDMI 2.1 to 4K with 75 Hz + HDR, AV 3,5mm.
USB                     | USB 3,0x1, USB 2,0x1
Power Supply            | 5W/2A
Misc			| IR-port, and microSD Slot

![Amlogic X96 Max](https://imgaz3.staticbg.com/thumb/large/oaupload/banggood/images/D0/6D/44667003-0534-4050-9249-6ab6dff88431.jpg "Amlogic X96 Max")

## Compile

First checkout Minimal TWRP with OmniROM Tree:

```
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
repo sync
```

And execute these:

```
export ALLOW_MISSING_DEPENDENCIES=true # Only if using Minimal TWRP Tree
. build/envsetup.sh
lunch omni_u212-eng
mka recoveryimage
```

## Installing:

Testing it:
```
fastboot boot out/target/product/onclite/recovery.img
```

Flash it via fastboot:
```
fastboot flash recovery recovery.img
```

Or use Official TWRP App to install it.
