# OpenLEDPar
Current state: only Schematic, no software

Reverse Engineering of an OEM LED Par with the goal to create a open source Firmware.

The LED Par in question is an Stairville Outdoor Stage Par 12x3W Tri, but judging by google image search there are many witj similar looking PCBs.
The Microcontroller is an STC STC12C5616AD. Each LED Driver is a PT4115. The STC could be simply reprogrammed over UART, but it can not be read. Hence a updating the firmware would be not reversible. STC12C5616AD are hard to get at the moment, so a small adapter PCB containing only a common MCU(EFM8?) seems like the way to go.

Probable Benefits:
- Custom DMX Profiles
- 16bit Resolution (the LED Driver claims a Contrast Ratio of 5000:1 which would be 12 bit, still better than 8)
- RDM: the transceiver is already fully wired, so only software changes would be necessary
- Automatic swiching to DMX if received.
![mainboard](https://user-images.githubusercontent.com/89604670/179404468-4fbaf212-467c-4b7c-ab31-ce2e79e3e6bd.jpg)
![Outdoor Stage Par](https://user-images.githubusercontent.com/89604670/179404744-946d5092-05e0-4f80-b54a-4865291ae6bb.svg)
