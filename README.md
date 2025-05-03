
THIS SCRIPT IS NOT WORKING AND BEING BUILT, PLEASE DON'T CLONE OR FORK THIS REPO

This is a little Bash script that configures a Proxmox 7 or 8 server to use Nvidia vGPU's. 

For further instructions see wvthoog's blogpost at https://wvthoog.nl/proxmox-7-vgpu-v3/

Changes in version 1.2
- Added driver versions 16
    16.0
    16.1
    16.2
    16.3
    16.4 / 16.5
    16.6
    16.7
    16.8
    16.9 !!! USE THIS IF YOU ARE ON PASCAL OR OLDER !!!
  - Added driver versions 17
    17.0
    17.1
    17.3
    17.4
    17.5
    17.6 (Only Native vGPU support)
- Added driver versions 18
    18.0
    18.1 (Only Native vGPU support)
- Added checks for multiple GPU's
- Added MD5 checksums on downloaded files
- Created database to check for PCI ID's to determine if a GPU is natively supported
- If multiple GPU's are detected, pass through the rest using UDEV rules
- Always write config.txt to script directory
- Use Docker for hosting FastAPI-DLS (licensing)
- Create Powershell (ps1) and Bash (sh) files to retrieve licenses from FastAPI-DLS

All Credit belong to wvthoog for creating the V1.1 script

All Thanks to foxipan at https://alist.homelabproject.cc/foxipan for providing the required drivers/patches/custom

Many thank to everone on vGPU Unlocking Discord for making vGPU easier for everone to get access (https://discord.gg/5rQsSV3Byq) 
