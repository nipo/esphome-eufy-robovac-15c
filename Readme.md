# Eufy Robovac 15C ESPHome controller

This repo contains an Eufy Robovac 15C communication MCU
implementation using [esphome](https://esphome.io).  Purpose is to
remove dependency on cloud platform to control a local device.

This Robovac model, like many (all?) others, uses two MCUs, one for
actual implementation of the vacuum function and another for Wi-Fi
control.  Communication between the two MCUs is using a Tuya-defined
protocol format.  Protocol is natively supported by ESPHome.  Mapping
of "Datapoints" exchanged over this protocol is propietary.  This is
what is defined in this configuration file.

Starting point was
[sibling project](https://github.com/Rjevski/esphome-eufy-robovac-g10-hybrid)
for G10.  Data mapping of C15 is not exactly the same but was found
back using the IR remote control.

# Compiling

You need a `secrets.yaml` file in the current working directory with the
following entries:

* wifi_ssid
* wifi_psk
* wifi_ap_psk

# Programming

There is an unpopulated header on the Wi-Fi module of the 15C where
all useful pins for programming are broken out.  Pins are identified
on silkscreen of the PCB.

# License

MIT
