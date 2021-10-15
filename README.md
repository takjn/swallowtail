# Swallowtail
A split keyboard with 5x6 column staggered keys.

![PXL_20210722_140038590](https://user-images.githubusercontent.com/7824306/128621548-49993a87-159e-4027-90ae-6c0eacff5b42.jpg)

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

![PXL_20210722_074656557](https://user-images.githubusercontent.com/7824306/128621618-ca94c453-dc8c-4e85-8de5-8b15a13d2023.jpg)

### Soldering
All parts have a position and orientation. See the photo to make sure it is placed correctly before soldering.

Maybe a good idea to use masking tape to hold parts before soldering.

#### Bridge jumpers
The PCB is reversible. Use one board for the left and the other for the right.
Bridge five jumpers on each board. One should be "Left" and the other should be "Right".

![PXL_20210712_115354749](https://user-images.githubusercontent.com/7824306/128621678-3dbf3265-fb9a-4d68-b3c0-6977d59effbf.jpg)
![PXL_20210712_131139684](https://user-images.githubusercontent.com/7824306/128621659-200fb01c-d1ce-44f1-ba66-789389cfbd0b.jpg)

#### Diode
Place diodes on the back side of the pcb. This is the same side on which you jumpered. Make sure the diode orientation is correct. All diodes orientation must be the same on a pcb.

![PXL_20210712_125730064](https://user-images.githubusercontent.com/7824306/128621693-8c088ae0-acd4-4b40-a282-c6cebb645733.jpg)
![PXL_20210712_120906744](https://user-images.githubusercontent.com/7824306/128621694-d8aff204-80f5-4a16-923f-9da99d8af35b.jpg)
![PXL_20210712_121046019](https://user-images.githubusercontent.com/7824306/128621698-7f7d97d0-ed8f-42bf-bc98-7a37e0ce122c.jpg)
![PXL_20210712_121323080](https://user-images.githubusercontent.com/7824306/128621702-e103f458-f083-4808-b376-5e953e79e655.jpg)
![PXL_20210712_132515537](https://user-images.githubusercontent.com/7824306/128621710-ee4c8333-db9e-4eca-a7cb-068b46c5e2f0.jpg)

#### Reset switch and TRRS jack
Solder a reset switch and TRRS jack on the **front** side of the pcb.

![PXL_20210712_141435243](https://user-images.githubusercontent.com/7824306/128621715-54061e05-5fa0-4aa6-bca8-0cc57dbb1727.jpg)
![PXL_20210712_142053217](https://user-images.githubusercontent.com/7824306/128621718-44cd3266-c909-4e77-85ed-42c03f34cda6.jpg)

#### Pro micro
Insert pin headers from the surface on which parts are mounted. Solder it from the **blank** side of the Pro micro.

Insert a Pro micro into the place on the PCB. If you are using spring loaded pin headers, you don't need to solder it on the PCB so that you can remove Pro micro later easily. If you don't, solder it and cut pins a little not to conflict with the cover plate.

#### Test
Before moving to the next step, test the pcb once. Flash a firmware to the Pro micro. Then, make short-circuit on each keyswitch pads. You will see some characters in your computer.

#### Kailh PCB Socket
Place a PCB socket on the back side of pcb. Make sure the position is correct.

![PXL_20210712_133130883](https://user-images.githubusercontent.com/7824306/128621724-36bb17aa-224d-4a2c-916f-6d3dbb2295bd.jpg)
![PXL_20210712_134213587](https://user-images.githubusercontent.com/7824306/128621731-f832238d-c43e-47bf-962a-e2bf7838a4e7.jpg)

#### OLED (optional)
Place a pin socket on the **front** side and solder it. Then solder a pin header on a OLED.

#### Back light (optional)
See a LED. You will see one of pins' corner is cut. The pin should be placed on the bottom-left in where a "L" shape silk is printed.

![PXL_20210714_134036294](https://user-images.githubusercontent.com/7824306/128621738-161f2429-2089-4840-a511-dfe1f9f3dae6.jpg)

LED can be broken easily by heat. Be careful not to take too long time to solder. I usually solder only one pin at once and go to the next LED. After all LEDs in a row is fixed, back to the first LED to solder the second pin and repeat the process. This will be good not to heat too much on a LED.

### Assemble
Screw top plate spacers. 3mm female-to-male spacer should be on the front side. Attach a PCB and fix the PCB with a 3mm female-to-female spacer from the back side.

![PXL_20210722_105505860](https://user-images.githubusercontent.com/7824306/128621751-dbbbb3e8-cf5d-474b-adb8-a1956fcf04dc.jpg)
![PXL_20210722_105544187](https://user-images.githubusercontent.com/7824306/128621781-25b90be9-557c-4b5f-9715-6888684e6630.jpg)
![PXL_20210722_105746206](https://user-images.githubusercontent.com/7824306/128621783-bacdb194-9853-4b9d-9142-e410acdef622.jpg)

Screw OLED spacers. Each 8mm female-to-female spacer should be on the front side. Fix the spacer with a 3mm female-to-male spacer from the back side.

![PXL_20210722_110209773](https://user-images.githubusercontent.com/7824306/128621793-91dee4c6-91a8-4202-8f63-209feb61cc46.jpg)

Put the bottom plate and OLED protection plate too.

![PXL_20210722_110312921](https://user-images.githubusercontent.com/7824306/128621826-e7f3364e-a99b-4f9d-bfee-6e5a1ca8f767.jpg)
![PXL_20210722_111859473](https://user-images.githubusercontent.com/7824306/128621828-63bf9303-e31e-4268-bb51-a6dddf6926a0.jpg)

Plug key switches on the top plate. Make sure all pins are straight before insert. 

![PXL_20210722_113817315](https://user-images.githubusercontent.com/7824306/128621845-0ac307b4-8aca-4eb9-8e40-9a580c033fde.jpg)

## Firmware
You can use a compiled firmware in the firmware directory. Go to [Pro Micro Web Updater](https://sekigon-gonnoc.github.io/promicro-web-updater/index.html) and flash the hex file in the firmware directory.

The firmware supports VIA. You can customize key bindings easily without compile. Go to [Remap](https://remap-keys.app/) and use info.json in the firmware directory as a definition file.

Swallowtail uses QMK firmware. If you want to customize the firmware, see [swallowtail branch in takjn/qmk_firmware](https://github.com/takjn/qmk_firmware/tree/swallowtail/keyboards/swallowtail).

## License
Licensed under the MIT License.

## Dependencies
This PCB uses [foostan/kbd](https://github.com/foostan/kbd) library.
