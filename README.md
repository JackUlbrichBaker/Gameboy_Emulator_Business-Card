# Gameboy_Emulator_Business-Card
This is a continuation of my Business Card design "series" in which I create various circuits with a footprint that of a typical business card with a low enough cost to theoretically give out as business cards. 


# Hardware
This uses an Allwinner V3s SOC that performs all the computing. While this is a great powerful and low cost chip there is very little documentation (especially in english) which made development very difficult.  However with the below specs for roughly $3 per chip I couldn't pass it up.
Specs: 
- ARM Cortex TM -A7 MP1 Processor @ 1.2GHz
- 32kB L1 Instriction Cache
- 128kB L2 Cache
- internal 512Mbit DDR2 
- 32kB internal memory
- Support for eMMC and TF (SD) Cards.

Power:
The power is handled by the EA3036C BMS and buck converter IC.  This has three internal buck converters and a single cell LiPO battery management system which allows it to power all the IO pins that the Allwinner V3s requires. (3.3V, 1.8V and 1.2V), which allows the system to be portable, or powered by a usb cable.

# Software
The Software used is the RetroARCH OS, using Buildroot to configure the os for the system.
