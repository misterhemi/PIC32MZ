# PIC32MZ
Code and Projects for the Microchip PIC32MZ series Microcontrollers

Including PIC32MZ USB without Harmony.

See the Microchip forum for basic USB and USB CDC ACM examples.
https://www.microchip.com/forums/m1083508.aspx#1083508

Here is an USB Audio Speaker example made using my USB device stack, without using Harmony.

UPDATE - 10 May 2020:
I added a "drop in" USB CDC ACM project. The main.c is only to be used as a reference, there are some
settings or initializations you'd need to add/include in your own project's main.c file.

It will work as-is for testing but it's intended to be copied into your project to save time and effort.
You only need to copy everything except the main.c file unless you intend to start your project with that.

There are four (4) files:
main.c
usb_cdc_acm.c
usb.h
usb_descriptors.h
 
NOTE: Pin/Port F3 is used on 100 and 144 pin device for the USBID. It may be different on other packages.
You can find the board initialization void initBoard() in main.c and you'll see:
 CNPUFbits.CNPUF3 = 1;       // Pull-up enabled on RPF3 (To set USB as a B-Device ) 



Mark S. Lewis AKA MisterHemi

mark(at)LewisTechnoGroup.com,
 misterhemi(at)yahoo.com
