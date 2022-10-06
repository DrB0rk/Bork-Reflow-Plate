###### Originally by AfterEarth Ltd and edit by DrB0rk

# **Bork Reflow Plate**

This is a collection of tweaks and changes for the v3 of the board and i made a handy tutorial for uploadinng the firmware because i really struggled to find everything. so i thought why not put everything in one place!

## tutorial

This tutorial shows how to upload the firmware to the Atmega4809 using an arduino nano (Atmega328P) programmer. if you have any problems feel free to contact me
 
1. Download/Clone the repo [here](https://github.com/ElTangas/jtag2updi) and rename the folder "source" to "jtag2updi" (otherwise the Arduino IDE won't open it)

2. Open `jtag2updi/jtag2updi.ino` in your Arduino IDE

3. Configure the flasher options for your Arduino Nano and flash it
```
Board: Arduino nano
Processor: Atmega328p (somtetimes Atmega328p(Old Bootloader) may be needed)

Port: (port of your nano)
``` 

4. Add the MegaCoreX hardware package to the Ardunio IDE (found [here](https://github.com/MCUdude/MegaCoreX#how-to-install))

5. Install the Adafruit_GFX, Adafruit_SSD1306 and Debounce2 libraries with the Library Manager (`Sketch > include library > manage libraries`)

6. Download and open the ino in this repo found [here](https://github.com/DrB0rk/Bork-Reflow-Plate/blob/main/Board%20Versions/70mm%20by%2050mm%20Ver3.0%20ATmega4809/Software/SW1.0_HW3.0_70by50mm/SW1.0_HW3.0_70by50mm.ino)

7. Connect ds on the arduino nano to the updi pin on the board through a 4.7k ohm resistor, and connect GND and 5v from the arduino to the board

8. Select the options below

```
Board: Atmega4809
Clock: Internal 16 MHz
BOD: BOD2.6V
EEPROM: EEPROM retained
Pinout: 48 pin standard
Reset pin: reset
Bootloader: No bootloader
port: (select the com port of your nano)

Programmer: Jtag2updi
```

11. upload the sketch using your programmer (`sketch > upload using programmer`)

## Versions

- 70mm x 50mm (Ver 2.4)
  - 12VDC (5A Minimum)
  - 5.5mm x 2.5mm Barrel Jack
  - 0.91" OLED Display
  - ATmega328p Microprocessor

- 70mm x 50mm (Ver 3.0) **NEW**
  - 12VDC (5A Minimum)
  - 5.5mm x 2.5mm Barrel Jack
  - 0.91" OLED Display
  - ATmega4809 Microprocessor
