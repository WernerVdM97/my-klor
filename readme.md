<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/klor-font-logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/klor-font-logo-bright.svg">
  <img alt="KLOR logo font" src="/docs/images/klor-font-logo-bright.svg">
</picture>

# By Werner
40 key column-staggered split keyboard, per key RGB matrix, encoders, OLED displays, haptic feedback, and audio.
![KLOR layouts](/docs/images/klor-layouts.svg)

QWERTY layout + nav-, number-, and symbol- layers.

If you choose one of the other layouts you can use the matching template in the default keymap.\
If you choose Konrad or Saegewerk and plan on using LEDs you need to uncomment the appropiate lines in the `klor.c` file.


## AVR MCU
**Sparkfun Pro Micro / Elite-C / Puchi-C**

You'll need to setup a local build environment of QMK. [Here](https://docs.qmk.fm/) you can find the instructions.\
Place the klor folder from this repository in the keyboards folder of your qmk installation.\
Than you can use this command to compile the firmware for the KLOR.

`qmk compile -kb klor -km default`




## RP2040 MCU
**Adafruit KB2040 / Sparkfun Pro Micro RP2040 / BastardKB Splinky / Boardsource Blok / Elite-Pi / Sea-Picro / key micro RP**

Place the klor folder from this repository in the keyboards folder of your qmk installation.\
Most of the RP2040 MCUs use the same pinout, the Adafruit KB2040 is an exclusion. If you plan on using it you need to uncomment the appropiate lines in the `/2040/rules.mk` file.\
Than you can use this command to compile the RP2040 firmware for the KLOR.

`qmk compile -kb klor/2040 -km default`


## TODO
- Add VIA(L) support
- Add custom LED animation
- Add OLED animation, see [video](https://www.youtube.com/watch?v=OJSOEStpPIo)
- Make the haptic feedback work on the peripheral side
