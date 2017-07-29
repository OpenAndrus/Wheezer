# Wheezer
Intel Hackathon 2017
Project Link: https://devpost.com/software/wheezer-418n3w

# What is it?
Our device measures the exhalation flow rate via the pressure drop through a venturi. Based on the venturi dimensions, the fluid density, and the pressure drop, the flow rate can be calculated and integrated for the total lung capacity. This information is plotted on a digital display on the device and is also transmitted via bluetooth to a connected android device.

# Circuit Diagram
![GitHub Logo](https://github.com/TylerBerzzz/Wheezer/blob/master/Electrical%20Schematic/Schematic.png?raw=true)
![GitHub Logo](https://github.com/TylerBerzzz/Wheezer/blob/master/Electrical%20Schematic/schematic_info.png?raw=true)

To avoid the lower resolution of the Arduino 101*, we needed to use a differential pressure sensor with i2c communication. We chose to use the SM5812 because it was affordable and had the option to output data over i2c or its analog output. We wanted our device to be portable, so we chose a 3.7V 500 mAh battery from Adafruit. The SM5812 needs to have 5V, so we chose the Powerboost 500c charger in order to boost the battery voltage. The Powerboost 500c charger also has the capability to charge the battery, which is super aweosome. When we started the project, the 1.44" TFT LCD Display was going to perform the realtime graphing operations for the data; however, we ended up deciding to switch to performing the realtime operations on an Android device through Bluetooth (which kind of defeats the purpose of the LCD.) This switch allowed us to fully use the arduino 101's BLE. 

*Purchasing links are in the BOM section.

# Datasheets
SM5812: http://www.mouser.com/ds/2/589/SM5812-254991.pdf

# BOM (Build of Materials)
+ Adafruit 1.44" Color TFT LCD Display with MicroSD Card breakout: https://www.adafruit.com/product/2088#tutorials
+ PowerBoost 500 Basic - 5V USB Boost @ 500mA from 1.8V+: https://www.adafruit.com/product/1944
+ Lithium Ion Polymer Battery - 3.7v 500mAh: https://www.adafruit.com/product/1578#tutorials
+ Switch: We just found a spdt switch lying around somewhere
+ Arduino 101 Curie
