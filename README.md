# opencore
Open Core Configuration for a Sandy Bridge Processor

Specs: 
- Processor: Intel(R) Core(TM) i7-3820 CPU @ 3.60GHz
- Motherboard: Asus Sabertooth X79
- GPU: NVIDIA GeForce GTX 650 Ti 2 GB

Steps taken.
- Followed guide letter by letter from Dortania for Ivy Bridge Desktop: https://dortania.github.io/OpenCore-Install-Guide/
- SMBIOS MacPro6,1
- Got stuck, but added npci=0x3000 to boot-args.
- Verified config lock was unlocked.
- Made custom SSDT-EC from Manual steps tutorial.
- USB Ports were not active so then I found this solution: Make 2 ACPI patches in config.plist:
  EUSB to EH01 (45555342 to 45483031 )
  USBE to EH02 (55534245 to 45483032 ) 
- Installed MacOS Catalina 10.15.6
- Created SSTD-PM from ssdtPRGen for Power Management
- Created USBPorts.kext from Hackintool
- Installed OpenCanopy. Didnt bother with Chime because I don't have speakers to plug into the built-in audio (I use external audio interfaces usually).

Current Status:
-  Working like a gem
![Success Screenshot](https://github.com/aaronpfoltzer/opencore/blob/master/Images/Success-Screenshot.png)


NOT WORKING:
Sleep doesn't work completely because the monitors never come back up when waking.  Still searching for a solution.
