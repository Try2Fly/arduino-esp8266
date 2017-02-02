# CeilingFanController

This device provides an interface for controlling Hampton Bay
ceiling fans.  Since I could not find a transitter/receiver
at the right freqency, its built from an purchased remote
with the esp "pushing" the buttons on the remote by using
transistors to drive the buttons high or low.

# Configuration

The following constants can be adjusted to fit your build
and configuration:

* Basic as part of ino file:
  * FAN_TOPIC - the topic on which the device listens
    for messages.  Messages are in the form of XXXX,command
    where XXXX is one of 0000 through 1111 to correspond to 
    the code selected for the fan, and command is one of
    high, med, low or off.

* Wifi configuration, from WirelessConfig.h:
  * ssid - The id of the wireless network to connect to.
  * pass - the password for the wireless network.
  * mqttServer - array with the IPV4 components for the mqtt
    server.

# Building

To build you need to add the following:

* [Arduino ESP library](https://github.com/esp8266/Arduino)
* [PubSubClient](https://github.com/knolleary/pubsubclient)

libraries as libraries in your Arduino IDE.

Once these are installed, you can then add your device and
Wifi configuration files and the compile and flash your esp8266.

# Schematic

The following is the schematic for the sensor hardware that I
used:

![schematic]()

# Pictures

The following are a few pictures of my build:

![picture1]()
![picture2]()

# Main Components

* [NodeMCU D1](http://www.ebay.com/itm/NodeMCU-Lua-ESP-12-WeMos-D1-Mini-WIFI-4M-Bytes-Development-Board-Module-ESP8266-/321989574625)
* [Remote Control]()