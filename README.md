# Stock-exchange-box
a 3D printed stock exchange box based on ESP8266 MCU controller

STL files available for 3D printing.

Pictures of the results can be seen here: https://www.facebook.com/photo.php?fbid=2633748539989628&set=a.101039313260576&type=3&theater

The ESP8266 needs to be mounted on a small breadboard and you need to use one of these small 220V to 5V or 3.3V block supplies to supply the unit. How to mount everything i leave to your skills. The connection for the buttons should be clear from the code.

The Frans van Hout stock exchanged box is based on the stock exchange price of Philips but you can target any other company of course by changing the API calls.
The box contains a ESP8266 controller which pulls the stock exchange price via a API from Internet and displays the price on a 7 segment display.
The unit contains a green and red LED which indicates the average price last hour going up (green LED)  or down (Red LED).

In the published code we have changed the SSID and API keys which you need to replace by your own code.

The code needs to be inserted in Platform IO.

The Platform IO config file looks like this:

; PlatformIO Project Configuration File
;
;   Build options: build flags, source filter
;   Upload options: custom upload port, speed and extra flags
;   Library options: dependencies, extra library storages
;   Advanced options: extra scripting
;
; Please visit documentation for the other options and examples
; https://docs.platformio.org/page/projectconf.html

[env:nodemcuv2]
platform = espressif8266
board = nodemcuv2
framework = arduino

monitor_speed = 115200

# using GIT Url (the latest development version)
lib_deps = https://github.com/arduino-libraries/NTPClient.git




