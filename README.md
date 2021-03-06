Acer V5-573G Hackintosh
=======================

> All my hackintosh stuffs of Acer V5-573G

## News
- Shutdown/Sleep/Restart issues described in [issue 6](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/issues/6) was fixed! Check the [**Management-Engine-Firmware**](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/tree/master/Management-Engine-Firmware) folder!
- I also wrote a **Tutorial about the modification of DSDT/SSDTs**. If you have a different model of V5-573 and want to modify your own DSDT/SSDTs, please check [this Repo](https://github.com/Kaijun/Acer-V5-573g-DSDT)

## Releases

**[Click to Download Releases](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/releases)**

**‼️ Notice:** You need to modify the **Memory Section** of `SMBIOS` in the config.plist to fit your own specs! Since El Capitan, we have to define this section explicitly, otherwise it will cause kernel panic.
My own memory works in 2 channels, which means i need set two memory entries for slot `0` and `2` and the slot count for `4`, the reason:
>Set the Size and Frequency for each of the two memory entries to match your installed RAM. If you know the vendor, part, and serial for your memory you can edit those fields too (if not, just leave them as is). Leave the two memory entries set for slots 0 and 2 and the slot count set for 4 even though the board only has two slots (Clover wants to see slots 0 and 2 configured to treat the memory as dual-channel).

**Versions:**

- 2016-07-22: Clover-3556-El-Capitan-2016-07-22
  * Change ig-platform-id to 0x0a16000c which is more compatible with HD4400 [issue #39](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/issues/39)

- 2016-06-25: Clover-3556-El-Capitan-2016-06-26
  * Now Fn+Left/Right keys are working now! Only for VoodooPS2 Users(Synaptics).

- 2016-06-25: Clover-3556-El-Capitan-2016-06-25
  * Manage-Engine-Firmware files and tutorial are added, which fixed Shutdown/Sleep/Restart issues described in [issue 6](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/issues/6) !
  * USB in DSDT fixed

- 2016-06-18: Clover-3556-El-Capitan-18062016
  * fix USB (Rename EHCI->EH01, FakePCIID_XHCIMux.kext, USBInjectAll.kext)
  * new DSDT/SSDTs from Bios 2.30, new [DSDT repo](https://github.com/Kaijun/Acer-V5-573g-DSDT)

- 2016-06-17: Clover-3556-El-Capitan-17062016


## Branches:
- [el-capitan-10.11---i7-4500U](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/tree/el-capitan-10.11---i7-4500U) maintained by [michaelspeed](https://github.com/michaelspeed)
- [el-capitan-10.11---i5-4200U-TouchScreen](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/tree/el-capitan-10.11---i5-4200U-TouchScreen) maintained by [Silveryard](https://github.com/Silveryard)
- archieve branches: check yourself 😄

## Overview

**Working**

- HD4400 graphic card
- Disabled NVIDA Geforce graphic card under DSDT
- Sounds: AppleHDA
	* Legacy Method (install the patched Kext)
	* New Method (Auto Patch even the OS X updates, needn't to install patched Kext any more)
- TouchPad: VoodooPS2Controller
- Brightness
- SpeedStepping (w/o Turbo Boost)
- Sleep
- Shutdown
- USB (to be test)

**Not Working**
- internal Wifi card, it must be replaced (buying suggestions see below)
  - i'm using `BCM94322HM8L` which doesn't contain the BlueTooth module.
  - `BCM943225HMB` with BlueTooth which is suggested by [@virusak](https://github.com/virusak) in [Issue #4](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/issues/4#issuecomment-56149694).
- to be tested: accidentally shutdown/sleep problem
  - description && ***temporary solution***: have a look at [Issue #6](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/issues/6)

=======

## Installation Guide

A brief guide to the installation wrote by [@Majkwin](https://github.com/Majkwin) plz see [Issue #7](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/issues/7). Thank him!

=======

## Feedback
Plese do not hesitate to contact me by using the **[issue function](https://github.com/Kaijun/Acer-V5-573G-Hackintosh/issues)**, if you have any questions about the setup.

## License

The source code is released under [GPL v3](http://www.gnu.org/copyleft/gpl.html) or (at your option) any later version.
