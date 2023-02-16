# Development thoughts

### PCB size
the size of the PCB should be bigger than all the MCU boards that could be used on top.
the biggest is probably the Nucleo board from STM NUCLEO-WB55RG and NUCLEO-WB15CC (70x82mm).

the board also need to be long enough to fit XLR connectors on it.
the pcb size should be a multiple of 2.54mm (0.1") * 5 = 12,7mm to have a millimeter measurement with only one digit behind the comma?
1st proposal to start with:
- length 127mm
- width 88,9mm

### Arduino Connector
- width between the two pin rows: 48.26mm (19 * 0.1")
- lower left pin row with 6 pins
- higher left pin row with 8 pins
- lower right pin row with 8 pins
- higher left pin row with 10 pins
- space between higher and lower pin row is 1 pin = 0.1"

### Power Supply
the different MCU boards usually come with a USB connector.
the hardware on the main pcb should be constructed in a way that the power can be supplied from the mcu boards.
not much power is needed for that. maybe approx. 100mA for the display, and 50mA for the RS485 circuit.

### Display
there are cheap small oled displays availabe with an I2C bus interface to reduce pins. this is good for the development version.
in a cost reduced version, only LEDs might be used. popular and easy to find are:
* 128x32 oled display 0,91"	with SSD1306 controller
* 128x64 oled display 0,96" with SSD1306 controller
* 128x64 oled display 1,30" with SSH1106 controller

### Status LEDs
maybe some status LEDs could be provided to show the bluetooth connection status and data transfer.
the LED activity should be configurable through bluetooth in case the LED flashing is disturbing the darkness on the stage.
also a kind of boot up flashing would be nice to show that the device is working.

### Buttons
some buttons to reset the bluetooth pairing etc. would be nice.
evtl. more buttons and a menu on the display could make sense.
the I2C bus with an input chip could be used too, if we already use I2C for the display.

### Case and Positioning of GUI elements
the display, LEDs, and buttons could be placed on the back side of the main pcb to be very close to the upper side of the case.
the size of the buttons and leds can be defined in a way to have the same distance from the pcb.
the case could be 3d-printed to have the holes in the right way for the display, buttons and LEDs.



