LED strip for LIFX app
=======
This is a project for remote controlling of LED strips connected to arduino via original mobile LIFX application.
This code will work with controllable and uncontrollable stips as well. 
Actually, that project based on FastLED library and kayno/arduinolifx project. All of the following is possible only 
coz of you, guys, big thanks for your examples! 

So via this project you can ezly control a wide variety of LET strips chipsets, like the ones
sold by adafruit (Neopixel, LPD8806), Sparkfun (WS2801), and aliexpress and actually of all other chips, 
which are supported by the fast led library.


## Supported LED chipsets

Here's a list of all the LED chipsets are supported.  More details on the led chipsets are included *TODO: Link to wiki page*

* Adafruit's Neopixel - aka the WS2812B (also WS2811/WS2812, also suppored in lo-speed mode) - a 3 wire addressable led chipset
* TM1809/4 - 3 wire chipset, cheaply available on aliexpress.com
* TM1803 - 3 wire chipset, sold by radio shack
* UCS1903 - another 3 wire led chipset, cheap
* LPD8806 - SPI based chpiset, very high speed
* WS2801 - SPI based chipset, cheap and widely available
* SM16716 - SPI based chipset
* DMX - send rgb data out over DMX using arduino DMX libraries

LPD6803, HL1606, and "595"-style shift registers are no longer supported by the library.  The older Version 1 of the library ("FastSPI_LED") has support for these, but is missing many of the advanced features of current versions and is no longer being maintained.

so, for quick setup you should do the next tips: 
## Setup for controllable strips:
* open the RGBMoodLifx.cpp 
* set the count of your LEDs in the strip to the end of the string "#define NUM_LEDS "
* set the pin number for controlling your strip from Arduino in #define DATA_PIN 
* set the type of your LED controller to the #define CONTROLLER_TYPE


## Setup for uncontrollable RGB strips:
* open the lifx_rebuilding.ino
* set the pins for red, green and blue LED pins to the const int redPin, const int greenPin and const int bluePin.

also you have to set unique MAC-adress into byte mac array in lifx_rebuilding.ino.


Special big thanks to:
https://github.com/kayno/arduinolifx
https://github.com/FastLED/FastLED (http://fastled.io/)
https://github.com/magicmonkey/lifxjs/
and others! 




