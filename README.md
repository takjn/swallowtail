# Swallowtail
A split keyboard with 5x6 column staggered keys.

## Parts List
### Required

|Name |Number |Notes |
|--- |--- |--- |
|PCB | 2 | This PCB is reversible. One is for left and the other is for right. You can use a gerber file in `pcb/plot` directory to order your one. |
|Top plate, bottom plate, OLED protection plate | 2 sets | You can see the svg file in `plate` directory. This is designed for 2mm acrylic plate. If you create your plate with another thickness or material, you may need to change spacer height and screw length. |
|3mm female-to-female spacer | 12 |https://www.aliexpress.com/item/33033691154.html |
|3mm female-to-male spacer | 16 |https://www.aliexpress.com/item/33033691154.html |
|8mm female-to-female spacer | 4 |https://www.aliexpress.com/item/33033691154.html |
|M2 3mm screw | 32 | |
|Diode 1N4148 | 60 | |
|Kailh PCB Socket | 60 | |
|2 pin Tactile switch | 2 | For reset switch |
|3.5mm TRRS jack | 2 | |
|Adhesive Rubber Cushions | 8 | |
|Pro micro | 2 | |
|Cherry MX switch (5 pin) | 60 | |
|Keycaps | 60 | 58 1u keycaps and 2 1.5u (or up to 2.25u) keycaps|
|TRS (3 pole) audio cable | 1 | |
|Micro USB Cable | 1 | |

### Options
#### Spring loaded pin headers
Highly recommend for beginners. Some shop sell it with a Pro micro.
|Name |Number |Notes |
|--- |--- |--- |
|Spring loaded 12-pin header (a.k.a. Conthrough) | 4 |https://talpkeyboard.net/items/5e056626d790db16e2889233  |

#### OLED
Just a decorative parts.
|Name |Number |Notes |
|--- |--- |--- |
|SSD1306 OLED module | 2 | |
|4 pin low profile socket (low profile)| 2 | |
|4 pin low profile header (low profile)| 2 | |

#### Back light
A led places in bottom (south) side of keycap. Transparent key switch is recommended.
|Name |Number |Notes |
|--- |--- |--- |
|SK6812MINI-E | 60 | |

## Build Instructions

### Preparation
#### QMK firmware
Swallowtail uses QMK firmware. See firmware section and flush a firmware to Pro micro in advance.

#### Pro micro
Pro micro USB connector is fragile. You can reinforce the connector with epoxy resin adhesive. Put a small amount of epoxy resin around the connector. Be careful not to flow it into the connector. Leave it until fixed.

### Soldering
All parts have a position and orientation. See the photo to make sure it is placed correctly before soldering.

Maybe a good idea to use masking tape to hold parts before soldering.

#### Bridge jumpers
The PCB is reversible. Use one board for the left and the other for the right.
Bridge five jumpers on each board. One should be "Left" and the other should be "Right".

#### Diode
Place diodes on the back side of the pcb. This is the same side on which you jumpered. Make sure the diode orientation is correct. All diodes orientation must be the same on a pcb.

#### Reset switch and TRRS jack
Solder a reset switch and TRRS jack on the **front** side of the pcb.

#### Pro micro
Insert pin headers from the surface on which parts are mounted. Solder it from the **blank** side of the board.

Insert a Pro micro into the place. If you are using spring loaded pin headers, you don't need to solder it. If you don't, solder it and cut pins a little not to conflict with the cover plate.

#### Test
Before moving to the next step, test the pcb once. Flash a firmware to the Pro micro. Then, make short-circuit on each keyswitch pads. You will see some characters in your computer.

#### Kailh PCB Socket
Place a PCB socket on the back side of pcb. Make sure the position is correct.

#### OLED (optional)
Place a pin socket on the **front** side and solder it. Then solder a pin header on a OLED.

#### Back light (optional)
See a LED. You will see one of pins' corner is cut. The pin should be placed on the bottom-left in where a "L" shape silk is printed.

LED can be broken easily by heat. Be careful not to take too long time to solder. I usually solder only one pin at once and go to the next LED. After all LEDs in a row is fixed, back to the first LED to solder the second pin and repeat the process. This will be good not to heat too much on a LED.

### Assemble
Screw top plate spacers. Each 3mm female-to-male spacer should be on the front side. Fix the spacer with a 3mm female-to-female spacer from the back side.

Screw OLED spacers. Each 8mm female-to-female spacer should be on the front side. Fix the spacer with a 3mm female-to-male spacer from the back side.

Plug key switches on the top plate. Make sure all pins are straight. Attatch the plate with keys to the PCB and fix with M2 screws. Then, put on the bottom plate and OLED protection plate too.

## Firmware
Swallowtail uses QMK firmware. If you want to customize the firmware, see the document and set up QMK.

You can use a compiled firmware. The firmware supports VIA. You can customize key bindings easily without compile.

## License
Licensed under the MIT License.

## Dependencies
This PCB uses [foostan/kbd](https://github.com/foostan/kbd) library.
