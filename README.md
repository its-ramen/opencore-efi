# OpenCore-Efi
This is an OpenCore implemenation for a custom build PC.
If you have a similar system, download the contents of the OpenCore 0.6.2 folder, and extract it to a folder called "EFI" in your EFI partition.
See https://dortania.github.io/OpenCore-Install-Guide/ for more details.
The config.plist was configured with minimalism and security as the primary design goals.

## OpenCore 0.6.2
A copy of my EFI folder using OpenCore version 0.6.2

### Boot
Contains bootx64.efi, nothing special here

### OC
Contains OpenCore files.

#### ACPI
In this folder is a custom SSDT made specifically for the **ASUS ROG STRIX B450-f gaming**.
If you have this motherboard in your hackintosh build, this should work for you.

#### Bootstrap
Default from OpenCore

#### Drivers
| Driver | Description |
|HfsPlus.efi | so that OpenCore can read HFS partitions like TimeMachine and Install MacOS installers |
|OpenCanopy.efi | for a clean, graphical boot picker |
|OpenRuntime.efi | standard for OpenCore |

#### Kexts
| kext | Description |
| AppleALC.kext | enables macOS HD audio |
| Lilu.kext | kext, library, and program patching |
| SmallTreeIntel82576.kext | this is required for the NIC card on the motherboard
| VirtualSMC.kext | SMC (system management controller) emulator |
| WhateverGreen.kext | patching for GPUs (In my case, RX 580) |

#### Resources
Contains resources for the OpenCanopy GUI boot picker. You can customize its appearance by changing these files.

#### Tools
Empty. Not needed.

#### OpenCore.efi
This is the EFI

#### Config.plist
Contains the settings for OpenCore.
Verbose and logging are all turned off. If you have any issues booting, you will want to re-enable them.
Security settings are on by default, but there was one I had to turn off to enable OpenCore to read a **FileVault** encrypted drive.

### Use this software at your own risk. I am not liable for any damages as the result of this software nor is there any guarantee written or implied that this software will work.
