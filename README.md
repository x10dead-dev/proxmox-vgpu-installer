
THIS SCRIPT IS NOT WORKING AND BEING BUILT, PLEASE DON'T CLONE OR FORK THIS REPO

This is a little Bash script that configures a Proxmox 7 or 8 server to use Nvidia vGPU's. 

For further instructions see wvthoog's blogpost at https://wvthoog.nl/proxmox-7-vgpu-v3/

Changes in version 1.2
- Added new driver versions
    16.2
    16.4
    17.0
    17.6
    18.1
- Added checks for multiple GPU's
- Added MD5 checksums on downloaded files
- Created database to check for PCI ID's to determine if a GPU is natively supported
- If multiple GPU's are detected, pass through the rest using UDEV rules
- Always write config.txt to script directory
- Use Docker for hosting FastAPI-DLS (licensing)
- Create Powershell (ps1) and Bash (sh) files to retrieve licenses from FastAPI-DLS

All Credit belong to wvthoog for creating the V1.1 script
