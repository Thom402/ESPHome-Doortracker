# ToFDoorEntryTracker

A ESPHome project designed to count people passing through a doorway using two Time-of-Flight (ToF) sensors mounted on a door frame.

## ESPHome CLI sheet

### update esp home
>
> pip3 install esphome -U
>

### configure yaml file in root directory and than compile file to generate firmware
>
> esphome compile thomas-room-door-tof.yaml
>

### install the firmware to the device

on first install you have to manual flash the binary file:  
>
>.esphome\build\exampleProject\.pioenvs\exampleProject\firmware.bin
>

to the connected esp device

## update firmware
>
1. > esphome compile thomas-room-door-tof.yaml
2. > esphome upload thomas-room-door-tof.yaml
>

or

>
1. > esphome run thomas-room-door-tof.yaml
>
---

## secrets

configure secrets in `secrets.yaml` file and bind the properties to the ``thomas-room-door-tof.yaml`` file

To Bind to the root secrets file you can add another secrets.yaml in the device folder and paste this into the file:
>
> <<: !include ../secrets.yaml
>

1. configure secret in `secrets.yaml` file
   >
   > property: "myRealProperty"
   >
2. configure secret in `thomas-room-door-tof.yaml` file
   >
   > property: !secret propety
   >