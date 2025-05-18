# Intel-NUC-Board-NUC10i3FN/NUC10i5FN/NUC10i7FN

# Intel® NUC Products NUC10i3FN/NUC10i5FN/NUC10i7FN

# Technical Product Specification 

# Regulatory Models:

NUC10-i5 FNH (Slim Kit/Mini PC) 

NUC10-i7 FNH (Tall Kit/Mini PC) 

NUC10-i3 FNH (Board)

Current characterized errata, if any, are documented in a separate Specification Update.  See 
http://www.intel.com/content/www/us/en/nuc/overview.html for the latest documentation 

# OS Version Tested

# macOS Sequoia 15.5 (WiFi Need OCLP-Mod ) 

# The overall configuration list of my black Apple host is as follows:

| Part Type     | Part Model 
|---------------|------------------------------------------------------|
| Opencore      |  1.0.5                                               |
| Version       |  macOS Sequoia 15.5                                  |
| Motherboard   |  Intel NUC10 NUC10i7FNH                              |
| Hard disk     |  Coiorful CN600 1T M2                                |
| GPU           |  Intel UHD Graphics 620                              |
| CPU           |  Intel Core i7-10710U                                |
| Memory        |  2 x DDR4-2666 SO-DIMM RAM 32 GB                     |
| Wireless      |  network card: ntel AX210                            |
| network card  |  Wired 219Gb over Intel Ethernet connection to I1-V  |
| Power adapter |  19V，6.32A AC-DC                                    |
|               |                                                      |

# ntel® NUC Products NUC10i3FN/NUC10i5FN/NUC10i7FN Series Motherboards MacOS 15.4 Completeness:

CPU Normal Turbo Frequency (i3/i5/i7/etc.)

Solution 1: The onboard intel AX210 Bluetooth and WIFi can be driven, and the network speed is very good, but it does not support air-car. MacOS 15 requires the HELIPORT APP to use the WIFI function

Solution 2: The onboard intel AX210 Bluetooth and WIFi can be driven, and the network speed is very good, but it does not support air-carry; MacOS 15 requires OCLP-Mod patching here using option 2

I won't talk about them one by one

# OpenCore Configuration

# ACPI

| ACPIs                                    |
|------------------------------------------|
|  SSDT-AWAC                               |
|  SSDT-CpuPlug                            |
|  SSDT-SsdtEC                             |
|  SSDT-LPCB                               |
|  SSDT-DMAR                               |  

# Drivers

| Driver Name     |
|-----------------|
| OpenHfsPlus     |
| OpenCanopy      |
| OpenRuntime     |
| ResetNvramEntry |
| ToggleSipEntry  |

# Kexts

| Kext Name                             |
|---------------------------------------|
| Lilu.kext                             |
| VirtualSMC.kext                       |
| WhateverGreen.kext                    |
| SMCProcessor.kext                     |
| SMCSuperIO.kext                       |
| AppleALC.kext                         ||
| RestrictEvents.kext                   |
| XHCI-unsupported.kext                 |
| NVMeFix.kext                          |
| HibernationFixup.kext                 | 
| IntelMausi.kext                       | 
| USBToolBox.kext                       | 
| UTBMap.kext                           | 
| IO80211FamilyLegacy.kext              | 
| IOSkywalkFamily                       |
| AirportItlwm-15.5Sequoia.kext         | 
| IntelBTPatcher.kext                   | 
| IntelBluetoothFirmware.kext           |
| BlueToolFixup.kext                    |
| AMFIPass.kext                         |

# BIOS Setup Reference:

# Advanced

Advanced-Storage-SATA Mode Selection -> AHCI

Advanced-Video-IGD-Minimum Memory -> 64MB

Advanced-Video-IGD-Aperture Size -> 512MB

Advanced-Video-IGD-Primary Video Port -> or (Depends on your default monitor)ThunderboltHDMI

Advanced-Video-IGD-Secondary Video Port -> None

# Boot

Boot-Secure Boot-Secure Boot -> Disabled

Boot Priority-UEFI Boot -> Checked

Boot Priority-Legacy Boot -> Unchecked

Boot Priority-Fast Boot -> Unchecked

# Power

Power-Secondary Power Settings-Deep S4/S5 -> On

Power-Secondary Power Settings-Wake on Lan from S4/S5 -> Power On - Normal Boot

Power-Secondary Power Settings-Wake System from S5 -> Off

Power-Secondary Power Settings-Wake From Thunderbolt Device -> Off

# 关于打赏

如果您认可我的工作，请通过打赏支持我后续的更新(自觉打赏的人真少啊，免费的东西长久不了,现已改为需要密码解压，需微信或支付宝打赏入群。打赏记得留言备注你的qq号，然后申请入群时，填写你的留言为验证答案就是，我确认后会通过你的验证的。PS:之所以设置打赏，并不是为了赚大钱，当然大家打赏的多是有一些零花钱。主要是维护更新不易，每次系统一更新，有问题的话，就要工作时间之外花时间去调试，解决问题。普通群最多500人，无门槛的入群，不够用，有些机友对无门槛进入还不珍惜，进退群很随意，不看相关说明，上来就问问题的又多。不多说了，理解不理解的，就这样吧。

|  微信                                                                                 |
|---------------------------------------------------------------------------------------|
| ![1](https://github.com/user-attachments/assets/06d87fea-0d11-4bf4-b9ed-034dc7f53d06) | 
|                                                                                       |

若有其他问题请加Q群： 738882434
