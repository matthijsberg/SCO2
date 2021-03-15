# SCO2
The SCO2 is a small scale personal initiative to create CO2 sensors for the school my kids go to. Goal is to make the sensor:
 - Easy to use for teachers and kids
 - Show details for those interested
 - Looks good draws attention when needed
 - Solid to survive the harse school environment
 - Decent but relatively cheap to build
 
# First Version
The first version is a completely home made device using some electronics, a soldering iron and a 3D printer (or an online 3D ordering service). 

## Components Used
The following components are used to build the sensor:
 - Wemos D1 Mini ESP board (this is the computer) https://www.wemos.cc/en/latest/d1/d1_mini.html
 - Sensirion SCD30 (This is the CO2 / Temp / Humidity sensor) https://www.sensirion.com/en/environmental-sensors/carbon-dioxide-sensors/carbon-dioxide-sensors-co2/
 - Wemos TGB Led Shield (to coler indicate air quality) https://www.wemos.cc/en/latest/d1_mini_shield/rgb_led.html
 - Some wires, shrinking tube and screws
 - 3D model exisiting out of 5 parts to put the sensor together. I fiddled around a bit with the tollorances to make the parts fit together nicely, so you might need to do so too. 

## Software used
I started out programming the thing myself in Visual code, that gives me great abilities but also is quite cumberstone since I'm not a programmer by trade. So I swtched to ESPhome (https://esphome.io/). ESP Home abstracts the actual programming for you and all you need is a configuration file to tell the system what to compile for you. It can be ran alone or integrated into Home Assistant if you want an easy and comprehansive overview of all the sensors in for example your school. 

To be clear, the device can run alone without wifi of back-end, but when you're up for it you can connect it and save the data in various systems. 

# 3D Files
The device exists out of 5 3D printer parts you can print on your own printer of via a service. You find the here, and assambling should be possible in one way only. :)

# Hardware assambly
Maybe i'll create a visual guide one day, but for now:


# Software Installation
When you have all the parts in house en printed the enclosure make sure you have ESPHome running. For me it's part of my Home Assistant installation and for the school I build this for I have a Raspberry PI where I run HASSOS with ESP Home in. To get HASSIO running, please find the software and instructions here: https://www.home-assistant.io/installation/ . 

When you have ESPHome running as a Add-on:
 - Open the ESPHome interface
 - Connect the Device with a USB cable to your HA device
 - Open the "Secrets" File in the rop right corner to enter your passwords you will use (example in this github calles secrets.yaml)
 - Create a new device, give it the right name straight away, but the rest of the information can be bogus IF you are using exactly the same ESP board
 - Now change the interface to upload the code to your device from over the air to the USB port (you can use OtA after inital flash)
 - Once created open the config by clicking "Edit" and past the example config from the repo into you config (sensor.yaml).
 - check if all the password and config options are correct and upload the file with "Upload"
 - See what happens. 
 - You can add the sensors to HA if you want under Integrations or under Device. 

Cheers! Drop me comments or improvents here in GitHub please. 
