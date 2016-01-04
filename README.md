# FabLab EAGLE workshop (INTRODUCTORY)
The official repo for the Munich Fablab EAGLE introductory course 

![https://raw.githubusercontent.com/chrisvoncsefalvay/fablab-eagle-workshop-INT/master/top.png]

## The board
The board used to demonstrate EAGLE's functionality is a small ATtiny based brake light tester. The general idea is as follows. Upon resetting the device, an ambient light measurement is taken for five seconds. At the end of the five seconds, you must have attached the device to your light. The device then enters measurement mode. The LED will light up red and turn green if and only if the brake light has lit up. After 60 seconds of no signal, the device will enter sleep. 

### Specs
The device must accommodate the ATtiny, an I2C based light sensor, a battery, a tricolour LED, a power management circuit and all else that's needed for the board's functioning.

The board is driven by three 3V CR927 batteries in series, yielding 9V. This is converted to 5V by the LDO (U2).

Most of the heavy lifting is done by the MCU. The MCU has to be programmable through ICSP headers, though these will not necessarily be mounted in production devices (potentially replaced by a pogo/bed of nails approach).

### Implementation

![https://raw.githubusercontent.com/chrisvoncsefalvay/fablab-eagle-workshop-INT/master/schematic.png]

This is a possible implementation, but not the only possible implementation. Be creative, use your mind.

### Board design considerations
The usual considerations apply, but don't forget to
- leave enough space,
- provide fiducials and mount holes,
- use largeish components (1206/1210) and large pads for hand soldering ('W pads') where available,
- stick to two layers, and
- avoid the autorouter.
