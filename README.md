# SCO2
The SCO2 is a small scale personal initiative to create CO2 sensors for the school my kids go to. Goal is to make the sensor:
 - Easy to use for teachers and kids
 - Show details for those interested
 - Looks good draw attention when needed
 - Solid to survice the harse school environment
 - Decent but relatively cheap to build
 
# First Version
The first version is a completely home made device using some electronics, a soldering iron and a 3D printer. 

## Components Used
The following components are used to build the sensor:
 - Wemos D1 Mini ESP board (this is the computer) https://www.wemos.cc/en/latest/d1/d1_mini.html
 - Sensirion SCD30 (This is the CO2 / Temp / Humidity sensor) https://www.sensirion.com/en/environmental-sensors/carbon-dioxide-sensors/carbon-dioxide-sensors-co2/
 - Wemos TGB Led Shield (to coler indicate air quality) https://www.wemos.cc/en/latest/d1_mini_shield/rgb_led.html
 - Some wires, shrinking tube and screws

## Software used
I started out programming the thing myself in Visual code, that gives me great abilities but also is quite cumberstone since I'm not a programmer by trade. So I swtched to ESPhome (https://esphome.io/). ESP Home abstracts the actual programming for you and all you need is a configuration file to tell the system what to compile for you. It can be ran alone or integrated into Home Assistant if you want an easy and comprehansive overview of all the sensors in for example your school. 

To be clear, the device can run alone without wifi of back-end, but when you're up for it you can connect it and save the data in various systems. 



