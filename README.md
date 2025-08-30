# vGPU Proxmox Script
This is a little Bash script that configures a Proxmox 8 or 9 server to use Nvidia vGPU's. 
For further instructions see wvthoog's blogpost at https://wvthoog.nl/proxmox-7-vgpu-v3/

## WARNING !!!
- fastapi-dls is not working correctly with v18.x but working fine on v17.x, please consider this for extended use
- 17.6 & 18.1 is download only and only for natively support vGPU, lookup on NVIDIA for supported GPU ([v18.x](https://docs.nvidia.com/vgpu/18.0/product-support-matrix/index.html) & [v17.x](https://docs.nvidia.com/vgpu/17.0/product-support-matrix/index.html))
## Changes
Changes in version 1.2
- Added support for Proxmox 9.
- Removed support for Proxmox 7.
- Removed kernel pinning as it's no longer necessary.
- Integrated `pve-nvidia-vgpu-helper` for a more robust setup.
- Updated the host driver installation method and its service.
- Updated supported vGPU driver versions to 18.3, 18.4, and 19.0. Check [PVE Wiki](https://pve.proxmox.com/wiki/NVIDIA_vGPU_on_Proxmox_VE#Software_Versions).
- Removed support for older driver versions (16.x, 17.0).
- Switched from `megadl` to `wget` for downloading drivers from new URLs.
### Added driver versions 16
	16.0
	16.1
	16.2
	16.3
	16.4 / 16.5
	16.7
	16.8
	16.9 !!! USE THIS IF YOU ARE ON PASCAL OR OLDER !!!
### Added driver versions 17
	17.0
	17.1
	17.3
	17.4
	17.5
	17.6 (Only Native vGPU support)
### Added driver versions 18
	18.0
	18.1 (Only Native vGPU support)
- Added checks for multiple GPU's
- Added MD5 checksums on downloaded files
- Created database to check for PCI ID's to determine if a GPU is natively supported
- If multiple GPU's are detected, pass through the rest using UDEV rules
- Always write config.txt to script directory
- Use Docker for hosting FastAPI-DLS (licensing) or using this docker [fastapi-dls](https://github.com/GreenDamTan/fastapi-dls_mirror) container on any host or capable server
- Create Powershell (ps1) and Bash (sh) files to retrieve licenses from FastAPI-DLS

## 🚀 Contributing
All Credit belong to wvthoog for creating the V1.1 script

All Thanks to foxipan at this [repo](https://alist.homelabproject.cc/foxipan) for providing the required drivers/patches/custom

Many thank to everone on [vGPU Unlocking Discord](https://discord.gg/5rQsSV3Byq) for making vGPU easier for everone to get access, also this is the link for [vGPU-Patch](https://gitlab.com/polloloco/vgpu-proxmox)
