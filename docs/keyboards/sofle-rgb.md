# Sofle RGB 

Available at: https://keyhive.xyz/shop/sofle

## Instructions

1. Solder
   - [diodes](#solder-diodes)
   - [underglow LEDs](#solder-underglow-leds)
   - [per-key RGB LEDs](#solder-per-key-rgb-leds)
   - [hot swap sockets](#solder-hot-swap-sockets)
1. [Flash controller](#flash-controller)
1. [Solder controller](#solder-controller)
1. [Solder the reset button](#Solder-reset-button)
1. [Test the keyboard](#test-the-keyboard)
1. [Solder OLEDs](#solder-oleds)
1. [Solder TRRS jacks](#solder-trrs-jacks)
1. Break PCBs from scaffold
1. [Solder encoders](#solder-encoders)
1. [Install OLED cover](#install-oled-cover)
1. [Install switches](#install-switches)
1. [Install encoder knobs](#install-encoder-knobs)

## Solder diodes

Soldering diodes is relatively straightforward. Refer to [Soldering diodes](../basic/soldering-diodes.md) if you need further guidance.

![](../images/sofle-rgb/diodes.gif)

## Solder underglow LEDs

> ⚠︎ LEDs can be very temperature sensitive. Be _very careful_. Consider setting your soldering to a low temp (about 200 C), using a fine tip, adding flux, and/or using a hot air station.

This is the LED order:

![](../images/sofle-rgb/LED_order%5B1%5D.png)


- Tin all the pads with a small bubble of solder, not too much.
- Orient the notched corner of the pixel with the line with the right angle shown on the silkscreen.
- Place the 5050 LED on top and center. 
- With some light pressure, hold the led in place while you flow the solder bubbles.
   - I use an aluminum screwdriver which also acts as a heat sink to protect the LED from burning out.
- Test each LED as you go.

![](../images/sofle-rgb/underglow-leds.gif)

### Alternate method

If you have the appropriate tools, especially liquid flux or preferably flux paste, the following drag-soldering-like method may result in more consistent joints.

- Flux the pads, then apply heat to activate the flux to clean the pads.
- Apply a generous amount of flux to the pads.
- Place the 5050 LED on top and center.
- Activate the flux again, making sure the flux drowns the contacts on both ends, but don't boil it all off.
- Transfer a tiny ball of solder to the iron tip. If it is resistant to transfer, remember to clean it with flux and iron sponge.
- Using e.g. tweezers to hold the LED in place with the other hand, transfer the solder to the joint. The solder should be eager to wet the contacts.

You can do this for the per-key RGB LEDs as well; as for the other components, this may be unnecessary and flux-core solder might suffice. Before testing, don't forget to thoroughly clean the board to remove any flux residue that might short pins, especially with the per-key RGB LEDs. I used 99% isopropyl alcohol and a toothbrush. For the per-key RGB LEDs, the cutout will be drenched in flux after this procedure, so consider cleaning it.

## Solder per-key RGB LEDs

> ⚠︎ LEDs can be very temperature sensitive, however this variant with the tabs are much easier to use and less prone to burning out. Still, take care to not allow too much heat to transfer.

- Tin one pad with a small amount of solder. 
- Place the LED into the cutout, orienting the notched tab with the line with the right angle on the silkscreen.
- Hold the LED in place with tweezers, and flow the solder under the tab. 
- Let cool and solidify. 
- Apply a tiny bit of solder to the remaining tabs. 
- Test each LED as you go.

![](../images/sofle-rgb/ez-leds.gif)

## Solder Kailh hot swap sockets

Refer to [Soldering Kailh hot swap sockets](../basic/soldering-kailh-hot-swap-sockets.md) if you need further guidance.

![](../images/sofle-rgb/sockets.gif)

## Flash controller

Flash the controller (pro micro, Elite C, nice!nano, etc) with the firmware. This ensures that the controller works completely **before** soldering it permanently to the board.

[TODO: Add link to firmware files](#todo)

## Solder controller

Refer to [Soldering the controller](../basic/soldering-the-controller.md) if you need further guidance.

![](../images/sofle-rgb/controller.gif)

## Solder reset button

Insert or align to holes. Solder in place.

![](../images/sofle-rgb/reset-button.gif)

## Test the keyboard

At this point it should function as a keyboard. When you plug it in, the on-board LEDs should turn on. Insert a switch into a hot swap socket and [test that a keycode is pressed](https://www.keyboardtester.com/tester.html). You might consider testing every key in case there are problems with the diodes or hot swap sockets.

After this, solder remaining components.

## Solder OLEDs

> If you've socketed the controller, also consider socketing the OLEDs else the controller will be trapped underneath it.

Insert headers into holes. Use electrical tape to secure in place while you solder the holes on the bottom side of the PCB.

![](../images/sofle-rgb/oleds.gif)

> ⚠︎ The OLED is not required but **if you omit it, you must disable it in the firmware**. If you do not, you will experience "jittery" keystrokes as if some keys were lost while in transit. Disabling it in the firmware will fix this behavior.

## Solder TRRS jacks

Insert into holes. Solder in place on the bottom side of the pcb.

![](../images/sofle-rgb/trrs-jack.gif)

## Solder encoders

- Insert encoder into place.
   - If pins are bent, realign them with tweezers.
- Flip pcb over.
- Using pliers, bend the larger tabs so that they "hold" to the pcb
   - Tighter is better but is not critical, as long as it stays in place long enough to solder the pins.
   - These tabs **do not** need to be soldered.
- Solder the 5 encoder pins in place.
- Optional: clip the excess pin length.

![](../images/sofle-rgb/encoder.jpg)

## Install OLED cover

- Remove any protective paper from the acrylic cover.
- Locate the four (4) spacers that are slightly longer than the rest.
- Install the spacers into the holes just below the controller and screw from the bottom.
- Remove any protective plastic from the OLED screen.
- Align the OLED cover with the standoffs and screw into place from the top.

## Install switches

- Install the standoffs onto the bottom side of the switch plates.
- Insert switches into the plate.
   - Begin by placing one on each of the corners of the PCB to give you some stability. Basically anywhere where they'll stay in place to help align the rest.
   - Be cautious of bent pins when pushing the switch down.
- Insert remaining switches.
- Turn over and screw bottom plate into place.

If the switches are too loose in the plate and keeps slipping down while pushing downward to add other switches, try this instead:

- install the standoffs onto the plate.
- lay the plate over top of the pcb and hold in hand, flattened together.
- insert the switches into the pcb (while not worrying about making sure they're secured into the plate).
- once all the switches are in place, put it down on hard flat surface with the standoffs holding everything up
- Slowly and firmly push down on all the whole set of until they all "click into" the plate.

## Install encoder knobs

Install the encoder knobs. Some are simply pressed onto the shaft, others fit loosely and require using a small hex wrench to secure with a set screw.
