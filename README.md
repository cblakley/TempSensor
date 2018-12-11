# TempSensor


## Table of Contents
1. [Introduction](#introduction)
2. [TempSensor Specifications](#TempSensor-specifications-and-parts)
3. [TempSensor Design Files](#TempSensor-design-files)
4. [TempSensor Assembly](#TempSensor-assembly)

## Introduction

The TempSensor i2c device is a fully enclosed temperature and humdity sensor. The  The TempSensor is built on the Broadcom develompent platfrom, using a Raspberry Pi 3B+. The device reads in temperature and humidity data and using a python script it displays the infromation to the user. 

## TempSensor Specifications and Parts

In order the build the TempSensor a couple of things are needed first. A full list of parts is avilable [here](https://github.com/cblakley/TempSensor/blob/master/Documentation/CENG319Budget.xlsx?raw=true).

Most importantly the Raspberry Pi. If one is not avalible I'd recommend the Canakit starter kit which is avalible [here](https://www.amazon.ca/CanaKit-Raspberry-Starter-Premium-Black/dp/B07BCC8PK7/ref=sr_1_1_sspa?s=pc&ie=UTF8&qid=1543943043&sr=1-1-spons&keywords=raspberry+pi+3+b%2B&psc=1) from Amazon Canda.

The AM2315 Sensor itself avalible [here](https://www.adafruit.com/product/1293) from Adafruit.

![Image of Sensor](https://cdn-shop.adafruit.com/970x728/1293-01.jpg)

One 4 pin header avalible [here](https://www.digikey.ca/product-detail/en/sullins-connector-solutions/PPTC041LFBN-RC/S7002-ND/810144) from Digi-Key.

![Image of Header](https://media.digikey.com/photos/Sullins%20Photos/PPTC041LFBN-RC_sml.jpg)

One 6 I/O pin Elevated Socket Connector avalible [here](https://www.digikey.ca/products/en?keywords=SAM9289-ND) which is also from Digi-Key.

![Image of 6 pin Extender](https://media.digikey.com/Photos/Samtec%20Photos/ESQ-103-14-G-D_sml.JPG)
## TempSensor Design Files

## TempSensor Assembly
Once the PCB has been recived its time to solder everything together.

First solder the 4 vias on the board. The vias are circled in red.

The top![image of top](https://github.com/cblakley/TempSensor/blob/master/images/via_top.jpg?raw=true)

The bottom![image of bottom](https://github.com/cblakley/TempSensor/blob/master/images/via_bottom.jpg?raw=true)

Then solder the 4 pin header to the PCB![image of 4 pin](https://github.com/cblakley/TempSensor/blob/master/images/4_pin.jpg?raw=true) Solder the 4 pins from the bottom only.

And finally solder the 6 pin I/O extender.![image of 6 pin](https://github.com/cblakley/TempSensor/blob/master/images/6_pin.jpg?raw=true) Only pins 4,6 and 3,5 need to be soldered. The 6 pin extender should be soldered from the top only.
## Raspberry Pi Setup
If your raspberry pi still need to be set up, I'd recommend this guide to set up using NOOBS[https://www.raspberrypi.org/help/noobs-setup/2/] 
->Once the OS is installed, enable I2C by going to preferences->

## PCB Power up
After soldering its time to attach the PCB to the Raspberry Pi. The 6 pin header plugs into the Pi's GPIO header. 

To check if the Pi can detect the AM2135 sensor open a terminal window and run the command "i2c detect -y1". You'll need to run the command twice in quick succession as the sensor will be in a sleep mode. ![https://github.com/cblakley/TempSensor/blob/master/images/i2cdetect.png?raw=true] 


