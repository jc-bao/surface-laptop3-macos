# Surface Laptop 3 13/15" OpenCore EFI for macOS Ventura/Sonoma/Sequoia

<!-- add github tags here -->
[![macOS](https://img.shields.io/badge/macOS-13.6.4-blue)](https://www.apple.com/macos/big-sur-preview/)
![OpenCore](https://img.shields.io/badge/OpenCore-0.9.1-9cf)

| **Surface Laptop 3 15"** | **macOS Ventura** | **macOS Sequoia** |
| ------------- | ------------- | --- |
| ![](figs/laptop.jpeg) |![](figs/screenshot.png) | ![](figs/sonoma.png) |

## Features

* Running macOS Ventura/Sonoma/Sequoia without major issues. 
* Support Bluetooth 4.0+ devices with the solution provided by [this issue](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/issues/51). 

## Hardware

* **CPU**: Intel Core i5-1035G7
* **iGPU**: Intel Iris Plus Graphics G7
* **Memory**: 16 GB 3733 MHz LPDDR4X
* **Storage**: 256 GB NVMe SSD HFM256GDGTNG-87A0A

## Current status

| Component | Status | Notes |
| --------- | ------ | ----- |
| CPU | ✅ | |
| iGPU | ✅ | |
| Audio | ✅ | |
| USB | ✅ | |
| Touchpad | ✅ | |
| Keyboard | ✅ | |
| Battery | ✅ | |
| Bluetooth | ✅ | |
| Front camera | ✅ | Working with USB mapping. |
| Graphics Acceleration | ✅ | |
| WiFi | ✅ | Airdrop, Handoff, Sidecar are not working. This is a known issue for `itlwm`. |
| Touchscreen | ✅ | For multi-touch, you need to install IPTSDaemon. |
| Sleep | :white_check_mark: | Can sleep and wake up well thanks to [jlempen](https://github.com/jlempen/Surface-IceLake-macOS-Hibernation-Fix/tree/main)'s method. |


## Installation

Please follow the [OpenCore guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) to create a bootable USB. Then replace the `EFI` folder with mine.

> Note: it is normal to have screen flickering during installation. 

## Post installation

* **Enable HiDPI** (optional): the default setting only supports HiDPI given a certain resolution. To enable more HiDPI options, I used BetterDisplay and enabled the smooth scaling feature. You can also try [one-key-hidpi](https://github.com/xzhih/one-key-hidpi). 
* **Wireless Network**: I use [itlwm](https://github.com/OpenIntelWireless/itlwm), don't forget to install [HeliPort](https://github.com/OpenIntelWireless/HeliPort) to manage the wireless network.
* **Change SMBIOS**: Please do not use the same SMBIOS as mine. Generate your own SMBIOS with [GenSMBIOS](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html). 

## Credits

* [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) for the OpenCore guide.
* [OpenIntelWireless](https://openintelwireless.github.io) for the WiFi and Bluetooth solution.
* [Surface Pro 7 OpenCore EFI](https://github.com/badstorm/surface-pro-7-opencore) for the initial OpenCore configuration.
