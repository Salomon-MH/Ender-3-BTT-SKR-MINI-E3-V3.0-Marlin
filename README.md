# Ender 3 Marlin w/ BIGTREETECH SKR MINI E3 V3.0 board
My hardware configuration

	- Creality Ender 3
	- BIGTREETECH SKR MINI E3 V3.0 replacement board (originally came with Creality 1.1.4 board)
	- 3D Touch sensor ("3DSWAY" clone) with printed [Adjustable BL-Touch sensor mount](https://www.thingiverse.com/thing:3148733)
	- Original Creality Ender 3 metal extruder upgrade
	- Ball bearing filament spool holder upgrade
	- Regular 0.4mm brass nozzle

Currently not using a connected raspberry pi or similar board.

## Connections
Most stuff is just connected equal to how it was with the 1.1.4 board, except for where polarities is switched when comparing the boards (careful!) and another connector being used for one fan (soldered a new connector to the wire).

3D Touch sensor is currently connected to the 5pin port.

## Troubleshooting

For troubleshooting, uncomment

	#define PINS_DEBUGGING

in the `Configuration_adv.h` file. When to e.g. check the BL-Touch connection you can try sending the command

	M43 S

e.g. via Pronterface. For me it returns:

	>>> M43 S
	SENDING:M43 S
	Servo probe test
	. using index:  0, deploy angle: 10, stow angle:   90
	. Probe Z_MIN_PROBE_PIN: 46
	. Z_MIN_PROBE_ENDSTOP_INVERTING: false
	. Check for BLTOUCH
	= BLTouch Classic 1.2, 1.3, Smart 1.0, 2.0, 2.2, 3.0, 3.1 detected.
	** Please trigger probe within 30 sec **
	. Pulse width (+/- 4ms): 8
	= BLTouch pre V3.1 (or compatible) detected.

