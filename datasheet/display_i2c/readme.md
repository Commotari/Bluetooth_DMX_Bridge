# Display

A makerhawk display with 128x32 pixel with an SSD1306 display controller chip has been ordered to do some tests.
It is a cheap, small 0,91" OLED display with white pixels. It should be good enough to visualize the status of the Bluetooth-DMX-Bridge.
The connection goes through I2C to the microcontroller board

### Pin header

| pin | description |
| --- | ----------- |
|  1  | GND |
|  2  | VCC (3.3V ... 5V) |
|  3  | I2C SCL |
|  4  | I2C SDA |


### Todo
* look at the driver interface from https://github.com/lexus2k/ssd1306
* document how it should be connected to the MCU board
* document how the driver should be separated (MPU independent abstraction through I2C driver)
* document defines in the source code (header file) for resolution, I2C address and parameters necessary
