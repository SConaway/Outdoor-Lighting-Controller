# Outdoor-Lighting-Controller

## Description

This is the hardware (PCB) and the software (ESPHome configuration) for a Home Assistant-based motion-lights controller. ESPHome is used to interface with Home Assistant, which is responsible for controlling the lights and motion alerts, etc.

## Instructions

1. Download the board files from GitHub releases.
2. Have the PCB fabricated.
    1. I used [JLCPCB](jlcpcb.com); it cost $2 (+ shipping) for 5 boards.
3. Order the needed parts ([parts list below](#parts-list)).
4. Assemble all parts on the PCB.
5. [Install ESPHome](https://esphome.io/guides/getting_started_command_line.html#getting-started-with-esphome).
6. Create the secrets file from the template.
7. Connect the ESP01 to the programming adapter.
8. Run `esphome lights.yaml compile` to compile the firmware.
9. Run `esphome lights.yaml upload` to upload the newly-compiled firmware.
10. Place the ESP01 in the PCB, paying attention to the direction of where it points

## Parts List

_Coming Soon!_

## Notes

-   The ESP01 needs a 5K ohm resistor (I used a 5.2K ohm resistor I had lying around) soldered between CH_EN and VCC to operate. This will be fixed in a later board revision.
-   If ESPHome is not working properly, you can upload the binary in the Release using another uploading tool, such as `esptool`.

## Credits

-   [esphome](esphome.io)
-   [Home Assistant](home-assistant.io)
-   [Sparkfun's EAGLE libraries](https://github.com/sparkfun/SparkFun-Eagle-Libraries)
