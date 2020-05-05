# ubuntu-base-setup

To dual boot Ubuntu with XPS 9560

https://medium.com/@pwaterz/how-to-dual-boot-windows-10-and-ubuntu-18-04-on-the-15-inch-dell-xps-9570-with-nvidia-1050ti-gpu-4b9a2901493d

Steps:
- BIOS
  - Disable Secure boot 
  - Enable Legacy ROMS, Enable Legacy Attempt ROMS
  - Change SATA from RAID to AHCI
- Windows 
  - Make sure IDE ATA/ATAPI controller” is “Intel(R) 100 Series/C230 Chipset Family SATA AHCI Controller” under Device Manager
  - Installed latest BIOS and SATA drivers from Dell
- Ubuntu installation
  - When I was trying to install with USB installation, it would get to the Checking files screen and just shutdown. Following seemed to get around it. Also try installing from Ubuntu Safe mode.
  - Added `nouveau.modeset=0` to boot options to disable Nvidia drivers initally.
  - References: 
    - https://github.com/rcasero/doc/wiki/Ubuntu-linux-on-Dell-XPS-15-(9560)
    - https://github.com/rcasero/doc/issues/6