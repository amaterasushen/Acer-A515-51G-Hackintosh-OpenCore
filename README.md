# Acer-A515-51G-Hackintosh-OpenCore

This is an upgraded fork from [SiddheshNan/Acer-A515-51G-Hackintosh-OpenCore](https://github.com/SiddheshNan/Acer-A515-51G-Hackintosh-OpenCore) with fewer bugs and constant updates.

[![Join the chat of the original repo at https://gitter.im/Acer-A515-51G-Hackintosh](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Acer-A515-51G-Hackintosh/community)


### To get support just leave an issue with a description of your problem and an image or gif if you feel inspired.

<details><summary>Ps: CMD + SHIFT + 5 opens record/print bar on macOS</summary>
Then you just need to paste it here - records are saved as .mov and need to be converted to .gif before pasting here.
</details>

---

#### Supports MacOS 13 Beta 2

<p align="center">
  <img src="https://user-images.githubusercontent.com/26356962/178634733-d7b1aaf7-8f84-4f87-a0dc-5f99f18788b1.png"  width="400px" alt="Specs">
</p>


## What's Working...
 - [x] Audio & headphone jack
 - [x] CPU Speedstep
 - [x] iGPU with disabled dGPU
 - [x] Fully Functional QE/CI Enabled Graphics
 - [x] Battery Management
 - [x] ACPI Display brightness with hot keys / slider
 - [x] Ethernet
 - [x] HDMI + Audio
 - [x] Smart Touchpad + Gestures (using Basic Mode)
 - [x] WebCam
 - [x] Usb 3.0 + Type C
 - [x] WiFi (2.4 + 5GHz) and Bluetooth from Intel (using AirportItlwm)
 - [x] Native hotkey support with Fn keys
 -  Sleep + Wake

 ### Known Issues
- Trackpad in Advance Mode, Only Basic mode works (but with all with gestures)!

### Not Tested
 - Internal SD card Reader (probaby need to map it through Windows)

### Important
 Please add `SystemSerialNumber`, `SystemUUID` and `MLB`.


## Installation

 ### BIOS Settings
* *Security* → Set supervisor password (to disable secure boot)
* *Security* → Password on boot → **Disable**
* *Boot* → Secure Boot → **Disable**
* *Boot* → Boot Mode → **UEFI**
* *Main* → Touchpad → Set touchpad mode → **Basic** *TODO: Advance Mode*
* *Main* → Lid Open resume → **Enabled**

###  Basic Installation

- Download and install the latest release of [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools/releases/) for the system you are using;
- Download this repo and open `config.plist` on OCAuxiliaryTools;
- With OCAuxiliaryTools fill `config.plist` with the closest info to your hardware. You will also need a matching SystemUUID and SystemSerialNumber as shown here: ![Screen-Recording-2022-07-12-at-23 12 48](https://user-images.githubusercontent.com/26356962/178636873-86c0d8a9-0ff1-4ec5-a611-375c10d71038.gif)
- Create a Bootable USB for MacOS by using by Dortania's [OpenCore-Install-Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/). (remember to add our EFI to the Bootable USB and to select MacOS Monterey or Ventura Beta 2 when downloading the system)
- **[IMPORTANT]** Make sure to Generate system definitions of MacBook pro 14.2 in config.plist file using OCAuxiliaryTools or [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) & add `SystemSerialNumber`, `SystemUUID` and `MLB`.
- Install MacOS to SSD / Hard drive. (While installing, connect USB keyboard and mouse).
- After installing the system copy **ALL** the contains of this Repo inside the EFI partition of SSD / Hard drive. (Will don't want to need your USB stick to boot everytime, but it's good to keep a copy of the EFI on it even after the install)

### Post Installation
- If you have Installed MacOS on SSD, Enable TRIM using following command (not recommended if dualbooting within the same drive):

```sh

$ sudo trimforce enable

```


<p align="center">
<b>⭐ Please consider starring this repository if it helped you! ⭐</b>
</p>

