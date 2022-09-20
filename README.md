# Marvelous65 Split (Forked from karnadii)

All the credit goes to [karnadii](https://github.com/karnadii/marvelous65). This repo is primarily for my documentation purposes, and as a guide for anyone that would like to build this but might be as inexperienced as I was when I attempted building this.

Shoutout to karnadii, Nicell and the other zmk and nice!nano discord folks that helped me get as far as I did.

## Differences from karnadii's original

I'm running nice!nano on my build instead of nrfmicro. So far, there's barely any difference other than building the firmware.

## 1. Ordering your PCB

Much like his original repo - you'll have to order these PCBs off of a site like JLCPCB (reach out to me as I might have a few extras lying around). 

You can upload the Gerbers I included to JLCPCB (`Hardware/Gerbers/Gerbers.zip`) or generate them yourself from the Kicad project file.

Options I chose, many of them are default, but I'm including them here for anyone that might find it useful:
- Base material: FR-4
- Layers: 2
- Dimensions: 345.28 * 107.17 (this should be default)
- Panel Qty: 5 (this is the minimum)
- Product Type: Industrial/Consumer electronics
- Different design: 2 
  - This defaults to 1 but it's 2 as they're two separate boards
- Delivery Format: Panel by Customer
- PCB Thickness: 1.6
- PCB Color: Hey, you do you
- Silkscreen: White
- Silkscreen Technology: Ink-jet/Screen Printing Silkscreen
- Sufrace Finish: LeadFree HASL
- Outer Copper Weight: 1 oz
- Gold Fingers: No
- Confirm Production file: Yes
- Flying Probe Test: Fully Test
- Castellated Holes: No
- Remove Order Number: No

### PCB Assembly options

- PCBA Type: Standard
- Assembly Side: Both Sides 
  - I believe you only need the Bottom, but I opted not to risk it during my first build
- PCBA Qty: 5
- Edge Rails/Fiducials: Added by JLCPCB
- Confirm Parts Placement: Yes

After this, you'll need to upload a BOM file and a CPL file. These are `Marvelous65 Split-bom.csv` and `Marvelous65 Split-all-pos.csv` respectively.

You might have to confirm/review the parts. I've noticed that the LED (WS2812B) and the 3.5mm audio jack (PJ-320D) tends to fail to match. Do a search for it and select the appropriate one.

Double check your PCB, I had to rotate the headphone jack to be vertical.

Boom - you're good to go. Pay the good folks and while you're waiting impatiently for your PCBs, get ready to do more shopping.

## 2. Other things you're going to need

I'm assuming you already have a soldering kit etc. Note that while I'll link to the shop pages I bought from - there are no affiliate links whatsoever and I have **no** relationships with these stores. Feel free to shop around and get what serves you best.

For this keyboard specifically, you'll need at least:
- 2x [nice!nano v2s](https://typeractive.xyz/products/nice-nano)
- 2x Lithium batteries
  - You can go big(ger) and grab the [750mAh](https://typeractive.xyz/products/lithium-battery-750mah) batteries or the slimmer [110mAh](https://typeractive.xyz/products/lithium-battery-110mah) versions. 
  - I've heard tell that you can tuck the 110mAh batteries under the nice!nano itself, which might be nice if you're looking for a neat, compact internal
  - I opted for ones with JST sockets
- 2x [Machine sockets and pins](https://typeractive.xyz/products/nice-nano)
  - Technically a nice-to-have but this saved me from a screwup, and it's helpful to be able to unplug the board for troubleshooting
- 2x 128x32 OLED
  - I've yet to implement this as ZMK seems to have an [OLED issue](https://github.com/zmkfirmware/zmk/issues/674), but I believe a kit [like this](https://smile.amazon.com/gp/product/B0925V1DZK/) should work
- 2x rotary encoder and knob
- 2x USB-C cables
  - You could just cut up USB-C cables you have and solder one end to the board and plug the other into your nice!nano, but note that the clearance for the nice!nano USB-C and the reset button etc is very slim
  - I opted for some [USB 2.0 cable](https://cruzctrl.gg/collections/diy-cable-parts/products/cable) along with some [USB-C 2.0 connectors](https://cruzctrl.gg/collections/diy-cable-parts/products/usb-c-2-0-connector)
- Case for the keyboard
  - I'm having mine printed from [craftcloud3d](https://craftcloud3d.com/), and they provided me with a 10% referral code: `REF49BRI7SK`
  - The .stl files worked better in my case, and a full PLA build cost about $50-60

