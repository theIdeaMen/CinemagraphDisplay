Cinemagraph Display
==============

A hackable digital picture frame optimized to display high quality animated gif's.

I designed version 0.1 on Upverter.com (very cool site) and even ordered boards from OSH Park before realizing that a) I wanted it to be hackable and b) I'm gonna need a 4-layer board.


I am now using DesignSpark PCB to design the schematics and board layout for version 0.2.

Version 0.2 uses an Atmel ARM Cortex-M3 as the main microcontroller. It has integrated USB and several UART/USART that are needed to interface to the LCD, the LCD controller, the accelerometer, and talking to user add-ons.

The whole device is Lithium-Polymer battery powered with micro-USB charging. A huge part of my design strategy is low power. To this end, I hope to sleep the display after no movement is detected by the accelerometer and wake back up when someone walks near it. This is the largest unknown for my project. Will I be able to distinguish human activity from a large truck passing by the house? Is the accelerometer even sensitive enough? I will find out.

The accelerometer will also be the user interface controls. I have always hated fingerprints on my screens so by tapping the edges of the frame for controls, no greasy LCD! This also makes the LCD cheaper by eliminating the touchscreen.

The LCD controller has different methods of interfacing to the microcontroller. I'm trying SPI first but I have my doubts on if it will be fast enough to handle animations.
