# PhotonOnAStick
Particle Photon Prototyping board on a USB Stick

## Currently untested (11 July 2015). PCBs ordered for testing.

## Use Case

* Prototype post breadboard. 
* Connection of sensors, LEDs, SparkFun style breakout boards etc.
* Deployed Thing on a Stick where the Photon may be used to make an internet connected sensor for a room, or lighting or ??? and can be plugged into a USB wall adaptor.
* Using readily available wall plugs board may be connected:
** with the board vertical, Photon facing outwards flat to the wall.
** with the board horizontal, Photon facing upwards. 
* These options makes for a nice option for uplighting (internet controlled nightlight?), or a room sensor.
* Other power adaptors exist, e.g. USB in a multi-gang outlet.

## Usage

* USB powered by plugging into a USB A socket on a USB Wall Adaptor, or A -> Micro B on the Particle Photon. Do not connect both at once.
* Top layer is mainly for 0805 devices (and through hole).
* Bottom layer is for 1206 devices (and through hole).

## Botton (looking at the baord with USB connector to the left)
* A0-A7 Analog signals come out to the option of a round test point (solder connection) via an 0805. Can be resistor, 0 ohm link or ....
* A0-A7 Analog signals also come out to a 1206 package with the other side unconnected so this can have a wire tacked on as needed.
** This arrangement may be used to provide either imput impedance/capacitance filter to the analog signal, 
** or by connecting the unterminated end to GND or 3V3 this can provice half of a potential divider for a sensor - the sensor may be providing the other half.
* +5V, Gnd, Tx and Rx come out to a 1206 only. Allows for a resitor and/or wire tacking.

## Center
* Top layer in the middle is a SO16 package outline, can be used for SO8 or anything that would fit. Pins 1-8 go to connectors by the USB port, 9-16 by the bottom of the Photon.
* Top 2 connectors in the middle of the Photon have +5V, +3V3 and Gnd available.

## Top (looking at the baord with USB connector to the left)
* 3v3, VBat and Gnd brought out to 4 pin connector. Pin 2 unconnected (may be used for polarity).
* D0-D7 connected to 1206 package on bottom layer with other end unconnected available for wire.
* D0-D7 on top layer go to 0805 package which is liked to a second 0805 with the far end connected to ground.
** This arrangement allows D0-D7 to be connected to a (0805) LED then a (0805)current limiting resitor on the top layer
** or to provide a pull down where the input is connected to the middle of the pins 0805 packages.

## Prototyping area (Right hand side looking at the baord with USB connector to the left).
* Top rail is 3v3 from the Photon (3)
* Second rail down is GND (G)
* Bottom rail is +5V (5)
* 3V3 and GND have a 0805 connection for a capacitor.
* Each pair of rows have possible connection for 0805 and 1206 device near the Photon to allow for capacitor, resistor or LED.
* Only power rails are connected hole to hole.
* 8 1206 or 8 * 2 0805s are available on the right, again for LEDs, Sensors, Resistors or Capacitors. 
** The 2x 0805 combination allows for a LED + resistor. Either side of the 1206 or 0805 pair are connected to the pins to the outside of them.

## Spark Photon
* This board is designed for the Particle Photon. It does need headers though.
* The Particle Core (Spark Core) may also be used.

## Eagle Libraries Used:

Particle Photon Library: https://github.com/spark/photon/tree/master/libraries
SparkFun: https://github.com/sparkfun/SparkFun-Eagle-Libraries


## Versioning

* Board will have multiple major versions. e.g.
** V1 A0-A8 1206/0805's unterminated.
** V1.x bug fixes for V1 board.

** V2 A0-A8 1206/0805's terminated with +5 or GND based on layer
** V2.x bug fixes for V2 board.


## Ideas

### Different versions

* Change A0-A8 1206 packages so unconnected end is connected to 
* Much narrower (just room for Photon)
* Wonly - USB port at Top Right corner to allow for top exit wall adaptors where USB socket is perpendicular to the wall.
* Surface mount photon

* Timer version. LED/LCD/OLED dispay. Sensor to allow for setting and starting of timer (Hands free)

## Bugs

* Missing Open Hardware Logo.