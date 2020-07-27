# opencore
Open Core Configuration for a Sandy Bridge Processor

Specs: 
- Processor: Intel(R) Core(TM) i7-3820 CPU @ 3.60GHz
- Motherboard: Asus Sabertooth X79
- GPU: NVIDIA GeForce GTX 650 Ti 2 GB

Steps taken.
- Followed guide letter by letter from Dortania for Ivy Bridge Desktop: https://dortania.github.io/OpenCore-Install-Guide/
- Got stuck, but added npci=0x3000 to boot-args.
- Verified config lock was unlocked.
- Made custom SSDT-EC from Manual steps tutorial.
- Attempted to get USBPorts working but no luck.

Current Status:
- Can boot to existing MacOS 10.15.6 installation.
- NO MOUSE OR KEYBOARD
- Cannot login.
- Cannot boot from thumb drive to installer because USB does not work after selecting the MacOS Installer from Open Core menu.
