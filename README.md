# arduino-leonardo-uploader
Simple wrapper for avrdude to allow firmware upload to Arduino Leonardo from command line

That's very common problem referenced on Arduino forums and Stackexchange - when you try to upload 
firmware to Arduino Leonardo and clones with avrdude, you get programmer timeout error message.

Reason for it is very simple - Arduino Leonardo should be reset to provide another serial port for flashing

This repository contains simple Windows-based bat file that identifies your Arduino Leonardo COM port through WMIC, performs COM port reset, then identifies bootloader COM port and invokes avrdude to upload firmware from firmware.hex file

firmware.hex file is empty here, please put yours. 

avrdude binary and config is taken from Arduino IDE 1.8.3

OS X and Linux version coming soon, idea is pretty much the same - to use stty to control serial port.
