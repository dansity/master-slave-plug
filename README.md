# master-slave-plug

This is a basic master-slave power plug. I use it for my hi-fi where I want the amplifier to turn on the subwoofer.

The design does not contain 3d model as you can pick any box you want. I downloaded a parametric box from thingiversre and printed it as is. I prefer drilling holes after the box is done, faster and gives flexibility. So to simply put you can buy any box from an electrical supply shop or print a box for yourself.

Shopping list:
-2 wall mounted sockets. Don't buy ganged sockets as they are usually connected internally. Buy two individual single sockets.
-Any microcontroller. Project uses 1 digital pin and 1 analog pin which is available on almost any microcontroller. I have used an arduino nano.
-230V to 5v power supply or if your microcontroller works with 3.3V get a 3.3v power supply.
-Relay module (5v or 3.3V depending on the microcontroller)
-ACS712-20A current sensor module
-Wago connectors, 1x 4wire and 3x 2wire
-1.5mm2 solid core wire for the sockets - 3 colors
-0.14mm2 wire for the low voltage part - 3 colors
-M3 bolts and nuts to fix socket to box
-Some insulating tape or shrink tube

Instructions:
Measure the two sockets together and print a box that is the same size. For depth of the box 40mm will be sufficient but if you have a larger PSU you may print it thicker.
Fix the sockets on the box and connect all wiring according to the wiring schematic.

Add the Filters library attached to your Arduino library.
Upload code to the microcontroller. Change pin numbers if needed.
Current sensor will read -0.04A when no load then the rest of the readings under load will be similarly off by a hair. But this is enough for us to switch.

Now it is set to switch above 0.1A load so I can avoid it to turn on with my amplifier's standby. You can change this setting to your liking by modifying line 43:
current_amps > 0.1

Be very careful with the mains power, make sure inside the box no bare metal remains, use more insulation then less.

Shopping links:
mini 5v or 3.3v power supply https://t.ly/VjMxn
Wall mount socket (EU) https://t.ly/i39MG
5v relay module https://t.ly/qhUNn
OR
3.3V relay module https://t.ly/DT1ni
Arduino Nano https://t.ly/nQxX7
ACS712-20A Current sensor https://t.ly/Mymd4
