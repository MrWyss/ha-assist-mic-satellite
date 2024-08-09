# HA Assist Mic Satellite

![GitHub last commit (branch)](https://img.shields.io/github/last-commit/MrWyss/ha-assist-mic-satellite/main)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/mrwyss/ha-assist-mic-satellite/publish.yml)
![GitHub manifest.json dynamic (branch)](https://img.shields.io/github/manifest-json/Version/mrwyss/ha-assist-mic-satellite/gh-pages?label=Version)
![GitHub Repo stars](https://img.shields.io/github/stars/mrwyss/ha-assist-mic-satellite)

<p align="center">
  <img alt="Logo" src="docs/assets/MicSatellite_Color_V3.png" width="100">
</p>

***<p style="text-align: center;">«The HA Assist Mic Satellite is a compact, ESPHome-based microphone only solution.»</p>***

## Features

*2024-08-08: This is in very early development. The firmware is working, but the documentation is still in progress. The PCB and case are still in development.*

A ~~tiny~~ Atom version of the [ESP32-S3-BOX](https://esphome.io/projects/index.html)

- Local **wake word detection** (😲 holy cow, this works fast and so well)
- Redirect TTS to a configurable media **media player entity** e.g. SONOS, to play the response
- HA **Assist Pipeline integration**
- Turn **on** and **off** listening mode (**wake word detection**)
- **Show current state** (listening, idle, request, response) on the display. It is fairly readable, though it requires good eyesight 👀.

### Future ideas

- [x] **Ready made project** / **Made for ESPHome** if that is requested
- [ ] option to change the wake word
- [ ] Online OTA update for the firmware
- [ ] Redesign Animation (for small screens)
- [ ] 🚧 **Timers** (this is still work in progress)
- [ ] 3D printable **case** and **mounting solution** for the AtomS3 and the microphone
- [ ] Royalty free **sound files** the alarm

## TL;DR

Gather the following items: **M5Stack AtomS3**, [PCB](https://www.pcbway.com/project/shareproject/HA_Assist_Mic_Satellite_f5cc4682.html), header sockets and pins, and an INMP441 breakout board.
3D print the case, solder the pbc, [flash the firmware](https://www.ittips.ch/ha-assist-mic-satellite/), configure the device in Home Assistant (**Allow the device to perform Home Assistant actions** and configure your **media_player entitiy**), and you're all set.

## Try it out / Tricks

- **Wake Word**: "Okay Nabu"
- The display itself is also a button, so you can **double press to mute** the device, it stops listening for the wake word.
- If you have Music Assistant you can change the **announcement volumes**. Goto the Music Assistant Addon -> Settings -> Players -> Your Speaker -> Configure -> Announcements configuration

## Hardware

### BOM

- [M5Stack AtomS3](https://docs.m5stack.com/en/core/AtomS3) ~15$
- [PCB](#pcb) ~5$ + Shipping
- [Case](#case) ~0.5$ Filament
- **INMP441** Breakout Board (usually comes with PinSockets) ~2$
  - 2x PinSocket 1x03 2.54mm (J3, J4)
- 1x PinHeader 1x05 2.54mm (J1)
- 1x PinHeader 1x04 2.54mm (J2)
- M2 x 5mm Screw nylon or with metal with nylon washer (optional)

### PCB

The pcb was designed in KiCAD. [KiCAD Canvas Online View](https://kicanvas.org/?github=https%3A%2F%2Fgithub.com%2FMrWyss%2Fha-assist-mic-satellite%2Ftree%2Fmain%2Fpcb%2FMic%2520HAT%2520for%2520M5Stack%2520Atom) | [KiCad Project](pcb/Mic%20HAT%20for%20M5Stack%20Atom) | [PCB Step File](<pcb/Mic HAT for M5Stack Atom/Mic HAT for M5Stack Atom.step>)

🔜 Order from [PCBWay](https://www.pcbway.com/project/shareproject/HA_Assist_Mic_Satellite_f5cc4682.html) (affiliated link)

### Case

The case was designed in Fusion 360 and exported as 3mf files and step files. [Step files](case/step) | [3mf files](case/3mf)
It shouldn't need any supports for 3d printing, but I recommend printing it with your high detail settings. It is rather small.

#### Body preview

```stl
solid ASCII
  facet normal 1.000000e+00 -0.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 1.200000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   -5.100000e+00 -9.000000e-02 1.200000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.200000e+01
      vertex   5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   1.138800e+00 -3.590000e+00 -2.589998e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   1.138800e+00 -3.590000e+00 -2.589998e-01
      vertex   1.084962e+00 -3.590000e+00 -5.989185e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   6.000000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 -4.050000e+00
      vertex   1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   1.094889e+01 -3.590000e+00 9.888229e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   1.094889e+01 -3.590000e+00 9.888229e+00
      vertex   1.079904e+01 -3.590000e+00 1.025000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   9.240000e+00 -3.590000e+00 -4.050000e+00
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   9.240000e+00 -3.590000e+00 -4.050000e+00
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   9.500000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   3.787188e-01 -3.590000e+00 -1.305162e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   3.787188e-01 -3.590000e+00 -1.305162e+00
      vertex   3.880009e-02 -3.590000e+00 -1.359000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   -6.000000e+00 -3.590000e+00 5.000000e+00
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   -6.000000e+00 -3.590000e+00 5.000000e+00
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -1.007362e+00 -3.590000e+00 8.091887e-02
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.007362e+00 -3.590000e+00 8.091887e-02
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -1.061200e+00 -3.590000e+00 -2.589998e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.061200e+00 -3.590000e+00 -2.589998e-01
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -1.007362e+00 -3.590000e+00 -5.989185e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.007362e+00 -3.590000e+00 -5.989185e-01
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -8.511186e-01 -3.590000e+00 -9.055636e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -8.511186e-01 -3.590000e+00 -9.055636e-01
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -6.077637e-01 -3.590000e+00 -1.148919e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.077637e-01 -3.590000e+00 -1.148919e+00
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -6.077637e-01 -3.590000e+00 -1.148919e+00
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   -3.011186e-01 -3.590000e+00 -1.305162e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -3.011186e-01 -3.590000e+00 -1.305162e+00
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   3.880009e-02 -3.590000e+00 -1.359000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   3.880009e-02 -3.590000e+00 -1.359000e+00
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.240000e+00 -3.590000e+00 -1.510000e+00
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   -9.500000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   -9.240000e+00 -3.590000e+00 -1.510000e+00
      vertex   -1.100000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   -9.240000e+00 -3.590000e+00 -1.510000e+00
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -1.094889e+01 -3.590000e+00 9.888229e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.094889e+01 -3.590000e+00 9.888229e+00
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -1.079904e+01 -3.590000e+00 1.025000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.079904e+01 -3.590000e+00 1.025000e+01
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -1.056066e+01 -3.590000e+00 1.056066e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.056066e+01 -3.590000e+00 1.056066e+01
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -1.025000e+01 -3.590000e+00 1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.025000e+01 -3.590000e+00 1.079904e+01
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -9.888229e+00 -3.590000e+00 1.094889e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.888229e+00 -3.590000e+00 1.094889e+01
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -9.500000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -6.000000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   -6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   -6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.007362e+00 -3.590000e+00 8.091887e-02
      vertex   -8.511186e-01 -3.590000e+00 3.875640e-01
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   -8.511186e-01 -3.590000e+00 3.875640e-01
      vertex   -6.077637e-01 -3.590000e+00 6.309189e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   -6.077637e-01 -3.590000e+00 6.309189e-01
      vertex   -3.011186e-01 -3.590000e+00 7.871623e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -3.011186e-01 -3.590000e+00 7.871623e-01
      vertex   3.880009e-02 -3.590000e+00 8.410002e-01
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   3.880009e-02 -3.590000e+00 8.410002e-01
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   3.880009e-02 -3.590000e+00 8.410002e-01
      vertex   3.787188e-01 -3.590000e+00 7.871623e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   3.787188e-01 -3.590000e+00 7.871623e-01
      vertex   6.853639e-01 -3.590000e+00 6.309189e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   6.853639e-01 -3.590000e+00 6.309189e-01
      vertex   9.287188e-01 -3.590000e+00 3.875640e-01
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   9.287188e-01 -3.590000e+00 3.875640e-01
      vertex   1.084962e+00 -3.590000e+00 8.091887e-02
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 5.000000e+00
      vertex   1.084962e+00 -3.590000e+00 8.091887e-02
      vertex   1.138800e+00 -3.590000e+00 -2.589998e-01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.084962e+00 -3.590000e+00 -5.989185e-01
      vertex   9.287188e-01 -3.590000e+00 -9.055636e-01
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   9.287188e-01 -3.590000e+00 -9.055636e-01
      vertex   6.853639e-01 -3.590000e+00 -1.148919e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   6.853639e-01 -3.590000e+00 -1.148919e+00
      vertex   3.787188e-01 -3.590000e+00 -1.305162e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.094889e+01 -3.590000e+00 -9.888229e+00
      vertex   -1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   -1.056066e+01 -3.590000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.056066e+01 -3.590000e+00 -1.056066e+01
      vertex   -1.025000e+01 -3.590000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.025000e+01 -3.590000e+00 -1.079904e+01
      vertex   -9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   -9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   3.800000e+00 -3.590000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   -9.987726e+00 -3.590000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   -9.945042e+00 -3.590000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   -9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   -1.045671e+01 -3.590000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   -9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   -1.036777e+01 -3.590000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   -1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   -1.088893e+01 -3.590000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   -1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   -1.074698e+01 -3.590000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   -1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   -1.126777e+01 -3.590000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   -1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   -1.106366e+01 -3.590000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   -1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   -1.157867e+01 -3.590000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   -1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   -1.130194e+01 -3.590000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   -1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   -1.180970e+01 -3.590000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   -1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   -1.144986e+01 -3.590000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   -1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   -1.195196e+01 -3.590000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   -1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.200000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.200000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.150000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.195196e+01 -3.590000e+00 9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   -1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.144986e+01 -3.590000e+00 9.945042e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   -1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   -1.180970e+01 -3.590000e+00 1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   -1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   -1.130194e+01 -3.590000e+00 1.036777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   -1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   -1.157867e+01 -3.590000e+00 1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   -1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   -1.106366e+01 -3.590000e+00 1.074698e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   -1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   -1.126777e+01 -3.590000e+00 1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   -1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   -1.074698e+01 -3.590000e+00 1.106366e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   -1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   -1.088893e+01 -3.590000e+00 1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   -1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   -1.036777e+01 -3.590000e+00 1.130194e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   -1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   -1.045671e+01 -3.590000e+00 1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   -1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   -9.945042e+00 -3.590000e+00 1.144986e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   -9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   -9.987726e+00 -3.590000e+00 1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   -9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   -9.500000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   -9.500000e+00 -3.590000e+00 1.150000e+01
      vertex   -9.500000e+00 -3.590000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   -9.500000e+00 -3.590000e+00 1.150000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   9.987726e+00 -3.590000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   9.945042e+00 -3.590000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   1.045671e+01 -3.590000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   1.036777e+01 -3.590000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   1.088893e+01 -3.590000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   1.074698e+01 -3.590000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   1.126777e+01 -3.590000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   1.106366e+01 -3.590000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   1.157867e+01 -3.590000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   1.130194e+01 -3.590000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   1.180970e+01 -3.590000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   1.144986e+01 -3.590000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   1.195196e+01 -3.590000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   1.150000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   1.200000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.200000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   1.200000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.200000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   1.200000e+01 -3.590000e+00 9.500000e+00
      vertex   1.195196e+01 -3.590000e+00 9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   1.144986e+01 -3.590000e+00 9.945042e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   1.180970e+01 -3.590000e+00 1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   1.130194e+01 -3.590000e+00 1.036777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   1.157867e+01 -3.590000e+00 1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   1.106366e+01 -3.590000e+00 1.074698e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   1.126777e+01 -3.590000e+00 1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   1.074698e+01 -3.590000e+00 1.106366e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   1.088893e+01 -3.590000e+00 1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   1.036777e+01 -3.590000e+00 1.130194e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   1.045671e+01 -3.590000e+00 1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   9.945042e+00 -3.590000e+00 1.144986e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   9.987726e+00 -3.590000e+00 1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   9.500000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 1.150000e+01
      vertex   9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   9.500000e+00 -3.590000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   5.100000e+00 -3.590000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   1.025000e+01 -3.590000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.025000e+01 -3.590000e+00 -1.079904e+01
      vertex   1.056066e+01 -3.590000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.056066e+01 -3.590000e+00 -1.056066e+01
      vertex   1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   1.094889e+01 -3.590000e+00 -9.888229e+00
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.079904e+01 -3.590000e+00 1.025000e+01
      vertex   1.056066e+01 -3.590000e+00 1.056066e+01
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   1.056066e+01 -3.590000e+00 1.056066e+01
      vertex   1.025000e+01 -3.590000e+00 1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   1.025000e+01 -3.590000e+00 1.079904e+01
      vertex   9.888229e+00 -3.590000e+00 1.094889e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.888229e+00 -3.590000e+00 1.094889e+01
      vertex   9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.200000e+01
      vertex   9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   5.100000e+00 -9.000000e-02 1.200000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   9.500000e+00 -9.000000e-02 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   -9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 1.200000e+01
      vertex   -9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   -9.500000e+00 -3.590000e+00 1.200000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   -5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   -6.000000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   -5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -6.000000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 5.000000e+00
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -1.007362e+00 -9.000000e-02 8.091887e-02
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -1.007362e+00 -9.000000e-02 8.091887e-02
      vertex   -1.061200e+00 -9.000000e-02 -2.589998e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   3.880009e-02 -9.000000e-02 8.410002e-01
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   3.880009e-02 -9.000000e-02 8.410002e-01
      vertex   -3.011186e-01 -9.000000e-02 7.871623e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -3.011186e-01 -9.000000e-02 7.871623e-01
      vertex   -6.077637e-01 -9.000000e-02 6.309189e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   1.138800e+00 -9.000000e-02 -2.589998e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.138800e+00 -9.000000e-02 -2.589998e-01
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   1.084962e+00 -9.000000e-02 -5.989185e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.084962e+00 -9.000000e-02 -5.989185e-01
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   9.287188e-01 -9.000000e-02 -9.055636e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.287188e-01 -9.000000e-02 -9.055636e-01
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   6.853639e-01 -9.000000e-02 -1.148919e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   6.853639e-01 -9.000000e-02 -1.148919e+00
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   3.787188e-01 -9.000000e-02 -1.305162e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   3.787188e-01 -9.000000e-02 -1.305162e+00
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   3.880009e-02 -9.000000e-02 -1.359000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   3.880009e-02 -9.000000e-02 -1.359000e+00
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   3.880009e-02 -9.000000e-02 -1.359000e+00
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   -3.011186e-01 -9.000000e-02 -1.305162e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -3.011186e-01 -9.000000e-02 -1.305162e+00
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -3.011186e-01 -9.000000e-02 -1.305162e+00
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -6.077637e-01 -9.000000e-02 -1.148919e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.077637e-01 -9.000000e-02 -1.148919e+00
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -8.511186e-01 -9.000000e-02 -9.055636e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -8.511186e-01 -9.000000e-02 -9.055636e-01
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -1.007362e+00 -9.000000e-02 -5.989185e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.007362e+00 -9.000000e-02 -5.989185e-01
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -1.061200e+00 -9.000000e-02 -2.589998e-01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 1.200000e+01
      vertex   9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   6.000000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   9.987726e+00 -9.000000e-02 1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   9.987726e+00 -9.000000e-02 1.195196e+01
      vertex   1.045671e+01 -9.000000e-02 1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.045671e+01 -9.000000e-02 1.180970e+01
      vertex   1.088893e+01 -9.000000e-02 1.157867e+01
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   1.088893e+01 -9.000000e-02 1.157867e+01
      vertex   1.126777e+01 -9.000000e-02 1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   1.126777e+01 -9.000000e-02 1.126777e+01
      vertex   1.157867e+01 -9.000000e-02 1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.157867e+01 -9.000000e-02 1.088893e+01
      vertex   1.180970e+01 -9.000000e-02 1.045671e+01
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   1.180970e+01 -9.000000e-02 1.045671e+01
      vertex   1.195196e+01 -9.000000e-02 9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   1.195196e+01 -9.000000e-02 9.987726e+00
      vertex   1.200000e+01 -9.000000e-02 9.500000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   9.240000e+00 -9.000000e-02 -4.050000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 -4.050000e+00
      vertex   1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 -4.050000e+00
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   9.987726e+00 -9.000000e-02 -1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.987726e+00 -9.000000e-02 -1.195196e+01
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   1.045671e+01 -9.000000e-02 -1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.045671e+01 -9.000000e-02 -1.180970e+01
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   1.088893e+01 -9.000000e-02 -1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.088893e+01 -9.000000e-02 -1.157867e+01
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   1.126777e+01 -9.000000e-02 -1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.126777e+01 -9.000000e-02 -1.126777e+01
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   1.157867e+01 -9.000000e-02 -1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.157867e+01 -9.000000e-02 -1.088893e+01
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   1.180970e+01 -9.000000e-02 -1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.180970e+01 -9.000000e-02 -1.045671e+01
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   1.195196e+01 -9.000000e-02 -9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 -4.050000e+00
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   -9.987726e+00 -9.000000e-02 -1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -9.987726e+00 -9.000000e-02 -1.195196e+01
      vertex   -1.045671e+01 -9.000000e-02 -1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -9.000000e-02 -1.180970e+01
      vertex   -1.088893e+01 -9.000000e-02 -1.157867e+01
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.088893e+01 -9.000000e-02 -1.157867e+01
      vertex   -1.126777e+01 -9.000000e-02 -1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.126777e+01 -9.000000e-02 -1.126777e+01
      vertex   -1.157867e+01 -9.000000e-02 -1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -9.000000e-02 -1.088893e+01
      vertex   -1.180970e+01 -9.000000e-02 -1.045671e+01
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.180970e+01 -9.000000e-02 -1.045671e+01
      vertex   -1.195196e+01 -9.000000e-02 -9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -9.240000e+00 -9.000000e-02 -1.510000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 -1.510000e+00
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.200000e+01 -9.000000e-02 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 -1.510000e+00
      vertex   -1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   -1.195196e+01 -9.000000e-02 9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -1.195196e+01 -9.000000e-02 9.987726e+00
      vertex   -1.180970e+01 -9.000000e-02 1.045671e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -9.000000e-02 1.045671e+01
      vertex   -1.157867e+01 -9.000000e-02 1.088893e+01
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -1.157867e+01 -9.000000e-02 1.088893e+01
      vertex   -1.126777e+01 -9.000000e-02 1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -1.126777e+01 -9.000000e-02 1.126777e+01
      vertex   -1.088893e+01 -9.000000e-02 1.157867e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -9.000000e-02 1.157867e+01
      vertex   -1.045671e+01 -9.000000e-02 1.180970e+01
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -1.045671e+01 -9.000000e-02 1.180970e+01
      vertex   -9.987726e+00 -9.000000e-02 1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -9.987726e+00 -9.000000e-02 1.195196e+01
      vertex   -9.500000e+00 -9.000000e-02 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   -6.000000e+00 -9.000000e-02 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.138800e+00 -9.000000e-02 -2.589998e-01
      vertex   1.084962e+00 -9.000000e-02 8.091887e-02
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   1.084962e+00 -9.000000e-02 8.091887e-02
      vertex   9.287188e-01 -9.000000e-02 3.875640e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   9.287188e-01 -9.000000e-02 3.875640e-01
      vertex   6.853639e-01 -9.000000e-02 6.309189e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   6.853639e-01 -9.000000e-02 6.309189e-01
      vertex   3.787188e-01 -9.000000e-02 7.871623e-01
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   3.787188e-01 -9.000000e-02 7.871623e-01
      vertex   3.880009e-02 -9.000000e-02 8.410002e-01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -6.077637e-01 -9.000000e-02 6.309189e-01
      vertex   -8.511186e-01 -9.000000e-02 3.875640e-01
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -5.100000e+00 -9.000000e-02 5.000000e+00
      vertex   -8.511186e-01 -9.000000e-02 3.875640e-01
      vertex   -1.007362e+00 -9.000000e-02 8.091887e-02
    endloop
  endfacet
  facet normal 9.937122e-01 -0.000000e+00 1.119645e-01
    outer loop
      vertex   1.150000e+01 -9.200000e+00 9.500000e+00
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   1.144986e+01 -9.200000e+00 9.945042e+00
    endloop
  endfacet
  facet normal 9.937122e-01 -0.000000e+00 1.119645e-01
    outer loop
      vertex   1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   1.144986e+01 -3.590000e+00 9.945042e+00
    endloop
  endfacet
  facet normal 9.438833e-01 -0.000000e+00 3.302791e-01
    outer loop
      vertex   1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   1.130194e+01 -9.200000e+00 1.036777e+01
    endloop
  endfacet
  facet normal 9.438833e-01 -0.000000e+00 3.302791e-01
    outer loop
      vertex   1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   1.130194e+01 -3.590000e+00 1.036777e+01
    endloop
  endfacet
  facet normal 8.467242e-01 -0.000000e+00 5.320321e-01
    outer loop
      vertex   1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   1.106366e+01 -9.200000e+00 1.074698e+01
    endloop
  endfacet
  facet normal 8.467242e-01 -0.000000e+00 5.320321e-01
    outer loop
      vertex   1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   1.106366e+01 -3.590000e+00 1.074698e+01
    endloop
  endfacet
  facet normal 7.071068e-01 -0.000000e+00 7.071068e-01
    outer loop
      vertex   1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   1.074698e+01 -9.200000e+00 1.106366e+01
    endloop
  endfacet
  facet normal 7.071068e-01 -0.000000e+00 7.071068e-01
    outer loop
      vertex   1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   1.074698e+01 -3.590000e+00 1.106366e+01
    endloop
  endfacet
  facet normal 5.320321e-01 -0.000000e+00 8.467242e-01
    outer loop
      vertex   1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   1.036777e+01 -9.200000e+00 1.130194e+01
    endloop
  endfacet
  facet normal 5.320321e-01 -0.000000e+00 8.467242e-01
    outer loop
      vertex   1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   1.036777e+01 -3.590000e+00 1.130194e+01
    endloop
  endfacet
  facet normal 3.302791e-01 -0.000000e+00 9.438833e-01
    outer loop
      vertex   1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   9.945042e+00 -9.200000e+00 1.144986e+01
    endloop
  endfacet
  facet normal 3.302791e-01 -0.000000e+00 9.438833e-01
    outer loop
      vertex   9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   9.945042e+00 -3.590000e+00 1.144986e+01
    endloop
  endfacet
  facet normal 1.119645e-01 -0.000000e+00 9.937122e-01
    outer loop
      vertex   9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   9.500000e+00 -9.200000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 1.119645e-01 -0.000000e+00 9.937122e-01
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   9.500000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 1.150000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   9.500000e+00 -9.200000e+00 1.150000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.150000e+01
      vertex   9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 1.150000e+01
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 9.937122e-01
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   -9.500000e+00 -3.590000e+00 1.150000e+01
      vertex   -9.945042e+00 -9.200000e+00 1.144986e+01
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 9.937122e-01
    outer loop
      vertex   -9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   -9.500000e+00 -3.590000e+00 1.150000e+01
      vertex   -9.945042e+00 -3.590000e+00 1.144986e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 9.438833e-01
    outer loop
      vertex   -9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   -9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   -1.036777e+01 -9.200000e+00 1.130194e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 9.438833e-01
    outer loop
      vertex   -1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   -9.945042e+00 -3.590000e+00 1.144986e+01
      vertex   -1.036777e+01 -3.590000e+00 1.130194e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 8.467242e-01
    outer loop
      vertex   -1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   -1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   -1.074698e+01 -9.200000e+00 1.106366e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 8.467242e-01
    outer loop
      vertex   -1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   -1.036777e+01 -3.590000e+00 1.130194e+01
      vertex   -1.074698e+01 -3.590000e+00 1.106366e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   -1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   -1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   -1.106366e+01 -9.200000e+00 1.074698e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   -1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   -1.074698e+01 -3.590000e+00 1.106366e+01
      vertex   -1.106366e+01 -3.590000e+00 1.074698e+01
    endloop
  endfacet
  facet normal -8.467242e-01 0.000000e+00 5.320321e-01
    outer loop
      vertex   -1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   -1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   -1.130194e+01 -9.200000e+00 1.036777e+01
    endloop
  endfacet
  facet normal -8.467242e-01 0.000000e+00 5.320321e-01
    outer loop
      vertex   -1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   -1.106366e+01 -3.590000e+00 1.074698e+01
      vertex   -1.130194e+01 -3.590000e+00 1.036777e+01
    endloop
  endfacet
  facet normal -9.438833e-01 0.000000e+00 3.302791e-01
    outer loop
      vertex   -1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   -1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   -1.144986e+01 -9.200000e+00 9.945042e+00
    endloop
  endfacet
  facet normal -9.438833e-01 0.000000e+00 3.302791e-01
    outer loop
      vertex   -1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   -1.130194e+01 -3.590000e+00 1.036777e+01
      vertex   -1.144986e+01 -3.590000e+00 9.945042e+00
    endloop
  endfacet
  facet normal -9.937122e-01 0.000000e+00 1.119645e-01
    outer loop
      vertex   -1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   -1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   -1.150000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -9.937122e-01 -6.293003e-16 1.119645e-01
    outer loop
      vertex   -1.150000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.144986e+01 -3.590000e+00 9.945042e+00
      vertex   -1.150000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 -6.332823e-16 -0.000000e+00
    outer loop
      vertex   -1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.150000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 -6.332823e-16 -0.000000e+00
    outer loop
      vertex   -1.150000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.150000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -9.937122e-01 -6.293003e-16 -1.119645e-01
    outer loop
      vertex   -1.150000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.144986e+01 -9.200000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal -9.937122e-01 0.000000e+00 -1.119645e-01
    outer loop
      vertex   -1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   -1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.144986e+01 -3.590000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal -9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   -1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   -1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   -1.130194e+01 -9.200000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal -9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   -1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   -1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   -1.130194e+01 -3.590000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal -8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   -1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   -1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   -1.106366e+01 -9.200000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal -8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   -1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   -1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   -1.106366e+01 -3.590000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   -1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   -1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   -1.074698e+01 -9.200000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   -1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   -1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   -1.074698e+01 -3.590000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   -1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   -1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   -1.036777e+01 -9.200000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   -1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   -1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   -1.036777e+01 -3.590000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   -1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   -1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   -9.945042e+00 -9.200000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   -9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   -1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   -9.945042e+00 -3.590000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   -9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   -9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.150000e+01
      vertex   -9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.150000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   -3.800000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 -1.583206e-16 0.000000e+00
    outer loop
      vertex   -3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   -3.800000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 -1.583206e-16 0.000000e+00
    outer loop
      vertex   -3.800000e+00 -9.200000e+00 -1.150000e+01
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   -3.800000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   -3.800000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -3.800000e+00 -9.200000e+00 -1.100000e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 1.305262e-01 -0.000000e+00 9.914449e-01
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   -9.888229e+00 -9.200000e+00 -1.094889e+01
    endloop
  endfacet
  facet normal 1.305262e-01 -4.132996e-17 9.914449e-01
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   -9.888229e+00 -3.590000e+00 -1.094889e+01
    endloop
  endfacet
  facet normal 3.826834e-01 -1.211733e-16 9.238795e-01
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   -9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   -1.025000e+01 -9.200000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal 3.826834e-01 5.019163e-17 9.238795e-01
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   -9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   -1.025000e+01 -3.590000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal 6.087614e-01 -1.343095e-16 7.933533e-01
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   -1.025000e+01 -3.590000e+00 -1.079904e+01
      vertex   -1.056066e+01 -9.200000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal 6.087614e-01 -0.000000e+00 7.933533e-01
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   -1.025000e+01 -3.590000e+00 -1.079904e+01
      vertex   -1.056066e+01 -3.590000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal 7.933533e-01 -0.000000e+00 6.087614e-01
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   -1.056066e+01 -3.590000e+00 -1.056066e+01
      vertex   -1.079904e+01 -9.200000e+00 -1.025000e+01
    endloop
  endfacet
  facet normal 7.933533e-01 -0.000000e+00 6.087614e-01
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   -1.056066e+01 -3.590000e+00 -1.056066e+01
      vertex   -1.079904e+01 -3.590000e+00 -1.025000e+01
    endloop
  endfacet
  facet normal 9.238795e-01 -0.000000e+00 3.826834e-01
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   -1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   -1.094889e+01 -9.200000e+00 -9.888229e+00
    endloop
  endfacet
  facet normal 9.238795e-01 -0.000000e+00 3.826834e-01
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   -1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   -1.094889e+01 -3.590000e+00 -9.888229e+00
    endloop
  endfacet
  facet normal 9.914449e-01 -0.000000e+00 1.305262e-01
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   -1.094889e+01 -3.590000e+00 -9.888229e+00
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 9.914449e-01 -0.000000e+00 1.305262e-01
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.094889e+01 -3.590000e+00 -9.888229e+00
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.100000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 9.914449e-01 0.000000e+00 -1.305262e-01
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.094889e+01 -9.200000e+00 9.888229e+00
    endloop
  endfacet
  facet normal 9.914449e-01 -4.132996e-17 -1.305262e-01
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   -1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.094889e+01 -3.590000e+00 9.888229e+00
    endloop
  endfacet
  facet normal 9.238795e-01 -1.211733e-16 -3.826834e-01
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   -1.094889e+01 -3.590000e+00 9.888229e+00
      vertex   -1.079904e+01 -9.200000e+00 1.025000e+01
    endloop
  endfacet
  facet normal 9.238795e-01 5.019163e-17 -3.826834e-01
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   -1.094889e+01 -3.590000e+00 9.888229e+00
      vertex   -1.079904e+01 -3.590000e+00 1.025000e+01
    endloop
  endfacet
  facet normal 7.933533e-01 -1.343095e-16 -6.087614e-01
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   -1.079904e+01 -3.590000e+00 1.025000e+01
      vertex   -1.056066e+01 -9.200000e+00 1.056066e+01
    endloop
  endfacet
  facet normal 7.933533e-01 0.000000e+00 -6.087614e-01
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   -1.079904e+01 -3.590000e+00 1.025000e+01
      vertex   -1.056066e+01 -3.590000e+00 1.056066e+01
    endloop
  endfacet
  facet normal 6.087614e-01 0.000000e+00 -7.933533e-01
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   -1.056066e+01 -3.590000e+00 1.056066e+01
      vertex   -1.025000e+01 -9.200000e+00 1.079904e+01
    endloop
  endfacet
  facet normal 6.087614e-01 0.000000e+00 -7.933533e-01
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   -1.056066e+01 -3.590000e+00 1.056066e+01
      vertex   -1.025000e+01 -3.590000e+00 1.079904e+01
    endloop
  endfacet
  facet normal 3.826834e-01 0.000000e+00 -9.238795e-01
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   -1.025000e+01 -3.590000e+00 1.079904e+01
      vertex   -9.888229e+00 -9.200000e+00 1.094889e+01
    endloop
  endfacet
  facet normal 3.826834e-01 0.000000e+00 -9.238795e-01
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   -1.025000e+01 -3.590000e+00 1.079904e+01
      vertex   -9.888229e+00 -3.590000e+00 1.094889e+01
    endloop
  endfacet
  facet normal 1.305262e-01 0.000000e+00 -9.914449e-01
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   -9.888229e+00 -3.590000e+00 1.094889e+01
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 1.305262e-01 6.278645e-16 -9.914449e-01
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   -9.888229e+00 -3.590000e+00 1.094889e+01
      vertex   -9.500000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 6.332823e-16 -1.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 6.332823e-16 -1.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 6.332823e-16 -1.000000e+00
    outer loop
      vertex   5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 6.332823e-16 -1.000000e+00
    outer loop
      vertex   -5.100000e+00 -3.590000e+00 1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   -9.500000e+00 -3.590000e+00 1.100000e+01
    endloop
  endfacet
  facet normal -1.305262e-01 6.278645e-16 -9.914449e-01
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   9.888229e+00 -9.200000e+00 1.094889e+01
    endloop
  endfacet
  facet normal -1.305262e-01 -4.132996e-17 -9.914449e-01
    outer loop
      vertex   9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   9.500000e+00 -3.590000e+00 1.100000e+01
      vertex   9.888229e+00 -3.590000e+00 1.094889e+01
    endloop
  endfacet
  facet normal -3.826834e-01 -1.211733e-16 -9.238795e-01
    outer loop
      vertex   9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   9.888229e+00 -3.590000e+00 1.094889e+01
      vertex   1.025000e+01 -9.200000e+00 1.079904e+01
    endloop
  endfacet
  facet normal -3.826834e-01 5.019163e-17 -9.238795e-01
    outer loop
      vertex   1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   9.888229e+00 -3.590000e+00 1.094889e+01
      vertex   1.025000e+01 -3.590000e+00 1.079904e+01
    endloop
  endfacet
  facet normal -6.087614e-01 -1.343095e-16 -7.933533e-01
    outer loop
      vertex   1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   1.025000e+01 -3.590000e+00 1.079904e+01
      vertex   1.056066e+01 -9.200000e+00 1.056066e+01
    endloop
  endfacet
  facet normal -6.087614e-01 0.000000e+00 -7.933533e-01
    outer loop
      vertex   1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   1.025000e+01 -3.590000e+00 1.079904e+01
      vertex   1.056066e+01 -3.590000e+00 1.056066e+01
    endloop
  endfacet
  facet normal -7.933533e-01 0.000000e+00 -6.087614e-01
    outer loop
      vertex   1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   1.056066e+01 -3.590000e+00 1.056066e+01
      vertex   1.079904e+01 -9.200000e+00 1.025000e+01
    endloop
  endfacet
  facet normal -7.933533e-01 0.000000e+00 -6.087614e-01
    outer loop
      vertex   1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   1.056066e+01 -3.590000e+00 1.056066e+01
      vertex   1.079904e+01 -3.590000e+00 1.025000e+01
    endloop
  endfacet
  facet normal -9.238795e-01 0.000000e+00 -3.826834e-01
    outer loop
      vertex   1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   1.079904e+01 -3.590000e+00 1.025000e+01
      vertex   1.094889e+01 -9.200000e+00 9.888229e+00
    endloop
  endfacet
  facet normal -9.238795e-01 0.000000e+00 -3.826834e-01
    outer loop
      vertex   1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   1.079904e+01 -3.590000e+00 1.025000e+01
      vertex   1.094889e+01 -3.590000e+00 9.888229e+00
    endloop
  endfacet
  facet normal -9.914449e-01 0.000000e+00 -1.305262e-01
    outer loop
      vertex   1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   1.094889e+01 -3.590000e+00 9.888229e+00
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -9.914449e-01 0.000000e+00 -1.305262e-01
    outer loop
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   1.094889e+01 -3.590000e+00 9.888229e+00
      vertex   1.100000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 -0.000000e+00 -0.000000e+00
    outer loop
      vertex   1.100000e+01 -3.590000e+00 9.500000e+00
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.100000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -9.914449e-01 0.000000e+00 1.305262e-01
    outer loop
      vertex   1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.094889e+01 -9.200000e+00 -9.888229e+00
    endloop
  endfacet
  facet normal -9.914449e-01 -4.132996e-17 1.305262e-01
    outer loop
      vertex   1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   1.100000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.094889e+01 -3.590000e+00 -9.888229e+00
    endloop
  endfacet
  facet normal -9.238795e-01 -1.211733e-16 3.826834e-01
    outer loop
      vertex   1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   1.094889e+01 -3.590000e+00 -9.888229e+00
      vertex   1.079904e+01 -9.200000e+00 -1.025000e+01
    endloop
  endfacet
  facet normal -9.238795e-01 5.019163e-17 3.826834e-01
    outer loop
      vertex   1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   1.094889e+01 -3.590000e+00 -9.888229e+00
      vertex   1.079904e+01 -3.590000e+00 -1.025000e+01
    endloop
  endfacet
  facet normal -7.933533e-01 -1.343095e-16 6.087614e-01
    outer loop
      vertex   1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   1.056066e+01 -9.200000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal -7.933533e-01 0.000000e+00 6.087614e-01
    outer loop
      vertex   1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   1.079904e+01 -3.590000e+00 -1.025000e+01
      vertex   1.056066e+01 -3.590000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal -6.087614e-01 0.000000e+00 7.933533e-01
    outer loop
      vertex   1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   1.056066e+01 -3.590000e+00 -1.056066e+01
      vertex   1.025000e+01 -9.200000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal -6.087614e-01 0.000000e+00 7.933533e-01
    outer loop
      vertex   1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   1.056066e+01 -3.590000e+00 -1.056066e+01
      vertex   1.025000e+01 -3.590000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal -3.826834e-01 0.000000e+00 9.238795e-01
    outer loop
      vertex   1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   1.025000e+01 -3.590000e+00 -1.079904e+01
      vertex   9.888229e+00 -9.200000e+00 -1.094889e+01
    endloop
  endfacet
  facet normal -3.826834e-01 0.000000e+00 9.238795e-01
    outer loop
      vertex   9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   1.025000e+01 -3.590000e+00 -1.079904e+01
      vertex   9.888229e+00 -3.590000e+00 -1.094889e+01
    endloop
  endfacet
  facet normal -1.305262e-01 0.000000e+00 9.914449e-01
    outer loop
      vertex   9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal -1.305262e-01 0.000000e+00 9.914449e-01
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   9.888229e+00 -3.590000e+00 -1.094889e+01
      vertex   9.500000e+00 -3.590000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   9.500000e+00 -3.590000e+00 -1.100000e+01
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   3.800000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 7.916029e-17 0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.100000e+01
      vertex   3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   3.800000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 7.916029e-17 0.000000e+00
    outer loop
      vertex   3.800000e+00 -9.200000e+00 -1.100000e+01
      vertex   3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   3.800000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -0.000000e+00 -1.000000e+00
    outer loop
      vertex   3.800000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   3.800000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   3.800000e+00 -9.200000e+00 -1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.500000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.150000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.945042e+00 -9.200000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal 1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   9.500000e+00 -3.590000e+00 -1.150000e+01
      vertex   9.945042e+00 -3.590000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal 3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   1.036777e+01 -9.200000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal 3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   9.945042e+00 -3.590000e+00 -1.144986e+01
      vertex   1.036777e+01 -3.590000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal 5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   1.074698e+01 -9.200000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal 5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   1.036777e+01 -3.590000e+00 -1.130194e+01
      vertex   1.074698e+01 -3.590000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   1.106366e+01 -9.200000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   1.074698e+01 -3.590000e+00 -1.106366e+01
      vertex   1.106366e+01 -3.590000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal 8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   1.130194e+01 -9.200000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal 8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   1.106366e+01 -3.590000e+00 -1.074698e+01
      vertex   1.130194e+01 -3.590000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal 9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   1.144986e+01 -9.200000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal 9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   1.130194e+01 -3.590000e+00 -1.036777e+01
      vertex   1.144986e+01 -3.590000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal 9.937122e-01 0.000000e+00 -1.119645e-01
    outer loop
      vertex   1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   1.150000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 9.937122e-01 0.000000e+00 -1.119645e-01
    outer loop
      vertex   1.150000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.144986e+01 -3.590000e+00 -9.945042e+00
      vertex   1.150000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   1.150000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   1.150000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   1.150000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.150000e+01 -3.590000e+00 9.500000e+00
      vertex   1.150000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -9.200000e+00 -1.150000e+01
      vertex   9.500000e+00 -9.200000e+00 -1.150000e+01
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   9.500000e+00 -9.200000e+00 -1.150000e+01
      vertex   9.945042e+00 -9.200000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   9.888229e+00 -9.200000e+00 -1.094889e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   1.036777e+01 -9.200000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   1.025000e+01 -9.200000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   1.074698e+01 -9.200000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   1.056066e+01 -9.200000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   1.106366e+01 -9.200000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   1.079904e+01 -9.200000e+00 -1.025000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   1.130194e+01 -9.200000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   1.094889e+01 -9.200000e+00 -9.888229e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   1.144986e+01 -9.200000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   1.100000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   1.150000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.150000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   1.150000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.150000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   1.150000e+01 -9.200000e+00 9.500000e+00
      vertex   1.144986e+01 -9.200000e+00 9.945042e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   1.094889e+01 -9.200000e+00 9.888229e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   1.130194e+01 -9.200000e+00 1.036777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   1.079904e+01 -9.200000e+00 1.025000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   1.106366e+01 -9.200000e+00 1.074698e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   1.056066e+01 -9.200000e+00 1.056066e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   1.074698e+01 -9.200000e+00 1.106366e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   1.025000e+01 -9.200000e+00 1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   1.036777e+01 -9.200000e+00 1.130194e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   9.888229e+00 -9.200000e+00 1.094889e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   9.945042e+00 -9.200000e+00 1.144986e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   9.500000e+00 -9.200000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   9.500000e+00 -9.200000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.150000e+01
      vertex   -9.945042e+00 -9.200000e+00 1.144986e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.100000e+01
      vertex   -9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   -9.888229e+00 -9.200000e+00 1.094889e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   -9.945042e+00 -9.200000e+00 1.144986e+01
      vertex   -1.036777e+01 -9.200000e+00 1.130194e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 1.094889e+01
      vertex   -1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   -1.025000e+01 -9.200000e+00 1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   -1.036777e+01 -9.200000e+00 1.130194e+01
      vertex   -1.074698e+01 -9.200000e+00 1.106366e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 1.079904e+01
      vertex   -1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   -1.056066e+01 -9.200000e+00 1.056066e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   -1.074698e+01 -9.200000e+00 1.106366e+01
      vertex   -1.106366e+01 -9.200000e+00 1.074698e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 1.056066e+01
      vertex   -1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   -1.079904e+01 -9.200000e+00 1.025000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   -1.106366e+01 -9.200000e+00 1.074698e+01
      vertex   -1.130194e+01 -9.200000e+00 1.036777e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 1.025000e+01
      vertex   -1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   -1.094889e+01 -9.200000e+00 9.888229e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   -1.130194e+01 -9.200000e+00 1.036777e+01
      vertex   -1.144986e+01 -9.200000e+00 9.945042e+00
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 9.888229e+00
      vertex   -1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   -1.100000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.144986e+01 -9.200000e+00 9.945042e+00
      vertex   -1.150000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.150000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.150000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.150000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.150000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.144986e+01 -9.200000e+00 -9.945042e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.100000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   -1.094889e+01 -9.200000e+00 -9.888229e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   -1.144986e+01 -9.200000e+00 -9.945042e+00
      vertex   -1.130194e+01 -9.200000e+00 -1.036777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.094889e+01 -9.200000e+00 -9.888229e+00
      vertex   -1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   -1.079904e+01 -9.200000e+00 -1.025000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   -1.130194e+01 -9.200000e+00 -1.036777e+01
      vertex   -1.106366e+01 -9.200000e+00 -1.074698e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.079904e+01 -9.200000e+00 -1.025000e+01
      vertex   -1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   -1.056066e+01 -9.200000e+00 -1.056066e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   -1.106366e+01 -9.200000e+00 -1.074698e+01
      vertex   -1.074698e+01 -9.200000e+00 -1.106366e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.056066e+01 -9.200000e+00 -1.056066e+01
      vertex   -1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   -1.025000e+01 -9.200000e+00 -1.079904e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   -1.074698e+01 -9.200000e+00 -1.106366e+01
      vertex   -1.036777e+01 -9.200000e+00 -1.130194e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -1.025000e+01 -9.200000e+00 -1.079904e+01
      vertex   -1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   -9.888229e+00 -9.200000e+00 -1.094889e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   -1.036777e+01 -9.200000e+00 -1.130194e+01
      vertex   -9.945042e+00 -9.200000e+00 -1.144986e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.888229e+00 -9.200000e+00 -1.094889e+01
      vertex   -9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   -9.945042e+00 -9.200000e+00 -1.144986e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.150000e+01
      vertex   -3.800000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -3.800000e+00 -9.200000e+00 -1.150000e+01
      vertex   -3.800000e+00 -9.200000e+00 -1.100000e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.100000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.100000e+01
      vertex   3.800000e+00 -9.200000e+00 -1.100000e+01
      vertex   3.800000e+00 -9.200000e+00 -1.150000e+01
    endloop
  endfacet
  facet normal 2.741291e-16 0.000000e+00 1.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 -4.050000e+00
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   9.240000e+00 -3.590000e+00 -4.050000e+00
    endloop
  endfacet
  facet normal 2.741291e-16 0.000000e+00 1.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 -4.050000e+00
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   6.000000e+00 -9.000000e-02 -4.050000e+00
      vertex   6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 -4.050000e+00
      vertex   6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   6.000000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   -6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   -6.000000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 -0.000000e+00 -0.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   -6.000000e+00 -9.000000e-02 5.000000e+00
      vertex   -6.000000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   -6.000000e+00 -9.000000e-02 5.000000e+00
      vertex   -6.000000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 -0.000000e+00 -1.367825e-08
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 5.000000e+00
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -6.000000e+00 -3.590000e+00 5.000000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 -1.367825e-08
    outer loop
      vertex   -6.000000e+00 -3.590000e+00 5.000000e+00
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   9.500000e+00 -3.590000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 9.801714e-02 0.000000e+00 -9.951847e-01
    outer loop
      vertex   9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   9.987726e+00 -3.590000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal 9.801714e-02 0.000000e+00 -9.951847e-01
    outer loop
      vertex   9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   9.500000e+00 -9.000000e-02 -1.200000e+01
      vertex   9.987726e+00 -9.000000e-02 -1.195196e+01
    endloop
  endfacet
  facet normal 2.902847e-01 0.000000e+00 -9.569403e-01
    outer loop
      vertex   9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   9.987726e+00 -9.000000e-02 -1.195196e+01
      vertex   1.045671e+01 -3.590000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal 2.902847e-01 0.000000e+00 -9.569403e-01
    outer loop
      vertex   1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   9.987726e+00 -9.000000e-02 -1.195196e+01
      vertex   1.045671e+01 -9.000000e-02 -1.180970e+01
    endloop
  endfacet
  facet normal 4.713967e-01 0.000000e+00 -8.819213e-01
    outer loop
      vertex   1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   1.045671e+01 -9.000000e-02 -1.180970e+01
      vertex   1.088893e+01 -3.590000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal 4.713967e-01 -8.952039e-16 -8.819213e-01
    outer loop
      vertex   1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   1.045671e+01 -9.000000e-02 -1.180970e+01
      vertex   1.088893e+01 -9.000000e-02 -1.157867e+01
    endloop
  endfacet
  facet normal 6.343933e-01 -7.846528e-16 -7.730105e-01
    outer loop
      vertex   1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   1.088893e+01 -9.000000e-02 -1.157867e+01
      vertex   1.126777e+01 -3.590000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal 6.343933e-01 -3.923264e-16 -7.730105e-01
    outer loop
      vertex   1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   1.088893e+01 -9.000000e-02 -1.157867e+01
      vertex   1.126777e+01 -9.000000e-02 -1.126777e+01
    endloop
  endfacet
  facet normal 7.730105e-01 -3.219740e-16 -6.343933e-01
    outer loop
      vertex   1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   1.126777e+01 -9.000000e-02 -1.126777e+01
      vertex   1.157867e+01 -3.590000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal 7.730105e-01 0.000000e+00 -6.343933e-01
    outer loop
      vertex   1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   1.126777e+01 -9.000000e-02 -1.126777e+01
      vertex   1.157867e+01 -9.000000e-02 -1.088893e+01
    endloop
  endfacet
  facet normal 8.819213e-01 0.000000e+00 -4.713967e-01
    outer loop
      vertex   1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   1.157867e+01 -9.000000e-02 -1.088893e+01
      vertex   1.180970e+01 -3.590000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal 8.819213e-01 0.000000e+00 -4.713967e-01
    outer loop
      vertex   1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   1.157867e+01 -9.000000e-02 -1.088893e+01
      vertex   1.180970e+01 -9.000000e-02 -1.045671e+01
    endloop
  endfacet
  facet normal 9.569403e-01 0.000000e+00 -2.902847e-01
    outer loop
      vertex   1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   1.180970e+01 -9.000000e-02 -1.045671e+01
      vertex   1.195196e+01 -3.590000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal 9.569403e-01 0.000000e+00 -2.902847e-01
    outer loop
      vertex   1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   1.180970e+01 -9.000000e-02 -1.045671e+01
      vertex   1.195196e+01 -9.000000e-02 -9.987726e+00
    endloop
  endfacet
  facet normal 9.951847e-01 0.000000e+00 -9.801714e-02
    outer loop
      vertex   1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   1.195196e+01 -9.000000e-02 -9.987726e+00
      vertex   1.200000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 9.951847e-01 0.000000e+00 -9.801714e-02
    outer loop
      vertex   1.200000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.195196e+01 -9.000000e-02 -9.987726e+00
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   1.200000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   1.200000e+01 -3.590000e+00 -9.500000e+00
      vertex   1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   1.200000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 9.951847e-01 -0.000000e+00 9.801714e-02
    outer loop
      vertex   1.200000e+01 -3.590000e+00 9.500000e+00
      vertex   1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   1.195196e+01 -3.590000e+00 9.987726e+00
    endloop
  endfacet
  facet normal 9.951847e-01 -0.000000e+00 9.801714e-02
    outer loop
      vertex   1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   1.195196e+01 -9.000000e-02 9.987726e+00
    endloop
  endfacet
  facet normal 9.569403e-01 -0.000000e+00 2.902847e-01
    outer loop
      vertex   1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   1.195196e+01 -9.000000e-02 9.987726e+00
      vertex   1.180970e+01 -3.590000e+00 1.045671e+01
    endloop
  endfacet
  facet normal 9.569403e-01 -0.000000e+00 2.902847e-01
    outer loop
      vertex   1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   1.195196e+01 -9.000000e-02 9.987726e+00
      vertex   1.180970e+01 -9.000000e-02 1.045671e+01
    endloop
  endfacet
  facet normal 8.819213e-01 -0.000000e+00 4.713967e-01
    outer loop
      vertex   1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   1.180970e+01 -9.000000e-02 1.045671e+01
      vertex   1.157867e+01 -3.590000e+00 1.088893e+01
    endloop
  endfacet
  facet normal 8.819213e-01 -0.000000e+00 4.713967e-01
    outer loop
      vertex   1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   1.180970e+01 -9.000000e-02 1.045671e+01
      vertex   1.157867e+01 -9.000000e-02 1.088893e+01
    endloop
  endfacet
  facet normal 7.730105e-01 -0.000000e+00 6.343933e-01
    outer loop
      vertex   1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   1.157867e+01 -9.000000e-02 1.088893e+01
      vertex   1.126777e+01 -3.590000e+00 1.126777e+01
    endloop
  endfacet
  facet normal 7.730105e-01 -0.000000e+00 6.343933e-01
    outer loop
      vertex   1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   1.157867e+01 -9.000000e-02 1.088893e+01
      vertex   1.126777e+01 -9.000000e-02 1.126777e+01
    endloop
  endfacet
  facet normal 6.343933e-01 -0.000000e+00 7.730105e-01
    outer loop
      vertex   1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   1.126777e+01 -9.000000e-02 1.126777e+01
      vertex   1.088893e+01 -3.590000e+00 1.157867e+01
    endloop
  endfacet
  facet normal 6.343933e-01 -0.000000e+00 7.730105e-01
    outer loop
      vertex   1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   1.126777e+01 -9.000000e-02 1.126777e+01
      vertex   1.088893e+01 -9.000000e-02 1.157867e+01
    endloop
  endfacet
  facet normal 4.713967e-01 -0.000000e+00 8.819213e-01
    outer loop
      vertex   1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   1.088893e+01 -9.000000e-02 1.157867e+01
      vertex   1.045671e+01 -3.590000e+00 1.180970e+01
    endloop
  endfacet
  facet normal 4.713967e-01 -0.000000e+00 8.819213e-01
    outer loop
      vertex   1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   1.088893e+01 -9.000000e-02 1.157867e+01
      vertex   1.045671e+01 -9.000000e-02 1.180970e+01
    endloop
  endfacet
  facet normal 2.902847e-01 -0.000000e+00 9.569403e-01
    outer loop
      vertex   1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   1.045671e+01 -9.000000e-02 1.180970e+01
      vertex   9.987726e+00 -3.590000e+00 1.195196e+01
    endloop
  endfacet
  facet normal 2.902847e-01 -3.383481e-16 9.569403e-01
    outer loop
      vertex   9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   1.045671e+01 -9.000000e-02 1.180970e+01
      vertex   9.987726e+00 -9.000000e-02 1.195196e+01
    endloop
  endfacet
  facet normal 9.801714e-02 -4.553399e-16 9.951847e-01
    outer loop
      vertex   9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   9.987726e+00 -9.000000e-02 1.195196e+01
      vertex   9.500000e+00 -3.590000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 9.801714e-02 -0.000000e+00 9.951847e-01
    outer loop
      vertex   9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   9.987726e+00 -9.000000e-02 1.195196e+01
      vertex   9.500000e+00 -9.000000e-02 1.200000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 -0.000000e+00 -0.000000e+00
    outer loop
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   9.240000e+00 -9.000000e-02 -4.050000e+00
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
      vertex   9.240000e+00 -9.000000e-02 -4.050000e+00
      vertex   9.240000e+00 -3.590000e+00 -4.050000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   6.000000e+00 -9.000000e-02 9.350000e+00
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   6.000000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 -1.000000e+00
    outer loop
      vertex   6.000000e+00 -3.590000e+00 9.350000e+00
      vertex   9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.240000e+00 -9.000000e-02 -1.510000e+00
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -9.240000e+00 -3.590000e+00 -1.510000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -9.240000e+00 -3.590000e+00 -1.510000e+00
      vertex   -9.240000e+00 -9.000000e-02 9.350000e+00
      vertex   -9.240000e+00 -3.590000e+00 9.350000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -6.000000e+00 -9.000000e-02 -1.510000e+00
      vertex   -9.240000e+00 -9.000000e-02 -1.510000e+00
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 0.000000e+00 1.000000e+00
    outer loop
      vertex   -6.000000e+00 -3.590000e+00 -1.510000e+00
      vertex   -9.240000e+00 -9.000000e-02 -1.510000e+00
      vertex   -9.240000e+00 -3.590000e+00 -1.510000e+00
    endloop
  endfacet
  facet normal 9.876883e-01 0.000000e+00 -1.564345e-01
    outer loop
      vertex   -1.007362e+00 -9.000000e-02 8.091887e-02
      vertex   -1.007362e+00 -3.590000e+00 8.091887e-02
      vertex   -1.061200e+00 -9.000000e-02 -2.589998e-01
    endloop
  endfacet
  facet normal 9.876883e-01 0.000000e+00 -1.564345e-01
    outer loop
      vertex   -1.061200e+00 -9.000000e-02 -2.589998e-01
      vertex   -1.007362e+00 -3.590000e+00 8.091887e-02
      vertex   -1.061200e+00 -3.590000e+00 -2.589998e-01
    endloop
  endfacet
  facet normal 9.876883e-01 0.000000e+00 1.564345e-01
    outer loop
      vertex   -1.061200e+00 -9.000000e-02 -2.589998e-01
      vertex   -1.061200e+00 -3.590000e+00 -2.589998e-01
      vertex   -1.007362e+00 -9.000000e-02 -5.989185e-01
    endloop
  endfacet
  facet normal 9.876883e-01 0.000000e+00 1.564345e-01
    outer loop
      vertex   -1.007362e+00 -9.000000e-02 -5.989185e-01
      vertex   -1.061200e+00 -3.590000e+00 -2.589998e-01
      vertex   -1.007362e+00 -3.590000e+00 -5.989185e-01
    endloop
  endfacet
  facet normal 8.910065e-01 0.000000e+00 4.539905e-01
    outer loop
      vertex   -1.007362e+00 -9.000000e-02 -5.989185e-01
      vertex   -1.007362e+00 -3.590000e+00 -5.989185e-01
      vertex   -8.511186e-01 -9.000000e-02 -9.055636e-01
    endloop
  endfacet
  facet normal 8.910065e-01 0.000000e+00 4.539905e-01
    outer loop
      vertex   -8.511186e-01 -9.000000e-02 -9.055636e-01
      vertex   -1.007362e+00 -3.590000e+00 -5.989185e-01
      vertex   -8.511186e-01 -3.590000e+00 -9.055636e-01
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   -8.511186e-01 -9.000000e-02 -9.055636e-01
      vertex   -8.511186e-01 -3.590000e+00 -9.055636e-01
      vertex   -6.077637e-01 -9.000000e-02 -1.148919e+00
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   -6.077637e-01 -9.000000e-02 -1.148919e+00
      vertex   -8.511186e-01 -3.590000e+00 -9.055636e-01
      vertex   -6.077637e-01 -3.590000e+00 -1.148919e+00
    endloop
  endfacet
  facet normal 4.539905e-01 0.000000e+00 8.910065e-01
    outer loop
      vertex   -6.077637e-01 -9.000000e-02 -1.148919e+00
      vertex   -6.077637e-01 -3.590000e+00 -1.148919e+00
      vertex   -3.011186e-01 -9.000000e-02 -1.305162e+00
    endloop
  endfacet
  facet normal 4.539905e-01 0.000000e+00 8.910065e-01
    outer loop
      vertex   -3.011186e-01 -9.000000e-02 -1.305162e+00
      vertex   -6.077637e-01 -3.590000e+00 -1.148919e+00
      vertex   -3.011186e-01 -3.590000e+00 -1.305162e+00
    endloop
  endfacet
  facet normal 1.564345e-01 0.000000e+00 9.876883e-01
    outer loop
      vertex   -3.011186e-01 -9.000000e-02 -1.305162e+00
      vertex   -3.011186e-01 -3.590000e+00 -1.305162e+00
      vertex   3.880009e-02 -9.000000e-02 -1.359000e+00
    endloop
  endfacet
  facet normal 1.564345e-01 0.000000e+00 9.876883e-01
    outer loop
      vertex   3.880009e-02 -9.000000e-02 -1.359000e+00
      vertex   -3.011186e-01 -3.590000e+00 -1.305162e+00
      vertex   3.880009e-02 -3.590000e+00 -1.359000e+00
    endloop
  endfacet
  facet normal -1.564345e-01 0.000000e+00 9.876883e-01
    outer loop
      vertex   3.880009e-02 -9.000000e-02 -1.359000e+00
      vertex   3.880009e-02 -3.590000e+00 -1.359000e+00
      vertex   3.787188e-01 -9.000000e-02 -1.305162e+00
    endloop
  endfacet
  facet normal -1.564345e-01 0.000000e+00 9.876883e-01
    outer loop
      vertex   3.787188e-01 -9.000000e-02 -1.305162e+00
      vertex   3.880009e-02 -3.590000e+00 -1.359000e+00
      vertex   3.787188e-01 -3.590000e+00 -1.305162e+00
    endloop
  endfacet
  facet normal -4.539905e-01 0.000000e+00 8.910065e-01
    outer loop
      vertex   3.787188e-01 -9.000000e-02 -1.305162e+00
      vertex   3.787188e-01 -3.590000e+00 -1.305162e+00
      vertex   6.853639e-01 -9.000000e-02 -1.148919e+00
    endloop
  endfacet
  facet normal -4.539905e-01 0.000000e+00 8.910065e-01
    outer loop
      vertex   6.853639e-01 -9.000000e-02 -1.148919e+00
      vertex   3.787188e-01 -3.590000e+00 -1.305162e+00
      vertex   6.853639e-01 -3.590000e+00 -1.148919e+00
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   6.853639e-01 -9.000000e-02 -1.148919e+00
      vertex   6.853639e-01 -3.590000e+00 -1.148919e+00
      vertex   9.287188e-01 -9.000000e-02 -9.055636e-01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   9.287188e-01 -9.000000e-02 -9.055636e-01
      vertex   6.853639e-01 -3.590000e+00 -1.148919e+00
      vertex   9.287188e-01 -3.590000e+00 -9.055636e-01
    endloop
  endfacet
  facet normal -8.910065e-01 0.000000e+00 4.539905e-01
    outer loop
      vertex   9.287188e-01 -9.000000e-02 -9.055636e-01
      vertex   9.287188e-01 -3.590000e+00 -9.055636e-01
      vertex   1.084962e+00 -9.000000e-02 -5.989185e-01
    endloop
  endfacet
  facet normal -8.910065e-01 0.000000e+00 4.539905e-01
    outer loop
      vertex   1.084962e+00 -9.000000e-02 -5.989185e-01
      vertex   9.287188e-01 -3.590000e+00 -9.055636e-01
      vertex   1.084962e+00 -3.590000e+00 -5.989185e-01
    endloop
  endfacet
  facet normal -9.876883e-01 0.000000e+00 1.564345e-01
    outer loop
      vertex   1.084962e+00 -9.000000e-02 -5.989185e-01
      vertex   1.084962e+00 -3.590000e+00 -5.989185e-01
      vertex   1.138800e+00 -9.000000e-02 -2.589998e-01
    endloop
  endfacet
  facet normal -9.876883e-01 0.000000e+00 1.564345e-01
    outer loop
      vertex   1.138800e+00 -9.000000e-02 -2.589998e-01
      vertex   1.084962e+00 -3.590000e+00 -5.989185e-01
      vertex   1.138800e+00 -3.590000e+00 -2.589998e-01
    endloop
  endfacet
  facet normal -9.876883e-01 -0.000000e+00 -1.564345e-01
    outer loop
      vertex   1.138800e+00 -9.000000e-02 -2.589998e-01
      vertex   1.138800e+00 -3.590000e+00 -2.589998e-01
      vertex   1.084962e+00 -9.000000e-02 8.091887e-02
    endloop
  endfacet
  facet normal -9.876883e-01 -0.000000e+00 -1.564345e-01
    outer loop
      vertex   1.084962e+00 -9.000000e-02 8.091887e-02
      vertex   1.138800e+00 -3.590000e+00 -2.589998e-01
      vertex   1.084962e+00 -3.590000e+00 8.091887e-02
    endloop
  endfacet
  facet normal -8.910065e-01 -0.000000e+00 -4.539905e-01
    outer loop
      vertex   1.084962e+00 -9.000000e-02 8.091887e-02
      vertex   1.084962e+00 -3.590000e+00 8.091887e-02
      vertex   9.287188e-01 -9.000000e-02 3.875640e-01
    endloop
  endfacet
  facet normal -8.910065e-01 -0.000000e+00 -4.539905e-01
    outer loop
      vertex   9.287188e-01 -9.000000e-02 3.875640e-01
      vertex   1.084962e+00 -3.590000e+00 8.091887e-02
      vertex   9.287188e-01 -3.590000e+00 3.875640e-01
    endloop
  endfacet
  facet normal -7.071068e-01 -0.000000e+00 -7.071068e-01
    outer loop
      vertex   9.287188e-01 -9.000000e-02 3.875640e-01
      vertex   9.287188e-01 -3.590000e+00 3.875640e-01
      vertex   6.853639e-01 -9.000000e-02 6.309189e-01
    endloop
  endfacet
  facet normal -7.071068e-01 -0.000000e+00 -7.071068e-01
    outer loop
      vertex   6.853639e-01 -9.000000e-02 6.309189e-01
      vertex   9.287188e-01 -3.590000e+00 3.875640e-01
      vertex   6.853639e-01 -3.590000e+00 6.309189e-01
    endloop
  endfacet
  facet normal -4.539905e-01 -0.000000e+00 -8.910065e-01
    outer loop
      vertex   6.853639e-01 -9.000000e-02 6.309189e-01
      vertex   6.853639e-01 -3.590000e+00 6.309189e-01
      vertex   3.787188e-01 -9.000000e-02 7.871623e-01
    endloop
  endfacet
  facet normal -4.539905e-01 -0.000000e+00 -8.910065e-01
    outer loop
      vertex   3.787188e-01 -9.000000e-02 7.871623e-01
      vertex   6.853639e-01 -3.590000e+00 6.309189e-01
      vertex   3.787188e-01 -3.590000e+00 7.871623e-01
    endloop
  endfacet
  facet normal -1.564345e-01 -0.000000e+00 -9.876883e-01
    outer loop
      vertex   3.787188e-01 -9.000000e-02 7.871623e-01
      vertex   3.787188e-01 -3.590000e+00 7.871623e-01
      vertex   3.880009e-02 -9.000000e-02 8.410002e-01
    endloop
  endfacet
  facet normal -1.564345e-01 -0.000000e+00 -9.876883e-01
    outer loop
      vertex   3.880009e-02 -9.000000e-02 8.410002e-01
      vertex   3.787188e-01 -3.590000e+00 7.871623e-01
      vertex   3.880009e-02 -3.590000e+00 8.410002e-01
    endloop
  endfacet
  facet normal 1.564345e-01 0.000000e+00 -9.876883e-01
    outer loop
      vertex   3.880009e-02 -9.000000e-02 8.410002e-01
      vertex   3.880009e-02 -3.590000e+00 8.410002e-01
      vertex   -3.011186e-01 -9.000000e-02 7.871623e-01
    endloop
  endfacet
  facet normal 1.564345e-01 0.000000e+00 -9.876883e-01
    outer loop
      vertex   -3.011186e-01 -9.000000e-02 7.871623e-01
      vertex   3.880009e-02 -3.590000e+00 8.410002e-01
      vertex   -3.011186e-01 -3.590000e+00 7.871623e-01
    endloop
  endfacet
  facet normal 4.539905e-01 0.000000e+00 -8.910065e-01
    outer loop
      vertex   -3.011186e-01 -9.000000e-02 7.871623e-01
      vertex   -3.011186e-01 -3.590000e+00 7.871623e-01
      vertex   -6.077637e-01 -9.000000e-02 6.309189e-01
    endloop
  endfacet
  facet normal 4.539905e-01 0.000000e+00 -8.910065e-01
    outer loop
      vertex   -6.077637e-01 -9.000000e-02 6.309189e-01
      vertex   -3.011186e-01 -3.590000e+00 7.871623e-01
      vertex   -6.077637e-01 -3.590000e+00 6.309189e-01
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   -6.077637e-01 -9.000000e-02 6.309189e-01
      vertex   -6.077637e-01 -3.590000e+00 6.309189e-01
      vertex   -8.511186e-01 -9.000000e-02 3.875640e-01
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   -8.511186e-01 -9.000000e-02 3.875640e-01
      vertex   -6.077637e-01 -3.590000e+00 6.309189e-01
      vertex   -8.511186e-01 -3.590000e+00 3.875640e-01
    endloop
  endfacet
  facet normal 8.910065e-01 0.000000e+00 -4.539905e-01
    outer loop
      vertex   -8.511186e-01 -9.000000e-02 3.875640e-01
      vertex   -8.511186e-01 -3.590000e+00 3.875640e-01
      vertex   -1.007362e+00 -9.000000e-02 8.091887e-02
    endloop
  endfacet
  facet normal 8.910065e-01 0.000000e+00 -4.539905e-01
    outer loop
      vertex   -1.007362e+00 -9.000000e-02 8.091887e-02
      vertex   -8.511186e-01 -3.590000e+00 3.875640e-01
      vertex   -1.007362e+00 -3.590000e+00 8.091887e-02
    endloop
  endfacet
  facet normal -9.951847e-01 0.000000e+00 -9.801714e-02
    outer loop
      vertex   -1.200000e+01 -3.590000e+00 -9.500000e+00
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.195196e+01 -3.590000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal -9.951847e-01 0.000000e+00 -9.801714e-02
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.195196e+01 -9.000000e-02 -9.987726e+00
    endloop
  endfacet
  facet normal -9.569403e-01 0.000000e+00 -2.902847e-01
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 -9.987726e+00
      vertex   -1.195196e+01 -9.000000e-02 -9.987726e+00
      vertex   -1.180970e+01 -3.590000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal -9.569403e-01 0.000000e+00 -2.902847e-01
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   -1.195196e+01 -9.000000e-02 -9.987726e+00
      vertex   -1.180970e+01 -9.000000e-02 -1.045671e+01
    endloop
  endfacet
  facet normal -8.819213e-01 0.000000e+00 -4.713967e-01
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 -1.045671e+01
      vertex   -1.180970e+01 -9.000000e-02 -1.045671e+01
      vertex   -1.157867e+01 -3.590000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal -8.819213e-01 0.000000e+00 -4.713967e-01
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   -1.180970e+01 -9.000000e-02 -1.045671e+01
      vertex   -1.157867e+01 -9.000000e-02 -1.088893e+01
    endloop
  endfacet
  facet normal -7.730105e-01 0.000000e+00 -6.343933e-01
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 -1.088893e+01
      vertex   -1.157867e+01 -9.000000e-02 -1.088893e+01
      vertex   -1.126777e+01 -3.590000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal -7.730105e-01 0.000000e+00 -6.343933e-01
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   -1.157867e+01 -9.000000e-02 -1.088893e+01
      vertex   -1.126777e+01 -9.000000e-02 -1.126777e+01
    endloop
  endfacet
  facet normal -6.343933e-01 0.000000e+00 -7.730105e-01
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 -1.126777e+01
      vertex   -1.126777e+01 -9.000000e-02 -1.126777e+01
      vertex   -1.088893e+01 -3.590000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal -6.343933e-01 0.000000e+00 -7.730105e-01
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   -1.126777e+01 -9.000000e-02 -1.126777e+01
      vertex   -1.088893e+01 -9.000000e-02 -1.157867e+01
    endloop
  endfacet
  facet normal -4.713967e-01 0.000000e+00 -8.819213e-01
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 -1.157867e+01
      vertex   -1.088893e+01 -9.000000e-02 -1.157867e+01
      vertex   -1.045671e+01 -3.590000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal -4.713967e-01 0.000000e+00 -8.819213e-01
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   -1.088893e+01 -9.000000e-02 -1.157867e+01
      vertex   -1.045671e+01 -9.000000e-02 -1.180970e+01
    endloop
  endfacet
  facet normal -2.902847e-01 0.000000e+00 -9.569403e-01
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 -1.180970e+01
      vertex   -1.045671e+01 -9.000000e-02 -1.180970e+01
      vertex   -9.987726e+00 -3.590000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal -2.902847e-01 0.000000e+00 -9.569403e-01
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   -1.045671e+01 -9.000000e-02 -1.180970e+01
      vertex   -9.987726e+00 -9.000000e-02 -1.195196e+01
    endloop
  endfacet
  facet normal -9.801714e-02 0.000000e+00 -9.951847e-01
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 -1.195196e+01
      vertex   -9.987726e+00 -9.000000e-02 -1.195196e+01
      vertex   -9.500000e+00 -3.590000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -9.801714e-02 0.000000e+00 -9.951847e-01
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 -1.200000e+01
      vertex   -9.987726e+00 -9.000000e-02 -1.195196e+01
      vertex   -9.500000e+00 -9.000000e-02 -1.200000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 4.674623e-16
    outer loop
      vertex   -1.200000e+01 -9.000000e-02 9.500000e+00
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.200000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 4.674623e-16
    outer loop
      vertex   -1.200000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.200000e+01 -9.000000e-02 -9.500000e+00
      vertex   -1.200000e+01 -3.590000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -9.801714e-02 0.000000e+00 9.951847e-01
    outer loop
      vertex   -9.500000e+00 -3.590000e+00 1.200000e+01
      vertex   -9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   -9.987726e+00 -3.590000e+00 1.195196e+01
    endloop
  endfacet
  facet normal -9.801714e-02 0.000000e+00 9.951847e-01
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   -9.500000e+00 -9.000000e-02 1.200000e+01
      vertex   -9.987726e+00 -9.000000e-02 1.195196e+01
    endloop
  endfacet
  facet normal -2.902847e-01 0.000000e+00 9.569403e-01
    outer loop
      vertex   -9.987726e+00 -3.590000e+00 1.195196e+01
      vertex   -9.987726e+00 -9.000000e-02 1.195196e+01
      vertex   -1.045671e+01 -3.590000e+00 1.180970e+01
    endloop
  endfacet
  facet normal -2.902847e-01 0.000000e+00 9.569403e-01
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   -9.987726e+00 -9.000000e-02 1.195196e+01
      vertex   -1.045671e+01 -9.000000e-02 1.180970e+01
    endloop
  endfacet
  facet normal -4.713967e-01 0.000000e+00 8.819213e-01
    outer loop
      vertex   -1.045671e+01 -3.590000e+00 1.180970e+01
      vertex   -1.045671e+01 -9.000000e-02 1.180970e+01
      vertex   -1.088893e+01 -3.590000e+00 1.157867e+01
    endloop
  endfacet
  facet normal -4.713967e-01 0.000000e+00 8.819213e-01
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   -1.045671e+01 -9.000000e-02 1.180970e+01
      vertex   -1.088893e+01 -9.000000e-02 1.157867e+01
    endloop
  endfacet
  facet normal -6.343933e-01 0.000000e+00 7.730105e-01
    outer loop
      vertex   -1.088893e+01 -3.590000e+00 1.157867e+01
      vertex   -1.088893e+01 -9.000000e-02 1.157867e+01
      vertex   -1.126777e+01 -3.590000e+00 1.126777e+01
    endloop
  endfacet
  facet normal -6.343933e-01 0.000000e+00 7.730105e-01
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   -1.088893e+01 -9.000000e-02 1.157867e+01
      vertex   -1.126777e+01 -9.000000e-02 1.126777e+01
    endloop
  endfacet
  facet normal -7.730105e-01 0.000000e+00 6.343933e-01
    outer loop
      vertex   -1.126777e+01 -3.590000e+00 1.126777e+01
      vertex   -1.126777e+01 -9.000000e-02 1.126777e+01
      vertex   -1.157867e+01 -3.590000e+00 1.088893e+01
    endloop
  endfacet
  facet normal -7.730105e-01 0.000000e+00 6.343933e-01
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   -1.126777e+01 -9.000000e-02 1.126777e+01
      vertex   -1.157867e+01 -9.000000e-02 1.088893e+01
    endloop
  endfacet
  facet normal -8.819213e-01 0.000000e+00 4.713967e-01
    outer loop
      vertex   -1.157867e+01 -3.590000e+00 1.088893e+01
      vertex   -1.157867e+01 -9.000000e-02 1.088893e+01
      vertex   -1.180970e+01 -3.590000e+00 1.045671e+01
    endloop
  endfacet
  facet normal -8.819213e-01 0.000000e+00 4.713967e-01
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   -1.157867e+01 -9.000000e-02 1.088893e+01
      vertex   -1.180970e+01 -9.000000e-02 1.045671e+01
    endloop
  endfacet
  facet normal -9.569403e-01 0.000000e+00 2.902847e-01
    outer loop
      vertex   -1.180970e+01 -3.590000e+00 1.045671e+01
      vertex   -1.180970e+01 -9.000000e-02 1.045671e+01
      vertex   -1.195196e+01 -3.590000e+00 9.987726e+00
    endloop
  endfacet
  facet normal -9.569403e-01 0.000000e+00 2.902847e-01
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   -1.180970e+01 -9.000000e-02 1.045671e+01
      vertex   -1.195196e+01 -9.000000e-02 9.987726e+00
    endloop
  endfacet
  facet normal -9.951847e-01 0.000000e+00 9.801714e-02
    outer loop
      vertex   -1.195196e+01 -3.590000e+00 9.987726e+00
      vertex   -1.195196e+01 -9.000000e-02 9.987726e+00
      vertex   -1.200000e+01 -3.590000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -9.951847e-01 0.000000e+00 9.801714e-02
    outer loop
      vertex   -1.200000e+01 -3.590000e+00 9.500000e+00
      vertex   -1.195196e+01 -9.000000e-02 9.987726e+00
      vertex   -1.200000e+01 -9.000000e-02 9.500000e+00
    endloop
  endfacet
endsolid

```

#### Top

```stl
solid ASCII
  facet normal 0.000000e+00 -9.523198e-01 3.051016e-01
    outer loop
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   9.500000e+00 -1.119781e+01 1.150684e+01
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal -1.731403e-04 -8.571656e-01 5.150408e-01
    outer loop
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   9.500000e+00 -1.119781e+01 1.150684e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
    endloop
  endfacet
  facet normal -3.587135e-04 -8.125102e-01 5.829468e-01
    outer loop
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   2.374770e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.877671e-01 6.159732e-01
    outer loop
      vertex   2.374770e+00 -1.115203e+01 1.156831e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   3.562263e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   2.374770e+00 -1.115203e+01 1.156831e+01
      vertex   3.562263e+00 -1.115203e+01 1.156831e+01
      vertex   3.562263e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   3.562263e+00 -1.107542e+01 1.165394e+01
      vertex   3.562263e+00 -1.115203e+01 1.156831e+01
      vertex   4.750005e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   3.562263e+00 -1.107542e+01 1.165394e+01
      vertex   4.750005e+00 -1.107542e+01 1.165394e+01
      vertex   4.750005e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal -2.150425e-15 -7.186833e-01 6.953375e-01
    outer loop
      vertex   4.750005e+00 -1.096651e+01 1.176651e+01
      vertex   4.750005e+00 -1.107542e+01 1.165394e+01
      vertex   5.937340e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal -2.080571e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   4.750005e+00 -1.096651e+01 1.176651e+01
      vertex   5.937340e+00 -1.096651e+01 1.176651e+01
      vertex   5.937340e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 4.162923e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   5.937340e+00 -1.085394e+01 1.187542e+01
      vertex   5.937340e+00 -1.096651e+01 1.176651e+01
      vertex   6.530754e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 3.992029e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   5.937340e+00 -1.085394e+01 1.187542e+01
      vertex   6.530754e+00 -1.085394e+01 1.187542e+01
      vertex   6.530754e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   6.530754e+00 -1.076831e+01 1.195203e+01
      vertex   6.530754e+00 -1.085394e+01 1.187542e+01
      vertex   7.124155e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.746246e-01 8.184171e-01
    outer loop
      vertex   6.530754e+00 -1.076831e+01 1.195203e+01
      vertex   7.124155e+00 -1.076831e+01 1.195203e+01
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.746246e-01 8.184171e-01
    outer loop
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   7.124155e+00 -1.076831e+01 1.195203e+01
      vertex   7.717663e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal -1.393263e-02 -3.050720e-01 9.522274e-01
    outer loop
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   7.717663e+00 -1.076831e+01 1.195203e+01
      vertex   9.500000e+00 -1.070684e+01 1.199781e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.972248e-01 8.020739e-01
    outer loop
      vertex   9.500000e+00 -1.070684e+01 1.199781e+01
      vertex   7.717663e+00 -1.076831e+01 1.195203e+01
      vertex   8.311394e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal -6.371919e-03 -5.150304e-01 8.571482e-01
    outer loop
      vertex   9.500000e+00 -1.070684e+01 1.199781e+01
      vertex   8.311394e+00 -1.076831e+01 1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 1.199019e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.159732e-01 7.877671e-01
    outer loop
      vertex   9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   8.311394e+00 -1.076831e+01 1.195203e+01
      vertex   8.905467e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 6.034636e-15 -6.159732e-01 7.877671e-01
    outer loop
      vertex   9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   8.905467e+00 -1.076831e+01 1.195203e+01
      vertex   9.500000e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 6.211164e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   8.905467e+00 -1.076831e+01 1.195203e+01
      vertex   8.905467e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 4.228096e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   8.905467e+00 -1.085394e+01 1.187542e+01
      vertex   9.500000e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 4.224838e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   8.905467e+00 -1.085394e+01 1.187542e+01
      vertex   8.905467e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 2.086420e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   8.905467e+00 -1.096651e+01 1.176651e+01
      vertex   9.500000e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 2.147295e-15 -7.186833e-01 6.953375e-01
    outer loop
      vertex   9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   8.905467e+00 -1.096651e+01 1.176651e+01
      vertex   8.905467e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 4.228726e-15 -7.186833e-01 6.953375e-01
    outer loop
      vertex   9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   8.905467e+00 -1.107542e+01 1.165394e+01
      vertex   9.500000e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 4.218907e-15 -7.452430e-01 6.667929e-01
    outer loop
      vertex   9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   8.905467e+00 -1.107542e+01 1.165394e+01
      vertex   8.905467e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 8.202252e-15 -7.452430e-01 6.667929e-01
    outer loop
      vertex   9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   8.905467e+00 -1.115203e+01 1.156831e+01
      vertex   9.500000e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 7.874953e-15 -7.877671e-01 6.159732e-01
    outer loop
      vertex   9.500000e+00 -1.115203e+01 1.156831e+01
      vertex   8.905467e+00 -1.115203e+01 1.156831e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.877671e-01 6.159732e-01
    outer loop
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   8.905467e+00 -1.115203e+01 1.156831e+01
      vertex   8.311394e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.877671e-01 6.159732e-01
    outer loop
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   8.311394e+00 -1.115203e+01 1.156831e+01
      vertex   7.717663e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   7.717663e+00 -1.115203e+01 1.156831e+01
      vertex   8.311394e+00 -1.115203e+01 1.156831e+01
      vertex   8.311394e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   7.717663e+00 -1.115203e+01 1.156831e+01
      vertex   8.311394e+00 -1.107542e+01 1.165394e+01
      vertex   7.717663e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   7.717663e+00 -1.107542e+01 1.165394e+01
      vertex   8.311394e+00 -1.107542e+01 1.165394e+01
      vertex   8.311394e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   7.717663e+00 -1.107542e+01 1.165394e+01
      vertex   8.311394e+00 -1.096651e+01 1.176651e+01
      vertex   7.717663e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   7.717663e+00 -1.096651e+01 1.176651e+01
      vertex   8.311394e+00 -1.096651e+01 1.176651e+01
      vertex   8.311394e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   7.717663e+00 -1.096651e+01 1.176651e+01
      vertex   8.311394e+00 -1.085394e+01 1.187542e+01
      vertex   7.717663e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   7.717663e+00 -1.085394e+01 1.187542e+01
      vertex   8.311394e+00 -1.085394e+01 1.187542e+01
      vertex   8.311394e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   7.717663e+00 -1.085394e+01 1.187542e+01
      vertex   8.311394e+00 -1.076831e+01 1.195203e+01
      vertex   7.717663e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.746246e-01 8.184171e-01
    outer loop
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   4.750005e+00 -1.076831e+01 1.195203e+01
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal -3.671288e-15 -5.746246e-01 8.184171e-01
    outer loop
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   4.750005e+00 -1.076831e+01 1.195203e+01
      vertex   5.937340e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 7.345720e-15 -5.746246e-01 8.184171e-01
    outer loop
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   5.937340e+00 -1.076831e+01 1.195203e+01
      vertex   6.530754e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 6.692555e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   6.530754e+00 -1.076831e+01 1.195203e+01
      vertex   5.937340e+00 -1.076831e+01 1.195203e+01
      vertex   5.937340e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -1.140987e-16 -3.051016e-01 9.523198e-01
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   -9.500000e+00 -1.070684e+01 1.199781e+01
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal 1.731399e-04 -5.150408e-01 8.571656e-01
    outer loop
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   -9.500000e+00 -1.070684e+01 1.199781e+01
      vertex   -9.500000e+00 -1.071951e+01 1.199019e+01
    endloop
  endfacet
  facet normal 3.587127e-04 -5.829468e-01 8.125102e-01
    outer loop
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   -9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   -2.374759e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 1.306772e-15 -6.159732e-01 7.877671e-01
    outer loop
      vertex   -2.374759e+00 -1.076831e+01 1.195203e+01
      vertex   -9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   -4.749985e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 1.173358e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   -2.374759e+00 -1.076831e+01 1.195203e+01
      vertex   -4.749985e+00 -1.076831e+01 1.195203e+01
      vertex   -4.749985e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -1.584172e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   -4.749985e+00 -1.085394e+01 1.187542e+01
      vertex   -4.749985e+00 -1.076831e+01 1.195203e+01
      vertex   -9.500000e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -1.586398e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   -4.749985e+00 -1.085394e+01 1.187542e+01
      vertex   -9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   -9.500000e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal -1.408952e-15 -6.159732e-01 7.877671e-01
    outer loop
      vertex   -9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   -9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   -4.749985e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal -1.364150e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   -4.749985e+00 -1.076831e+01 1.195203e+01
      vertex   -9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   -9.500000e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -2.588139e-16 -6.953375e-01 7.186833e-01
    outer loop
      vertex   -4.749985e+00 -1.085394e+01 1.187542e+01
      vertex   -9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   -4.749985e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal -2.687650e-16 -7.186833e-01 6.953375e-01
    outer loop
      vertex   -4.749985e+00 -1.096651e+01 1.176651e+01
      vertex   -9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   -9.500000e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal -5.292862e-16 -7.186833e-01 6.953375e-01
    outer loop
      vertex   -4.749985e+00 -1.096651e+01 1.176651e+01
      vertex   -9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   -4.749985e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal -5.280572e-16 -7.452430e-01 6.667929e-01
    outer loop
      vertex   -4.749985e+00 -1.107542e+01 1.165394e+01
      vertex   -9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   -9.500000e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal -1.026630e-15 -7.452430e-01 6.667929e-01
    outer loop
      vertex   -4.749985e+00 -1.107542e+01 1.165394e+01
      vertex   -9.500000e+00 -1.115203e+01 1.156831e+01
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal -9.856642e-16 -7.877671e-01 6.159732e-01
    outer loop
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
      vertex   -9.500000e+00 -1.115203e+01 1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 1.151951e+01
    endloop
  endfacet
  facet normal 1.594489e-03 -8.571645e-01 5.150402e-01
    outer loop
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   -9.500000e+00 -1.119781e+01 1.150684e+01
    endloop
  endfacet
  facet normal 5.228347e-03 -9.523068e-01 3.050974e-01
    outer loop
      vertex   -9.500000e+00 -1.119781e+01 1.150684e+01
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -8.184171e-01 5.746246e-01
    outer loop
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -8.184171e-01 5.746246e-01
    outer loop
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   -2.374759e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -8.184171e-01 5.746246e-01
    outer loop
      vertex   -2.374759e+00 -1.115203e+01 1.156831e+01
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   1.154595e-05 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   -2.374759e+00 -1.115203e+01 1.156831e+01
      vertex   1.154595e-05 -1.115203e+01 1.156831e+01
      vertex   1.154595e-05 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   1.154595e-05 -1.107542e+01 1.165394e+01
      vertex   1.154595e-05 -1.115203e+01 1.156831e+01
      vertex   2.374770e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   1.154595e-05 -1.107542e+01 1.165394e+01
      vertex   2.374770e+00 -1.107542e+01 1.165394e+01
      vertex   2.374770e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   2.374770e+00 -1.096651e+01 1.176651e+01
      vertex   2.374770e+00 -1.107542e+01 1.165394e+01
      vertex   3.562263e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   2.374770e+00 -1.096651e+01 1.176651e+01
      vertex   3.562263e+00 -1.096651e+01 1.176651e+01
      vertex   3.562263e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   3.562263e+00 -1.085394e+01 1.187542e+01
      vertex   3.562263e+00 -1.096651e+01 1.176651e+01
      vertex   4.750005e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   3.562263e+00 -1.085394e+01 1.187542e+01
      vertex   4.750005e+00 -1.085394e+01 1.187542e+01
      vertex   4.750005e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal -3.344845e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   4.750005e+00 -1.076831e+01 1.195203e+01
      vertex   4.750005e+00 -1.085394e+01 1.187542e+01
      vertex   5.937340e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.877671e-01 6.159732e-01
    outer loop
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   7.124155e+00 -1.115203e+01 1.156831e+01
      vertex   6.530754e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   6.530754e+00 -1.115203e+01 1.156831e+01
      vertex   7.124155e+00 -1.115203e+01 1.156831e+01
      vertex   7.124155e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   6.530754e+00 -1.115203e+01 1.156831e+01
      vertex   7.124155e+00 -1.107542e+01 1.165394e+01
      vertex   6.530754e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   6.530754e+00 -1.107542e+01 1.165394e+01
      vertex   7.124155e+00 -1.107542e+01 1.165394e+01
      vertex   7.124155e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   6.530754e+00 -1.107542e+01 1.165394e+01
      vertex   7.124155e+00 -1.096651e+01 1.176651e+01
      vertex   6.530754e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   6.530754e+00 -1.096651e+01 1.176651e+01
      vertex   7.124155e+00 -1.096651e+01 1.176651e+01
      vertex   7.124155e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   6.530754e+00 -1.096651e+01 1.176651e+01
      vertex   7.124155e+00 -1.085394e+01 1.187542e+01
      vertex   6.530754e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   6.530754e+00 -1.085394e+01 1.187542e+01
      vertex   7.124155e+00 -1.085394e+01 1.187542e+01
      vertex   7.124155e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 2.353524e-15 -7.877671e-01 6.159732e-01
    outer loop
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   6.530754e+00 -1.115203e+01 1.156831e+01
      vertex   5.937340e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 2.230852e-15 -7.452430e-01 6.667929e-01
    outer loop
      vertex   5.937340e+00 -1.115203e+01 1.156831e+01
      vertex   6.530754e+00 -1.115203e+01 1.156831e+01
      vertex   6.530754e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 6.220539e-15 -7.452430e-01 6.667929e-01
    outer loop
      vertex   5.937340e+00 -1.115203e+01 1.156831e+01
      vertex   6.530754e+00 -1.107542e+01 1.165394e+01
      vertex   5.937340e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 6.314270e-15 -7.186833e-01 6.953375e-01
    outer loop
      vertex   5.937340e+00 -1.107542e+01 1.165394e+01
      vertex   6.530754e+00 -1.107542e+01 1.165394e+01
      vertex   6.530754e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 2.146348e-15 -7.186833e-01 6.953375e-01
    outer loop
      vertex   5.937340e+00 -1.107542e+01 1.165394e+01
      vertex   6.530754e+00 -1.096651e+01 1.176651e+01
      vertex   5.937340e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 2.081462e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   5.937340e+00 -1.096651e+01 1.176651e+01
      vertex   6.530754e+00 -1.096651e+01 1.176651e+01
      vertex   6.530754e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -8.184171e-01 5.746246e-01
    outer loop
      vertex   1.154595e-05 -1.115203e+01 1.156831e+01
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   2.374770e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.746246e-01 8.184171e-01
    outer loop
      vertex   3.562263e+00 -1.076831e+01 1.195203e+01
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   2.374770e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.746246e-01 8.184171e-01
    outer loop
      vertex   2.374770e+00 -1.076831e+01 1.195203e+01
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   1.154595e-05 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   2.374770e+00 -1.076831e+01 1.195203e+01
      vertex   1.154595e-05 -1.076831e+01 1.195203e+01
      vertex   1.154595e-05 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   1.154595e-05 -1.085394e+01 1.187542e+01
      vertex   1.154595e-05 -1.076831e+01 1.195203e+01
      vertex   -2.374759e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   1.154595e-05 -1.085394e+01 1.187542e+01
      vertex   -2.374759e+00 -1.085394e+01 1.187542e+01
      vertex   -2.374759e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 5.200211e-16 -6.953375e-01 7.186833e-01
    outer loop
      vertex   -2.374759e+00 -1.096651e+01 1.176651e+01
      vertex   -2.374759e+00 -1.085394e+01 1.187542e+01
      vertex   -4.749985e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 5.374807e-16 -7.186833e-01 6.953375e-01
    outer loop
      vertex   -2.374759e+00 -1.096651e+01 1.176651e+01
      vertex   -4.749985e+00 -1.096651e+01 1.176651e+01
      vertex   -4.749985e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   8.311394e+00 -1.076831e+01 1.195203e+01
      vertex   8.311394e+00 -1.085394e+01 1.187542e+01
      vertex   8.905467e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   8.905467e+00 -1.076831e+01 1.195203e+01
      vertex   8.311394e+00 -1.085394e+01 1.187542e+01
      vertex   8.905467e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   8.311394e+00 -1.085394e+01 1.187542e+01
      vertex   8.311394e+00 -1.096651e+01 1.176651e+01
      vertex   8.905467e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   8.905467e+00 -1.085394e+01 1.187542e+01
      vertex   8.311394e+00 -1.096651e+01 1.176651e+01
      vertex   8.905467e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   8.311394e+00 -1.115203e+01 1.156831e+01
      vertex   8.905467e+00 -1.115203e+01 1.156831e+01
      vertex   8.905467e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   8.311394e+00 -1.096651e+01 1.176651e+01
      vertex   8.311394e+00 -1.107542e+01 1.165394e+01
      vertex   8.905467e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   8.905467e+00 -1.096651e+01 1.176651e+01
      vertex   8.311394e+00 -1.107542e+01 1.165394e+01
      vertex   8.905467e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.877671e-01 6.159732e-01
    outer loop
      vertex   7.124155e+00 -1.115203e+01 1.156831e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   7.717663e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   8.311394e+00 -1.107542e+01 1.165394e+01
      vertex   8.311394e+00 -1.115203e+01 1.156831e+01
      vertex   8.905467e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.746246e-01 8.184171e-01
    outer loop
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   -2.374759e+00 -1.076831e+01 1.195203e+01
      vertex   1.154595e-05 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   1.154595e-05 -1.076831e+01 1.195203e+01
      vertex   -2.374759e+00 -1.076831e+01 1.195203e+01
      vertex   -2.374759e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 2.112287e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   -4.749985e+00 -1.096651e+01 1.176651e+01
      vertex   -2.374759e+00 -1.085394e+01 1.187542e+01
      vertex   -4.749985e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 2.112035e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   -4.749985e+00 -1.085394e+01 1.187542e+01
      vertex   -2.374759e+00 -1.085394e+01 1.187542e+01
      vertex   -2.374759e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   -2.374759e+00 -1.096651e+01 1.176651e+01
      vertex   -2.374759e+00 -1.107542e+01 1.165394e+01
      vertex   1.154595e-05 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   1.154595e-05 -1.096651e+01 1.176651e+01
      vertex   -2.374759e+00 -1.107542e+01 1.165394e+01
      vertex   1.154595e-05 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   1.154595e-05 -1.096651e+01 1.176651e+01
      vertex   1.154595e-05 -1.107542e+01 1.165394e+01
      vertex   2.374770e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
      vertex   -2.374759e+00 -1.115203e+01 1.156831e+01
      vertex   -2.374759e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   -2.374759e+00 -1.107542e+01 1.165394e+01
      vertex   -2.374759e+00 -1.115203e+01 1.156831e+01
      vertex   1.154595e-05 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   -4.749985e+00 -1.115203e+01 1.156831e+01
      vertex   -2.374759e+00 -1.107542e+01 1.165394e+01
      vertex   -4.749985e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   -4.749985e+00 -1.107542e+01 1.165394e+01
      vertex   -2.374759e+00 -1.107542e+01 1.165394e+01
      vertex   -2.374759e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   2.374770e+00 -1.107542e+01 1.165394e+01
      vertex   1.154595e-05 -1.115203e+01 1.156831e+01
      vertex   2.374770e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   -2.374759e+00 -1.096651e+01 1.176651e+01
      vertex   1.154595e-05 -1.096651e+01 1.176651e+01
      vertex   1.154595e-05 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   1.154595e-05 -1.085394e+01 1.187542e+01
      vertex   1.154595e-05 -1.096651e+01 1.176651e+01
      vertex   2.374770e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   1.154595e-05 -1.085394e+01 1.187542e+01
      vertex   2.374770e+00 -1.085394e+01 1.187542e+01
      vertex   2.374770e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   2.374770e+00 -1.076831e+01 1.195203e+01
      vertex   2.374770e+00 -1.085394e+01 1.187542e+01
      vertex   3.562263e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   2.374770e+00 -1.085394e+01 1.187542e+01
      vertex   1.154595e-05 -1.096651e+01 1.176651e+01
      vertex   2.374770e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   3.562263e+00 -1.096651e+01 1.176651e+01
      vertex   2.374770e+00 -1.107542e+01 1.165394e+01
      vertex   3.562263e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   3.562263e+00 -1.107542e+01 1.165394e+01
      vertex   2.374770e+00 -1.107542e+01 1.165394e+01
      vertex   2.374770e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   3.562263e+00 -1.076831e+01 1.195203e+01
      vertex   2.374770e+00 -1.085394e+01 1.187542e+01
      vertex   3.562263e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   3.562263e+00 -1.085394e+01 1.187542e+01
      vertex   2.374770e+00 -1.085394e+01 1.187542e+01
      vertex   2.374770e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   3.562263e+00 -1.085394e+01 1.187542e+01
      vertex   4.750005e+00 -1.076831e+01 1.195203e+01
      vertex   3.562263e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -5.746246e-01 8.184171e-01
    outer loop
      vertex   3.562263e+00 -1.076831e+01 1.195203e+01
      vertex   4.750005e+00 -1.076831e+01 1.195203e+01
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   7.124155e+00 -1.076831e+01 1.195203e+01
      vertex   7.124155e+00 -1.085394e+01 1.187542e+01
      vertex   7.717663e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 7.452430e-01
    outer loop
      vertex   7.717663e+00 -1.076831e+01 1.195203e+01
      vertex   7.124155e+00 -1.085394e+01 1.187542e+01
      vertex   7.717663e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   7.124155e+00 -1.085394e+01 1.187542e+01
      vertex   7.124155e+00 -1.096651e+01 1.176651e+01
      vertex   7.717663e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   7.717663e+00 -1.085394e+01 1.187542e+01
      vertex   7.124155e+00 -1.096651e+01 1.176651e+01
      vertex   7.717663e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   7.124155e+00 -1.115203e+01 1.156831e+01
      vertex   7.717663e+00 -1.115203e+01 1.156831e+01
      vertex   7.717663e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   7.124155e+00 -1.096651e+01 1.176651e+01
      vertex   7.124155e+00 -1.107542e+01 1.165394e+01
      vertex   7.717663e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   7.717663e+00 -1.096651e+01 1.176651e+01
      vertex   7.124155e+00 -1.107542e+01 1.165394e+01
      vertex   7.717663e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal -1.176258e-15 -7.877671e-01 6.159732e-01
    outer loop
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   5.937340e+00 -1.115203e+01 1.156831e+01
      vertex   4.750005e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal -1.114948e-15 -7.452430e-01 6.667929e-01
    outer loop
      vertex   4.750005e+00 -1.115203e+01 1.156831e+01
      vertex   5.937340e+00 -1.115203e+01 1.156831e+01
      vertex   5.937340e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal -3.108938e-15 -7.452430e-01 6.667929e-01
    outer loop
      vertex   4.750005e+00 -1.115203e+01 1.156831e+01
      vertex   5.937340e+00 -1.107542e+01 1.165394e+01
      vertex   4.750005e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal -3.155783e-15 -7.186833e-01 6.953375e-01
    outer loop
      vertex   4.750005e+00 -1.107542e+01 1.165394e+01
      vertex   5.937340e+00 -1.107542e+01 1.165394e+01
      vertex   5.937340e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   7.124155e+00 -1.107542e+01 1.165394e+01
      vertex   7.124155e+00 -1.115203e+01 1.156831e+01
      vertex   7.717663e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 6.667929e-01
    outer loop
      vertex   4.750005e+00 -1.107542e+01 1.165394e+01
      vertex   3.562263e+00 -1.115203e+01 1.156831e+01
      vertex   4.750005e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.877671e-01 6.159732e-01
    outer loop
      vertex   4.750005e+00 -1.115203e+01 1.156831e+01
      vertex   3.562263e+00 -1.115203e+01 1.156831e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
    endloop
  endfacet
  facet normal -2.080133e-15 -6.953375e-01 7.186833e-01
    outer loop
      vertex   4.750005e+00 -1.096651e+01 1.176651e+01
      vertex   5.937340e+00 -1.085394e+01 1.187542e+01
      vertex   4.750005e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -1.995160e-15 -6.667929e-01 7.452430e-01
    outer loop
      vertex   4.750005e+00 -1.085394e+01 1.187542e+01
      vertex   5.937340e+00 -1.085394e+01 1.187542e+01
      vertex   5.937340e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 6.953375e-01
    outer loop
      vertex   3.562263e+00 -1.107542e+01 1.165394e+01
      vertex   4.750005e+00 -1.096651e+01 1.176651e+01
      vertex   3.562263e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 7.186833e-01
    outer loop
      vertex   3.562263e+00 -1.096651e+01 1.176651e+01
      vertex   4.750005e+00 -1.096651e+01 1.176651e+01
      vertex   4.750005e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -9.481548e-01 -3.037672e-01 9.342319e-02
    outer loop
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   -1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
    endloop
  endfacet
  facet normal -9.948426e-01 -3.790053e-02 9.408344e-02
    outer loop
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
      vertex   -1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   -1.196197e+01 -1.071951e+01 9.873870e+00
    endloop
  endfacet
  facet normal -8.225950e-01 -5.439417e-01 1.657253e-01
    outer loop
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
      vertex   -1.196197e+01 -1.071951e+01 9.873870e+00
      vertex   -1.191545e+01 -1.071951e+01 1.010476e+01
    endloop
  endfacet
  facet normal -7.725896e-01 -6.155307e-01 1.556509e-01
    outer loop
      vertex   -1.191545e+01 -1.071951e+01 1.010476e+01
      vertex   -1.196197e+01 -1.071951e+01 9.873870e+00
      vertex   -1.192424e+01 -1.076831e+01 9.868141e+00
    endloop
  endfacet
  facet normal -7.725896e-01 -6.155307e-01 1.556509e-01
    outer loop
      vertex   -1.191545e+01 -1.071951e+01 1.010476e+01
      vertex   -1.192424e+01 -1.076831e+01 9.868141e+00
      vertex   -1.187844e+01 -1.076831e+01 1.009549e+01
    endloop
  endfacet
  facet normal -7.396306e-01 -6.563096e-01 1.490108e-01
    outer loop
      vertex   -1.187844e+01 -1.076831e+01 1.009549e+01
      vertex   -1.192424e+01 -1.076831e+01 9.868141e+00
      vertex   -1.189130e+01 -1.080658e+01 9.863138e+00
    endloop
  endfacet
  facet normal -7.396306e-01 -6.563096e-01 1.490108e-01
    outer loop
      vertex   -1.187844e+01 -1.076831e+01 1.009549e+01
      vertex   -1.189130e+01 -1.080658e+01 9.863138e+00
      vertex   -1.184612e+01 -1.080658e+01 1.008740e+01
    endloop
  endfacet
  facet normal -7.239756e-01 -6.742293e-01 1.458568e-01
    outer loop
      vertex   -1.184612e+01 -1.080658e+01 1.008740e+01
      vertex   -1.189130e+01 -1.080658e+01 9.863138e+00
      vertex   -1.184849e+01 -1.085394e+01 9.856638e+00
    endloop
  endfacet
  facet normal -7.239756e-01 -6.742293e-01 1.458568e-01
    outer loop
      vertex   -1.184612e+01 -1.080658e+01 1.008740e+01
      vertex   -1.184849e+01 -1.085394e+01 9.856638e+00
      vertex   -1.180412e+01 -1.085394e+01 1.007689e+01
    endloop
  endfacet
  facet normal -7.109844e-01 -6.884647e-01 1.432395e-01
    outer loop
      vertex   -1.180412e+01 -1.085394e+01 1.007689e+01
      vertex   -1.184849e+01 -1.085394e+01 9.856638e+00
      vertex   -1.179729e+01 -1.090844e+01 9.848862e+00
    endloop
  endfacet
  facet normal -7.109844e-01 -6.884647e-01 1.432395e-01
    outer loop
      vertex   -1.180412e+01 -1.085394e+01 1.007689e+01
      vertex   -1.179729e+01 -1.090844e+01 9.848862e+00
      vertex   -1.175388e+01 -1.090844e+01 1.006431e+01
    endloop
  endfacet
  facet normal -6.992751e-01 -7.008331e-01 1.408805e-01
    outer loop
      vertex   -1.175388e+01 -1.090844e+01 1.006431e+01
      vertex   -1.179729e+01 -1.090844e+01 9.848862e+00
      vertex   -1.174082e+01 -1.096651e+01 9.840287e+00
    endloop
  endfacet
  facet normal -6.992751e-01 -7.008331e-01 1.408805e-01
    outer loop
      vertex   -1.175388e+01 -1.090844e+01 1.006431e+01
      vertex   -1.174082e+01 -1.096651e+01 9.840287e+00
      vertex   -1.169848e+01 -1.096651e+01 1.005044e+01
    endloop
  endfacet
  facet normal -6.820490e-01 -7.182811e-01 1.374100e-01
    outer loop
      vertex   -1.169848e+01 -1.096651e+01 1.005044e+01
      vertex   -1.174082e+01 -1.096651e+01 9.840287e+00
      vertex   -1.162953e+01 -1.107542e+01 9.823386e+00
    endloop
  endfacet
  facet normal -6.820490e-01 -7.182811e-01 1.374100e-01
    outer loop
      vertex   -1.169848e+01 -1.096651e+01 1.005044e+01
      vertex   -1.162953e+01 -1.107542e+01 9.823386e+00
      vertex   -1.158929e+01 -1.107542e+01 1.002310e+01
    endloop
  endfacet
  facet normal -6.540793e-01 -7.448594e-01 1.317751e-01
    outer loop
      vertex   -1.158929e+01 -1.107542e+01 1.002310e+01
      vertex   -1.162953e+01 -1.107542e+01 9.823386e+00
      vertex   -1.154487e+01 -1.115203e+01 9.810530e+00
    endloop
  endfacet
  facet normal -6.540793e-01 -7.448594e-01 1.317751e-01
    outer loop
      vertex   -1.158929e+01 -1.107542e+01 1.002310e+01
      vertex   -1.154487e+01 -1.115203e+01 9.810530e+00
      vertex   -1.150623e+01 -1.115203e+01 1.000230e+01
    endloop
  endfacet
  facet normal -6.042741e-01 -7.874211e-01 1.217410e-01
    outer loop
      vertex   -1.150623e+01 -1.115203e+01 1.000230e+01
      vertex   -1.154487e+01 -1.115203e+01 9.810530e+00
      vertex   -1.149662e+01 -1.119019e+01 9.803203e+00
    endloop
  endfacet
  facet normal -6.042741e-01 -7.874211e-01 1.217410e-01
    outer loop
      vertex   -1.150623e+01 -1.115203e+01 1.000230e+01
      vertex   -1.149662e+01 -1.119019e+01 9.803203e+00
      vertex   -1.145890e+01 -1.119019e+01 9.990452e+00
    endloop
  endfacet
  facet normal -4.853684e-01 -8.688242e-01 9.778547e-02
    outer loop
      vertex   -1.145890e+01 -1.119019e+01 9.990452e+00
      vertex   -1.149662e+01 -1.119019e+01 9.803203e+00
      vertex   -1.146156e+01 -1.120000e+01 9.890099e+00
    endloop
  endfacet
  facet normal -3.311594e-01 -9.382106e-01 1.004701e-01
    outer loop
      vertex   -1.145890e+01 -1.119019e+01 9.990452e+00
      vertex   -1.146156e+01 -1.120000e+01 9.890099e+00
      vertex   -1.140344e+01 -1.119019e+01 1.017326e+01
    endloop
  endfacet
  facet normal -3.261002e-01 -9.400847e-01 9.949641e-02
    outer loop
      vertex   -1.140344e+01 -1.119019e+01 1.017326e+01
      vertex   -1.146156e+01 -1.120000e+01 9.890099e+00
      vertex   -1.134719e+01 -1.120000e+01 1.026495e+01
    endloop
  endfacet
  facet normal -4.563328e-01 -8.699627e-01 1.868833e-01
    outer loop
      vertex   -1.140344e+01 -1.119019e+01 1.017326e+01
      vertex   -1.134719e+01 -1.120000e+01 1.026495e+01
      vertex   -1.133101e+01 -1.119019e+01 1.035010e+01
    endloop
  endfacet
  facet normal -3.127757e-01 -9.350133e-01 1.670974e-01
    outer loop
      vertex   -1.133101e+01 -1.119019e+01 1.035010e+01
      vertex   -1.134719e+01 -1.120000e+01 1.026495e+01
      vertex   -1.116243e+01 -1.120000e+01 1.061079e+01
    endloop
  endfacet
  facet normal -4.932691e-01 -8.207765e-01 2.881172e-01
    outer loop
      vertex   -1.133101e+01 -1.119019e+01 1.035010e+01
      vertex   -1.116243e+01 -1.120000e+01 1.061079e+01
      vertex   -1.113842e+01 -1.119019e+01 1.067982e+01
    endloop
  endfacet
  facet normal -2.813627e-01 -9.315879e-01 2.301717e-01
    outer loop
      vertex   -1.113842e+01 -1.119019e+01 1.067982e+01
      vertex   -1.116243e+01 -1.120000e+01 1.061079e+01
      vertex   -1.091421e+01 -1.120000e+01 1.091421e+01
    endloop
  endfacet
  facet normal -4.155888e-01 -8.341303e-01 3.626466e-01
    outer loop
      vertex   -1.113842e+01 -1.119019e+01 1.067982e+01
      vertex   -1.091421e+01 -1.120000e+01 1.091421e+01
      vertex   -1.088743e+01 -1.119019e+01 1.096746e+01
    endloop
  endfacet
  facet normal -2.380402e-01 -9.268216e-01 2.904112e-01
    outer loop
      vertex   -1.088743e+01 -1.119019e+01 1.096746e+01
      vertex   -1.091421e+01 -1.120000e+01 1.091421e+01
      vertex   -1.061103e+01 -1.120000e+01 1.116272e+01
    endloop
  endfacet
  facet normal -3.226260e-01 -8.512132e-01 4.139428e-01
    outer loop
      vertex   -1.088743e+01 -1.119019e+01 1.096746e+01
      vertex   -1.061103e+01 -1.120000e+01 1.116272e+01
      vertex   -1.058633e+01 -1.119019e+01 1.120214e+01
    endloop
  endfacet
  facet normal -2.033875e-01 -9.126666e-01 3.545041e-01
    outer loop
      vertex   -1.058633e+01 -1.119019e+01 1.120214e+01
      vertex   -1.061103e+01 -1.120000e+01 1.116272e+01
      vertex   -1.042057e+01 -1.119019e+01 1.129724e+01
    endloop
  endfacet
  facet normal -3.067685e-01 -7.873958e-01 5.346970e-01
    outer loop
      vertex   -1.058633e+01 -1.119019e+01 1.120214e+01
      vertex   -1.042057e+01 -1.119019e+01 1.129724e+01
      vertex   -1.044282e+01 -1.115203e+01 1.134067e+01
    endloop
  endfacet
  facet normal -2.551817e-01 -7.874090e-01 5.611322e-01
    outer loop
      vertex   -1.044282e+01 -1.115203e+01 1.134067e+01
      vertex   -1.042057e+01 -1.119019e+01 1.129724e+01
      vertex   -1.026465e+01 -1.115203e+01 1.142169e+01
    endloop
  endfacet
  facet normal -2.762134e-01 -7.448461e-01 6.073799e-01
    outer loop
      vertex   -1.044282e+01 -1.115203e+01 1.134067e+01
      vertex   -1.026465e+01 -1.115203e+01 1.142169e+01
      vertex   -1.029631e+01 -1.107542e+01 1.150125e+01
    endloop
  endfacet
  facet normal -2.173235e-01 -7.448647e-01 6.308304e-01
    outer loop
      vertex   -1.029631e+01 -1.107542e+01 1.150125e+01
      vertex   -1.026465e+01 -1.115203e+01 1.142169e+01
      vertex   -1.010356e+01 -1.107542e+01 1.156765e+01
    endloop
  endfacet
  facet normal -2.266168e-01 -7.182866e-01 6.578063e-01
    outer loop
      vertex   -1.029631e+01 -1.107542e+01 1.150125e+01
      vertex   -1.010356e+01 -1.107542e+01 1.156765e+01
      vertex   -1.013510e+01 -1.096651e+01 1.167571e+01
    endloop
  endfacet
  facet normal -1.630560e-01 -7.182917e-01 6.763651e-01
    outer loop
      vertex   -1.013510e+01 -1.096651e+01 1.167571e+01
      vertex   -1.010356e+01 -1.107542e+01 1.156765e+01
      vertex   -9.926617e+00 -1.096651e+01 1.172597e+01
    endloop
  endfacet
  facet normal -1.671744e-01 -7.008439e-01 6.934483e-01
    outer loop
      vertex   -1.013510e+01 -1.096651e+01 1.167571e+01
      vertex   -9.926617e+00 -1.096651e+01 1.172597e+01
      vertex   -9.937367e+00 -1.090844e+01 1.178206e+01
    endloop
  endfacet
  facet normal -1.009871e-01 -7.008422e-01 7.061316e-01
    outer loop
      vertex   -9.937367e+00 -1.090844e+01 1.178206e+01
      vertex   -9.926617e+00 -1.096651e+01 1.172597e+01
      vertex   -9.719737e+00 -1.090844e+01 1.181319e+01
    endloop
  endfacet
  facet normal -1.026782e-01 -6.884740e-01 7.179560e-01
    outer loop
      vertex   -9.937367e+00 -1.090844e+01 1.178206e+01
      vertex   -9.719737e+00 -1.090844e+01 1.181319e+01
      vertex   -9.724635e+00 -1.085394e+01 1.186475e+01
    endloop
  endfacet
  facet normal -3.441191e-02 -6.884757e-01 7.244426e-01
    outer loop
      vertex   -9.724635e+00 -1.085394e+01 1.186475e+01
      vertex   -9.719737e+00 -1.090844e+01 1.181319e+01
      vertex   -9.500000e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -3.504071e-02 -6.742404e-01 7.376801e-01
    outer loop
      vertex   -9.724635e+00 -1.085394e+01 1.186475e+01
      vertex   -9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   -9.728729e+00 -1.080658e+01 1.190785e+01
    endloop
  endfacet
  facet normal -3.240909e-02 -6.664427e-01 7.448516e-01
    outer loop
      vertex   -9.728729e+00 -1.080658e+01 1.190785e+01
      vertex   -9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   -9.500000e+00 -1.076831e+01 1.195203e+01
    endloop
  endfacet
  facet normal -3.579845e-02 -6.563209e-01 7.536321e-01
    outer loop
      vertex   -9.728729e+00 -1.080658e+01 1.190785e+01
      vertex   -9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   -9.731880e+00 -1.076831e+01 1.194102e+01
    endloop
  endfacet
  facet normal -3.739373e-02 -6.155424e-01 7.872162e-01
    outer loop
      vertex   -9.731880e+00 -1.076831e+01 1.194102e+01
      vertex   -9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   -9.500000e+00 -1.071951e+01 1.199019e+01
    endloop
  endfacet
  facet normal -3.739373e-02 -6.155424e-01 7.872162e-01
    outer loop
      vertex   -9.731880e+00 -1.076831e+01 1.194102e+01
      vertex   -9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   -9.735488e+00 -1.071951e+01 1.197901e+01
    endloop
  endfacet
  facet normal -4.068271e-02 -5.146145e-01 8.564560e-01
    outer loop
      vertex   -9.735488e+00 -1.071951e+01 1.197901e+01
      vertex   -9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   -9.500000e+00 -1.070684e+01 1.199781e+01
    endloop
  endfacet
  facet normal -5.950433e-02 -3.045610e-01 9.506323e-01
    outer loop
      vertex   -9.735488e+00 -1.071951e+01 1.197901e+01
      vertex   -9.500000e+00 -1.070684e+01 1.199781e+01
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal -9.690021e-01 2.256693e-01 1.005396e-01
    outer loop
      vertex   -1.196197e+01 -1.071951e+01 9.873870e+00
      vertex   -1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   -1.198628e+01 -1.071951e+01 9.639563e+00
    endloop
  endfacet
  facet normal -8.569179e-01 -5.148920e-01 2.404018e-02
    outer loop
      vertex   -1.198628e+01 -1.071951e+01 9.639563e+00
      vertex   -1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   -1.199019e+01 -1.071951e+01 9.500000e+00
    endloop
  endfacet
  facet normal -7.875748e-01 -6.158228e-01 2.209481e-02
    outer loop
      vertex   -1.198628e+01 -1.071951e+01 9.639563e+00
      vertex   -1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 9.500000e+00
    endloop
  endfacet
  facet normal -7.451490e-01 -6.667088e-01 1.588740e-02
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   -1.191491e+01 -1.080658e+01 9.635557e+00
      vertex   -1.195203e+01 -1.076831e+01 9.500000e+00
    endloop
  endfacet
  facet normal -7.539467e-01 -6.565950e-01 2.115140e-02
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   -1.191491e+01 -1.080658e+01 9.635557e+00
      vertex   -1.194818e+01 -1.076831e+01 9.637424e+00
    endloop
  endfacet
  facet normal -7.875748e-01 -6.158228e-01 2.209481e-02
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   -1.194818e+01 -1.076831e+01 9.637424e+00
      vertex   -1.198628e+01 -1.071951e+01 9.639563e+00
    endloop
  endfacet
  facet normal -7.838937e-01 -6.155449e-01 8.133355e-02
    outer loop
      vertex   -1.198628e+01 -1.071951e+01 9.639563e+00
      vertex   -1.194818e+01 -1.076831e+01 9.637424e+00
      vertex   -1.196197e+01 -1.071951e+01 9.873870e+00
    endloop
  endfacet
  facet normal -7.186025e-01 -6.952593e-01 1.499825e-02
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   -1.181997e+01 -1.090844e+01 9.630228e+00
      vertex   -1.187542e+01 -1.085394e+01 9.500000e+00
    endloop
  endfacet
  facet normal -7.247221e-01 -6.887413e-01 2.033153e-02
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   -1.181997e+01 -1.090844e+01 9.630228e+00
      vertex   -1.187168e+01 -1.085394e+01 9.633131e+00
    endloop
  endfacet
  facet normal -7.379752e-01 -6.745101e-01 2.070333e-02
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   -1.187168e+01 -1.085394e+01 9.633131e+00
      vertex   -1.191491e+01 -1.080658e+01 9.635557e+00
    endloop
  endfacet
  facet normal -7.345663e-01 -6.742429e-01 7.621555e-02
    outer loop
      vertex   -1.191491e+01 -1.080658e+01 9.635557e+00
      vertex   -1.187168e+01 -1.085394e+01 9.633131e+00
      vertex   -1.189130e+01 -1.080658e+01 9.863138e+00
    endloop
  endfacet
  facet normal -7.504510e-01 -6.563235e-01 7.786368e-02
    outer loop
      vertex   -1.191491e+01 -1.080658e+01 9.635557e+00
      vertex   -1.189130e+01 -1.080658e+01 9.863138e+00
      vertex   -1.192424e+01 -1.076831e+01 9.868141e+00
    endloop
  endfacet
  facet normal -7.127772e-01 -7.011054e-01 1.999642e-02
    outer loop
      vertex   -1.181997e+01 -1.090844e+01 9.630228e+00
      vertex   -1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   -1.176295e+01 -1.096651e+01 9.627027e+00
    endloop
  endfacet
  facet normal -6.952053e-01 -7.185466e-01 1.950346e-02
    outer loop
      vertex   -1.176295e+01 -1.096651e+01 9.627027e+00
      vertex   -1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   -1.165394e+01 -1.107542e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.952053e-01 -7.185466e-01 1.950346e-02
    outer loop
      vertex   -1.176295e+01 -1.096651e+01 9.627027e+00
      vertex   -1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   -1.165056e+01 -1.107542e+01 9.620718e+00
    endloop
  endfacet
  facet normal -6.666763e-01 -7.451127e-01 1.870310e-02
    outer loop
      vertex   -1.165056e+01 -1.107542e+01 9.620718e+00
      vertex   -1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.666763e-01 -7.451127e-01 1.870310e-02
    outer loop
      vertex   -1.165056e+01 -1.107542e+01 9.620718e+00
      vertex   -1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   -1.156506e+01 -1.115203e+01 9.615919e+00
    endloop
  endfacet
  facet normal -6.158812e-01 -7.876495e-01 1.727808e-02
    outer loop
      vertex   -1.156506e+01 -1.115203e+01 9.615919e+00
      vertex   -1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.158812e-01 -7.876495e-01 1.727808e-02
    outer loop
      vertex   -1.156506e+01 -1.115203e+01 9.615919e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.151634e+01 -1.119019e+01 9.613184e+00
    endloop
  endfacet
  facet normal -5.149871e-01 -8.570762e-01 1.444757e-02
    outer loop
      vertex   -1.151634e+01 -1.119019e+01 9.613184e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.150684e+01 -1.119781e+01 9.500000e+00
    endloop
  endfacet
  facet normal -3.048761e-01 -9.516161e-01 3.843645e-02
    outer loop
      vertex   -1.151634e+01 -1.119019e+01 9.613184e+00
      vertex   -1.150684e+01 -1.119781e+01 9.500000e+00
      vertex   -1.150000e+01 -1.120000e+01 9.500000e+00
    endloop
  endfacet
  facet normal -3.357872e-01 -9.413566e-01 3.308564e-02
    outer loop
      vertex   -1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   -1.146156e+01 -1.120000e+01 9.890099e+00
      vertex   -1.151634e+01 -1.119019e+01 9.613184e+00
    endloop
  endfacet
  facet normal -3.521352e-01 -9.352358e-01 3.653608e-02
    outer loop
      vertex   -1.151634e+01 -1.119019e+01 9.613184e+00
      vertex   -1.146156e+01 -1.120000e+01 9.890099e+00
      vertex   -1.149662e+01 -1.119019e+01 9.803203e+00
    endloop
  endfacet
  facet normal -6.131100e-01 -7.874322e-01 6.361374e-02
    outer loop
      vertex   -1.151634e+01 -1.119019e+01 9.613184e+00
      vertex   -1.149662e+01 -1.119019e+01 9.803203e+00
      vertex   -1.154487e+01 -1.115203e+01 9.810530e+00
    endloop
  endfacet
  facet normal -1.522045e-01 -9.465158e-01 2.845023e-01
    outer loop
      vertex   -1.061103e+01 -1.120000e+01 1.116272e+01
      vertex   -1.026535e+01 -1.120000e+01 1.134765e+01
      vertex   -1.042057e+01 -1.119019e+01 1.129724e+01
    endloop
  endfacet
  facet normal -1.950096e-01 -8.820927e-01 4.288166e-01
    outer loop
      vertex   -1.042057e+01 -1.119019e+01 1.129724e+01
      vertex   -1.026535e+01 -1.120000e+01 1.134765e+01
      vertex   -1.024661e+01 -1.119019e+01 1.137635e+01
    endloop
  endfacet
  facet normal -2.551817e-01 -7.874090e-01 5.611322e-01
    outer loop
      vertex   -1.042057e+01 -1.119019e+01 1.129724e+01
      vertex   -1.024661e+01 -1.119019e+01 1.137635e+01
      vertex   -1.026465e+01 -1.115203e+01 1.142169e+01
    endloop
  endfacet
  facet normal -2.007751e-01 -7.874258e-01 5.827949e-01
    outer loop
      vertex   -1.026465e+01 -1.115203e+01 1.142169e+01
      vertex   -1.024661e+01 -1.119019e+01 1.137635e+01
      vertex   -1.007957e+01 -1.115203e+01 1.148545e+01
    endloop
  endfacet
  facet normal -2.173235e-01 -7.448647e-01 6.308304e-01
    outer loop
      vertex   -1.026465e+01 -1.115203e+01 1.142169e+01
      vertex   -1.007957e+01 -1.115203e+01 1.148545e+01
      vertex   -1.010356e+01 -1.107542e+01 1.156765e+01
    endloop
  endfacet
  facet normal -1.563692e-01 -7.448695e-01 6.486278e-01
    outer loop
      vertex   -1.010356e+01 -1.107542e+01 1.156765e+01
      vertex   -1.007957e+01 -1.115203e+01 1.148545e+01
      vertex   -9.905429e+00 -1.107542e+01 1.161542e+01
    endloop
  endfacet
  facet normal -1.630560e-01 -7.182917e-01 6.763651e-01
    outer loop
      vertex   -1.010356e+01 -1.107542e+01 1.156765e+01
      vertex   -9.905429e+00 -1.107542e+01 1.161542e+01
      vertex   -9.926617e+00 -1.096651e+01 1.172597e+01
    endloop
  endfacet
  facet normal -9.849934e-02 -7.182900e-01 6.887361e-01
    outer loop
      vertex   -9.926617e+00 -1.096651e+01 1.172597e+01
      vertex   -9.905429e+00 -1.107542e+01 1.161542e+01
      vertex   -9.714335e+00 -1.096651e+01 1.175633e+01
    endloop
  endfacet
  facet normal -1.009871e-01 -7.008422e-01 7.061316e-01
    outer loop
      vertex   -9.926617e+00 -1.096651e+01 1.172597e+01
      vertex   -9.714335e+00 -1.096651e+01 1.175633e+01
      vertex   -9.719737e+00 -1.090844e+01 1.181319e+01
    endloop
  endfacet
  facet normal -3.384516e-02 -7.008439e-01 7.125113e-01
    outer loop
      vertex   -9.719737e+00 -1.090844e+01 1.181319e+01
      vertex   -9.714335e+00 -1.096651e+01 1.175633e+01
      vertex   -9.500000e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal -3.106396e-02 -6.950020e-01 7.183365e-01
    outer loop
      vertex   -9.719737e+00 -1.090844e+01 1.181319e+01
      vertex   -9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   -9.500000e+00 -1.085394e+01 1.187542e+01
    endloop
  endfacet
  facet normal -1.376745e-01 -9.062785e-01 3.996311e-01
    outer loop
      vertex   -1.024661e+01 -1.119019e+01 1.137635e+01
      vertex   -1.026535e+01 -1.120000e+01 1.134765e+01
      vertex   -1.006589e+01 -1.119019e+01 1.143861e+01
    endloop
  endfacet
  facet normal -9.279314e-02 -9.476078e-01 3.056615e-01
    outer loop
      vertex   -1.006589e+01 -1.119019e+01 1.143861e+01
      vertex   -1.026535e+01 -1.120000e+01 1.134765e+01
      vertex   -9.890201e+00 -1.120000e+01 1.146154e+01
    endloop
  endfacet
  facet normal -1.080320e-01 -8.874206e-01 4.481226e-01
    outer loop
      vertex   -1.006589e+01 -1.119019e+01 1.143861e+01
      vertex   -9.890201e+00 -1.120000e+01 1.146154e+01
      vertex   -9.880125e+00 -1.119019e+01 1.148339e+01
    endloop
  endfacet
  facet normal -6.182307e-02 -8.996153e-01 4.322850e-01
    outer loop
      vertex   -9.880125e+00 -1.119019e+01 1.148339e+01
      vertex   -9.890201e+00 -1.120000e+01 1.146154e+01
      vertex   -9.690978e+00 -1.119019e+01 1.151044e+01
    endloop
  endfacet
  facet normal -8.726711e-02 -7.874287e-01 6.101970e-01
    outer loop
      vertex   -9.880125e+00 -1.119019e+01 1.148339e+01
      vertex   -9.690978e+00 -1.119019e+01 1.151044e+01
      vertex   -9.695593e+00 -1.115203e+01 1.155902e+01
    endloop
  endfacet
  facet normal -2.924696e-02 -7.874301e-01 6.157097e-01
    outer loop
      vertex   -9.695593e+00 -1.115203e+01 1.155902e+01
      vertex   -9.690978e+00 -1.119019e+01 1.151044e+01
      vertex   -9.500000e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal -3.165761e-02 -7.448695e-01 6.664587e-01
    outer loop
      vertex   -9.695593e+00 -1.115203e+01 1.155902e+01
      vertex   -9.500000e+00 -1.115203e+01 1.156831e+01
      vertex   -9.500000e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal -3.005630e-02 -9.518896e-01 3.049638e-01
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   -9.500000e+00 -1.119781e+01 1.150684e+01
      vertex   -9.890201e+00 -1.120000e+01 1.146154e+01
    endloop
  endfacet
  facet normal -3.174269e-02 -9.471353e-01 3.192603e-01
    outer loop
      vertex   -9.890201e+00 -1.120000e+01 1.146154e+01
      vertex   -9.500000e+00 -1.119781e+01 1.150684e+01
      vertex   -9.690978e+00 -1.119019e+01 1.151044e+01
    endloop
  endfacet
  facet normal -2.445775e-02 -8.569092e-01 5.148868e-01
    outer loop
      vertex   -9.500000e+00 -1.119781e+01 1.150684e+01
      vertex   -9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   -9.690978e+00 -1.119019e+01 1.151044e+01
    endloop
  endfacet
  facet normal -2.924696e-02 -7.874301e-01 6.157097e-01
    outer loop
      vertex   -9.690978e+00 -1.119019e+01 1.151044e+01
      vertex   -9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   -9.500000e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal -3.165761e-02 -7.448695e-01 6.664587e-01
    outer loop
      vertex   -9.695593e+00 -1.115203e+01 1.155902e+01
      vertex   -9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   -9.703690e+00 -1.107542e+01 1.164427e+01
    endloop
  endfacet
  facet normal -3.301138e-02 -7.182916e-01 6.949586e-01
    outer loop
      vertex   -9.703690e+00 -1.107542e+01 1.164427e+01
      vertex   -9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   -9.500000e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal -3.301138e-02 -7.182916e-01 6.949586e-01
    outer loop
      vertex   -9.703690e+00 -1.107542e+01 1.164427e+01
      vertex   -9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   -9.714335e+00 -1.096651e+01 1.175633e+01
    endloop
  endfacet
  facet normal -9.746066e-02 1.123611e-01 9.888763e-01
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   -9.987751e+00 -1.070000e+01 1.195193e+01
      vertex   -9.735488e+00 -1.071951e+01 1.197901e+01
    endloop
  endfacet
  facet normal -1.287907e-01 -4.152551e-01 9.005422e-01
    outer loop
      vertex   -9.735488e+00 -1.071951e+01 1.197901e+01
      vertex   -9.987751e+00 -1.070000e+01 1.195193e+01
      vertex   -9.968720e+00 -1.071951e+01 1.194565e+01
    endloop
  endfacet
  facet normal -1.115753e-01 -6.155406e-01 7.801671e-01
    outer loop
      vertex   -9.735488e+00 -1.071951e+01 1.197901e+01
      vertex   -9.968720e+00 -1.071951e+01 1.194565e+01
      vertex   -9.961537e+00 -1.076831e+01 1.190818e+01
    endloop
  endfacet
  facet normal -1.847022e-01 -6.155424e-01 7.661545e-01
    outer loop
      vertex   -9.961537e+00 -1.076831e+01 1.190818e+01
      vertex   -9.968720e+00 -1.071951e+01 1.194565e+01
      vertex   -1.018709e+01 -1.076831e+01 1.185380e+01
    endloop
  endfacet
  facet normal -1.768224e-01 -6.563210e-01 7.334689e-01
    outer loop
      vertex   -9.961537e+00 -1.076831e+01 1.190818e+01
      vertex   -1.018709e+01 -1.076831e+01 1.185380e+01
      vertex   -1.017775e+01 -1.080658e+01 1.182181e+01
    endloop
  endfacet
  facet normal -2.457492e-01 -6.563156e-01 7.133423e-01
    outer loop
      vertex   -1.017775e+01 -1.080658e+01 1.182181e+01
      vertex   -1.018709e+01 -1.076831e+01 1.185380e+01
      vertex   -1.039419e+01 -1.080658e+01 1.174725e+01
    endloop
  endfacet
  facet normal -2.405476e-01 -6.742351e-01 6.982434e-01
    outer loop
      vertex   -1.017775e+01 -1.080658e+01 1.182181e+01
      vertex   -1.039419e+01 -1.080658e+01 1.174725e+01
      vertex   -1.037818e+01 -1.085394e+01 1.170703e+01
    endloop
  endfacet
  facet normal -3.057289e-01 -6.742145e-01 6.722831e-01
    outer loop
      vertex   -1.037818e+01 -1.085394e+01 1.170703e+01
      vertex   -1.039419e+01 -1.080658e+01 1.174725e+01
      vertex   -1.058281e+01 -1.085394e+01 1.161397e+01
    endloop
  endfacet
  facet normal -3.002431e-01 -6.884501e-01 6.602200e-01
    outer loop
      vertex   -1.037818e+01 -1.085394e+01 1.170703e+01
      vertex   -1.058281e+01 -1.085394e+01 1.161397e+01
      vertex   -1.055920e+01 -1.090844e+01 1.156788e+01
    endloop
  endfacet
  facet normal -3.609371e-01 -6.884341e-01 6.291128e-01
    outer loop
      vertex   -1.055920e+01 -1.090844e+01 1.156788e+01
      vertex   -1.058281e+01 -1.085394e+01 1.161397e+01
      vertex   -1.074991e+01 -1.090844e+01 1.145846e+01
    endloop
  endfacet
  facet normal -3.549933e-01 -7.008030e-01 6.187527e-01
    outer loop
      vertex   -1.055920e+01 -1.090844e+01 1.156788e+01
      vertex   -1.074991e+01 -1.090844e+01 1.145846e+01
      vertex   -1.071919e+01 -1.096651e+01 1.141032e+01
    endloop
  endfacet
  facet normal -4.392378e-01 -6.996208e-01 5.635608e-01
    outer loop
      vertex   -1.071919e+01 -1.096651e+01 1.141032e+01
      vertex   -1.074991e+01 -1.090844e+01 1.145846e+01
      vertex   -1.105712e+01 -1.096651e+01 1.114694e+01
    endloop
  endfacet
  facet normal -4.284536e-01 -7.170990e-01 5.497241e-01
    outer loop
      vertex   -1.071919e+01 -1.096651e+01 1.141032e+01
      vertex   -1.105712e+01 -1.096651e+01 1.114694e+01
      vertex   -1.097979e+01 -1.107542e+01 1.106514e+01
    endloop
  endfacet
  facet normal -5.251624e-01 -7.170780e-01 4.582615e-01
    outer loop
      vertex   -1.097979e+01 -1.107542e+01 1.106514e+01
      vertex   -1.105712e+01 -1.096651e+01 1.114694e+01
      vertex   -1.124749e+01 -1.107542e+01 1.075836e+01
    endloop
  endfacet
  facet normal -5.036941e-01 -7.437118e-01 4.395281e-01
    outer loop
      vertex   -1.097979e+01 -1.107542e+01 1.106514e+01
      vertex   -1.124749e+01 -1.107542e+01 1.075836e+01
      vertex   -1.117802e+01 -1.115203e+01 1.070833e+01
    endloop
  endfacet
  facet normal -5.773065e-01 -7.436472e-01 3.372033e-01
    outer loop
      vertex   -1.117802e+01 -1.115203e+01 1.070833e+01
      vertex   -1.124749e+01 -1.107542e+01 1.075836e+01
      vertex   -1.137526e+01 -1.115203e+01 1.037065e+01
    endloop
  endfacet
  facet normal -5.334743e-01 -7.863269e-01 3.116010e-01
    outer loop
      vertex   -1.117802e+01 -1.115203e+01 1.070833e+01
      vertex   -1.137526e+01 -1.115203e+01 1.037065e+01
      vertex   -1.133101e+01 -1.119019e+01 1.035010e+01
    endloop
  endfacet
  facet normal -5.705342e-01 -7.873355e-01 2.336526e-01
    outer loop
      vertex   -1.133101e+01 -1.119019e+01 1.035010e+01
      vertex   -1.137526e+01 -1.115203e+01 1.037065e+01
      vertex   -1.140344e+01 -1.119019e+01 1.017326e+01
    endloop
  endfacet
  facet normal -2.061090e-01 -4.760019e-01 8.549511e-01
    outer loop
      vertex   -9.968720e+00 -1.071951e+01 1.194565e+01
      vertex   -9.987751e+00 -1.070000e+01 1.195193e+01
      vertex   -1.019778e+01 -1.071951e+01 1.189043e+01
    endloop
  endfacet
  facet normal -2.887170e-01 1.103256e-01 9.510367e-01
    outer loop
      vertex   -1.019778e+01 -1.071951e+01 1.189043e+01
      vertex   -9.987751e+00 -1.070000e+01 1.195193e+01
      vertex   -1.045669e+01 -1.070000e+01 1.180957e+01
    endloop
  endfacet
  facet normal -3.020356e-01 -3.743337e-01 8.767262e-01
    outer loop
      vertex   -1.019778e+01 -1.071951e+01 1.189043e+01
      vertex   -1.045669e+01 -1.070000e+01 1.180957e+01
      vertex   -1.042062e+01 -1.071951e+01 1.181366e+01
    endloop
  endfacet
  facet normal -3.589941e-01 -4.979499e-01 7.894107e-01
    outer loop
      vertex   -1.042062e+01 -1.071951e+01 1.181366e+01
      vertex   -1.045669e+01 -1.070000e+01 1.180957e+01
      vertex   -1.063512e+01 -1.071951e+01 1.171611e+01
    endloop
  endfacet
  facet normal -3.262572e-01 -6.155154e-01 7.174239e-01
    outer loop
      vertex   -1.042062e+01 -1.071951e+01 1.181366e+01
      vertex   -1.063512e+01 -1.071951e+01 1.171611e+01
      vertex   -1.061773e+01 -1.076831e+01 1.168215e+01
    endloop
  endfacet
  facet normal -3.922083e-01 -6.154985e-01 6.836185e-01
    outer loop
      vertex   -1.061773e+01 -1.076831e+01 1.168215e+01
      vertex   -1.063512e+01 -1.071951e+01 1.171611e+01
      vertex   -1.081899e+01 -1.076831e+01 1.156669e+01
    endloop
  endfacet
  facet normal -3.754782e-01 -6.562781e-01 6.544579e-01
    outer loop
      vertex   -1.061773e+01 -1.076831e+01 1.168215e+01
      vertex   -1.081899e+01 -1.076831e+01 1.156669e+01
      vertex   -1.080106e+01 -1.080658e+01 1.153860e+01
    endloop
  endfacet
  facet normal -4.644912e-01 -6.550400e-01 5.959619e-01
    outer loop
      vertex   -1.080106e+01 -1.080658e+01 1.153860e+01
      vertex   -1.081899e+01 -1.076831e+01 1.156669e+01
      vertex   -1.116169e+01 -1.080658e+01 1.125754e+01
    endloop
  endfacet
  facet normal -4.546966e-01 -6.729794e-01 5.833950e-01
    outer loop
      vertex   -1.080106e+01 -1.080658e+01 1.153860e+01
      vertex   -1.116169e+01 -1.080658e+01 1.125754e+01
      vertex   -1.113194e+01 -1.085394e+01 1.122608e+01
    endloop
  endfacet
  facet normal -5.573268e-01 -6.729572e-01 4.863285e-01
    outer loop
      vertex   -1.113194e+01 -1.085394e+01 1.122608e+01
      vertex   -1.116169e+01 -1.080658e+01 1.125754e+01
      vertex   -1.142717e+01 -1.085394e+01 1.088775e+01
    endloop
  endfacet
  facet normal -5.473627e-01 -6.872119e-01 4.776337e-01
    outer loop
      vertex   -1.113194e+01 -1.085394e+01 1.122608e+01
      vertex   -1.142717e+01 -1.085394e+01 1.088775e+01
      vertex   -1.138515e+01 -1.090844e+01 1.085749e+01
    endloop
  endfacet
  facet normal -6.273472e-01 -6.871413e-01 3.664319e-01
    outer loop
      vertex   -1.138515e+01 -1.090844e+01 1.085749e+01
      vertex   -1.142717e+01 -1.085394e+01 1.088775e+01
      vertex   -1.160674e+01 -1.090844e+01 1.047812e+01
    endloop
  endfacet
  facet normal -6.170540e-01 -6.995298e-01 3.604197e-01
    outer loop
      vertex   -1.138515e+01 -1.090844e+01 1.085749e+01
      vertex   -1.160674e+01 -1.090844e+01 1.047812e+01
      vertex   -1.155495e+01 -1.096651e+01 1.045408e+01
    endloop
  endfacet
  facet normal -6.602065e-01 -7.007311e-01 2.703763e-01
    outer loop
      vertex   -1.155495e+01 -1.096651e+01 1.045408e+01
      vertex   -1.160674e+01 -1.090844e+01 1.047812e+01
      vertex   -1.163624e+01 -1.096651e+01 1.025560e+01
    endloop
  endfacet
  facet normal -6.439473e-01 -7.181816e-01 2.637177e-01
    outer loop
      vertex   -1.155495e+01 -1.096651e+01 1.045408e+01
      vertex   -1.163624e+01 -1.096651e+01 1.025560e+01
      vertex   -1.153014e+01 -1.107542e+01 1.021808e+01
    endloop
  endfacet
  facet normal -6.658310e-01 -7.182359e-01 2.020057e-01
    outer loop
      vertex   -1.153014e+01 -1.107542e+01 1.021808e+01
      vertex   -1.163624e+01 -1.096651e+01 1.025560e+01
      vertex   -1.158929e+01 -1.107542e+01 1.002310e+01
    endloop
  endfacet
  facet normal -6.385296e-01 -7.448164e-01 1.937228e-01
    outer loop
      vertex   -1.153014e+01 -1.107542e+01 1.021808e+01
      vertex   -1.158929e+01 -1.107542e+01 1.002310e+01
      vertex   -1.150623e+01 -1.115203e+01 1.000230e+01
    endloop
  endfacet
  facet normal -4.697954e-01 9.028051e-02 8.781467e-01
    outer loop
      vertex   -1.045669e+01 -1.070000e+01 1.180957e+01
      vertex   -1.088879e+01 -1.070000e+01 1.157840e+01
      vertex   -1.063512e+01 -1.071951e+01 1.171611e+01
    endloop
  endfacet
  facet normal -4.700467e-01 -3.283578e-01 8.192907e-01
    outer loop
      vertex   -1.063512e+01 -1.071951e+01 1.171611e+01
      vertex   -1.088879e+01 -1.070000e+01 1.157840e+01
      vertex   -1.083951e+01 -1.071951e+01 1.159885e+01
    endloop
  endfacet
  facet normal -3.922083e-01 -6.154985e-01 6.836185e-01
    outer loop
      vertex   -1.063512e+01 -1.071951e+01 1.171611e+01
      vertex   -1.083951e+01 -1.071951e+01 1.159885e+01
      vertex   -1.081899e+01 -1.076831e+01 1.156669e+01
    endloop
  endfacet
  facet normal -4.851041e-01 -6.142318e-01 6.224092e-01
    outer loop
      vertex   -1.081899e+01 -1.076831e+01 1.156669e+01
      vertex   -1.083951e+01 -1.071951e+01 1.159885e+01
      vertex   -1.118458e+01 -1.076831e+01 1.128175e+01
    endloop
  endfacet
  facet normal -4.644912e-01 -6.550400e-01 5.959619e-01
    outer loop
      vertex   -1.081899e+01 -1.076831e+01 1.156669e+01
      vertex   -1.118458e+01 -1.076831e+01 1.128175e+01
      vertex   -1.116169e+01 -1.080658e+01 1.125754e+01
    endloop
  endfacet
  facet normal -5.693314e-01 -6.550174e-01 4.968038e-01
    outer loop
      vertex   -1.116169e+01 -1.080658e+01 1.125754e+01
      vertex   -1.118458e+01 -1.076831e+01 1.128175e+01
      vertex   -1.146229e+01 -1.080658e+01 1.091304e+01
    endloop
  endfacet
  facet normal -5.573268e-01 -6.729572e-01 4.863285e-01
    outer loop
      vertex   -1.116169e+01 -1.080658e+01 1.125754e+01
      vertex   -1.146229e+01 -1.080658e+01 1.091304e+01
      vertex   -1.142717e+01 -1.085394e+01 1.088775e+01
    endloop
  endfacet
  facet normal -6.387649e-01 -6.728856e-01 3.731010e-01
    outer loop
      vertex   -1.142717e+01 -1.085394e+01 1.088775e+01
      vertex   -1.146229e+01 -1.080658e+01 1.091304e+01
      vertex   -1.165370e+01 -1.085394e+01 1.049992e+01
    endloop
  endfacet
  facet normal -6.273472e-01 -6.871413e-01 3.664319e-01
    outer loop
      vertex   -1.142717e+01 -1.085394e+01 1.088775e+01
      vertex   -1.165370e+01 -1.085394e+01 1.049992e+01
      vertex   -1.160674e+01 -1.090844e+01 1.047812e+01
    endloop
  endfacet
  facet normal -6.712582e-01 -6.883611e-01 2.749024e-01
    outer loop
      vertex   -1.160674e+01 -1.090844e+01 1.047812e+01
      vertex   -1.165370e+01 -1.085394e+01 1.049992e+01
      vertex   -1.169007e+01 -1.090844e+01 1.027464e+01
    endloop
  endfacet
  facet normal -6.602065e-01 -7.007311e-01 2.703763e-01
    outer loop
      vertex   -1.160674e+01 -1.090844e+01 1.047812e+01
      vertex   -1.169007e+01 -1.090844e+01 1.027464e+01
      vertex   -1.163624e+01 -1.096651e+01 1.025560e+01
    endloop
  endfacet
  facet normal -6.826453e-01 -7.007867e-01 2.071070e-01
    outer loop
      vertex   -1.163624e+01 -1.096651e+01 1.025560e+01
      vertex   -1.169007e+01 -1.090844e+01 1.027464e+01
      vertex   -1.169848e+01 -1.096651e+01 1.005044e+01
    endloop
  endfacet
  facet normal -6.658310e-01 -7.182359e-01 2.020057e-01
    outer loop
      vertex   -1.163624e+01 -1.096651e+01 1.025560e+01
      vertex   -1.169848e+01 -1.096651e+01 1.005044e+01
      vertex   -1.158929e+01 -1.107542e+01 1.002310e+01
    endloop
  endfacet
  facet normal -4.975203e-01 -5.873635e-01 6.383397e-01
    outer loop
      vertex   -1.083951e+01 -1.071951e+01 1.159885e+01
      vertex   -1.088879e+01 -1.070000e+01 1.157840e+01
      vertex   -1.121079e+01 -1.071951e+01 1.130948e+01
    endloop
  endfacet
  facet normal -6.218877e-01 -1.939507e-01 7.587087e-01
    outer loop
      vertex   -1.121079e+01 -1.071951e+01 1.130948e+01
      vertex   -1.088879e+01 -1.070000e+01 1.157840e+01
      vertex   -1.126777e+01 -1.070000e+01 1.126777e+01
    endloop
  endfacet
  facet normal -5.899391e-01 -6.220667e-01 5.147863e-01
    outer loop
      vertex   -1.121079e+01 -1.071951e+01 1.130948e+01
      vertex   -1.126777e+01 -1.070000e+01 1.126777e+01
      vertex   -1.152029e+01 -1.071951e+01 1.095480e+01
    endloop
  endfacet
  facet normal -7.666342e-01 -1.376630e-01 6.271531e-01
    outer loop
      vertex   -1.152029e+01 -1.071951e+01 1.095480e+01
      vertex   -1.126777e+01 -1.070000e+01 1.126777e+01
      vertex   -1.157804e+01 -1.070000e+01 1.088849e+01
    endloop
  endfacet
  facet normal -6.606663e-01 -6.438992e-01 3.858935e-01
    outer loop
      vertex   -1.152029e+01 -1.071951e+01 1.095480e+01
      vertex   -1.157804e+01 -1.070000e+01 1.088849e+01
      vertex   -1.175776e+01 -1.071951e+01 1.054824e+01
    endloop
  endfacet
  facet normal -8.782445e-01 -9.243396e-02 4.691936e-01
    outer loop
      vertex   -1.175776e+01 -1.071951e+01 1.054824e+01
      vertex   -1.157804e+01 -1.070000e+01 1.088849e+01
      vertex   -1.180899e+01 -1.070000e+01 1.045619e+01
    endloop
  endfacet
  facet normal -7.788045e-01 -5.401268e-01 3.189461e-01
    outer loop
      vertex   -1.175776e+01 -1.071951e+01 1.054824e+01
      vertex   -1.180899e+01 -1.070000e+01 1.045619e+01
      vertex   -1.184706e+01 -1.071951e+01 1.033017e+01
    endloop
  endfacet
  facet normal -9.563094e-01 -1.836045e-02 2.917795e-01
    outer loop
      vertex   -1.184706e+01 -1.071951e+01 1.033017e+01
      vertex   -1.180899e+01 -1.070000e+01 1.045619e+01
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
    endloop
  endfacet
  facet normal -9.558611e-01 -4.723250e-02 2.899976e-01
    outer loop
      vertex   -1.184706e+01 -1.071951e+01 1.033017e+01
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
      vertex   -1.191545e+01 -1.071951e+01 1.010476e+01
    endloop
  endfacet
  facet normal -6.131100e-01 -7.874322e-01 6.361374e-02
    outer loop
      vertex   -1.151634e+01 -1.119019e+01 9.613184e+00
      vertex   -1.154487e+01 -1.115203e+01 9.810530e+00
      vertex   -1.156506e+01 -1.115203e+01 9.615919e+00
    endloop
  endfacet
  facet normal -6.636451e-01 -7.448717e-01 6.885705e-02
    outer loop
      vertex   -1.156506e+01 -1.115203e+01 9.615919e+00
      vertex   -1.154487e+01 -1.115203e+01 9.810530e+00
      vertex   -1.162953e+01 -1.107542e+01 9.823386e+00
    endloop
  endfacet
  facet normal -6.636451e-01 -7.448717e-01 6.885705e-02
    outer loop
      vertex   -1.156506e+01 -1.115203e+01 9.615919e+00
      vertex   -1.162953e+01 -1.107542e+01 9.823386e+00
      vertex   -1.165056e+01 -1.107542e+01 9.620718e+00
    endloop
  endfacet
  facet normal -6.920248e-01 -7.182940e-01 7.180161e-02
    outer loop
      vertex   -1.165056e+01 -1.107542e+01 9.620718e+00
      vertex   -1.162953e+01 -1.107542e+01 9.823386e+00
      vertex   -1.174082e+01 -1.096651e+01 9.840287e+00
    endloop
  endfacet
  facet normal -6.920248e-01 -7.182940e-01 7.180161e-02
    outer loop
      vertex   -1.165056e+01 -1.107542e+01 9.620718e+00
      vertex   -1.174082e+01 -1.096651e+01 9.840287e+00
      vertex   -1.176295e+01 -1.096651e+01 9.627027e+00
    endloop
  endfacet
  facet normal -7.095035e-01 -7.008463e-01 7.361514e-02
    outer loop
      vertex   -1.176295e+01 -1.096651e+01 9.627027e+00
      vertex   -1.174082e+01 -1.096651e+01 9.840287e+00
      vertex   -1.179729e+01 -1.090844e+01 9.848862e+00
    endloop
  endfacet
  facet normal -7.095035e-01 -7.008463e-01 7.361514e-02
    outer loop
      vertex   -1.176295e+01 -1.096651e+01 9.627027e+00
      vertex   -1.179729e+01 -1.090844e+01 9.848862e+00
      vertex   -1.181997e+01 -1.090844e+01 9.630228e+00
    endloop
  endfacet
  facet normal -7.213845e-01 -6.884781e-01 7.484786e-02
    outer loop
      vertex   -1.181997e+01 -1.090844e+01 9.630228e+00
      vertex   -1.179729e+01 -1.090844e+01 9.848862e+00
      vertex   -1.184849e+01 -1.085394e+01 9.856638e+00
    endloop
  endfacet
  facet normal -7.213845e-01 -6.884781e-01 7.484786e-02
    outer loop
      vertex   -1.181997e+01 -1.090844e+01 9.630228e+00
      vertex   -1.184849e+01 -1.085394e+01 9.856638e+00
      vertex   -1.187168e+01 -1.085394e+01 9.633131e+00
    endloop
  endfacet
  facet normal -7.345663e-01 -6.742429e-01 7.621555e-02
    outer loop
      vertex   -1.187168e+01 -1.085394e+01 9.633131e+00
      vertex   -1.184849e+01 -1.085394e+01 9.856638e+00
      vertex   -1.189130e+01 -1.080658e+01 9.863138e+00
    endloop
  endfacet
  facet normal -7.838937e-01 -6.155449e-01 8.133355e-02
    outer loop
      vertex   -1.196197e+01 -1.071951e+01 9.873870e+00
      vertex   -1.194818e+01 -1.076831e+01 9.637424e+00
      vertex   -1.192424e+01 -1.076831e+01 9.868141e+00
    endloop
  endfacet
  facet normal -7.504510e-01 -6.563235e-01 7.786368e-02
    outer loop
      vertex   -1.192424e+01 -1.076831e+01 9.868141e+00
      vertex   -1.194818e+01 -1.076831e+01 9.637424e+00
      vertex   -1.191491e+01 -1.080658e+01 9.635557e+00
    endloop
  endfacet
  facet normal -5.899135e-01 -7.873822e-01 1.789732e-01
    outer loop
      vertex   -1.150623e+01 -1.115203e+01 1.000230e+01
      vertex   -1.145890e+01 -1.119019e+01 9.990452e+00
      vertex   -1.144943e+01 -1.115203e+01 1.018953e+01
    endloop
  endfacet
  facet normal -5.899135e-01 -7.873822e-01 1.789732e-01
    outer loop
      vertex   -1.144943e+01 -1.115203e+01 1.018953e+01
      vertex   -1.145890e+01 -1.119019e+01 9.990452e+00
      vertex   -1.140344e+01 -1.119019e+01 1.017326e+01
    endloop
  endfacet
  facet normal -5.705342e-01 -7.873355e-01 2.336526e-01
    outer loop
      vertex   -1.144943e+01 -1.115203e+01 1.018953e+01
      vertex   -1.140344e+01 -1.119019e+01 1.017326e+01
      vertex   -1.137526e+01 -1.115203e+01 1.037065e+01
    endloop
  endfacet
  facet normal -6.826453e-01 -7.007867e-01 2.071070e-01
    outer loop
      vertex   -1.169848e+01 -1.096651e+01 1.005044e+01
      vertex   -1.169007e+01 -1.090844e+01 1.027464e+01
      vertex   -1.175388e+01 -1.090844e+01 1.006431e+01
    endloop
  endfacet
  facet normal -6.940746e-01 -6.884176e-01 2.105745e-01
    outer loop
      vertex   -1.175388e+01 -1.090844e+01 1.006431e+01
      vertex   -1.169007e+01 -1.090844e+01 1.027464e+01
      vertex   -1.173889e+01 -1.085394e+01 1.029191e+01
    endloop
  endfacet
  facet normal -6.940746e-01 -6.884176e-01 2.105745e-01
    outer loop
      vertex   -1.175388e+01 -1.090844e+01 1.006431e+01
      vertex   -1.173889e+01 -1.085394e+01 1.029191e+01
      vertex   -1.180412e+01 -1.085394e+01 1.007689e+01
    endloop
  endfacet
  facet normal -7.067551e-01 -6.741815e-01 2.144216e-01
    outer loop
      vertex   -1.180412e+01 -1.085394e+01 1.007689e+01
      vertex   -1.173889e+01 -1.085394e+01 1.029191e+01
      vertex   -1.177969e+01 -1.080658e+01 1.030634e+01
    endloop
  endfacet
  facet normal -7.067551e-01 -6.741815e-01 2.144216e-01
    outer loop
      vertex   -1.180412e+01 -1.085394e+01 1.007689e+01
      vertex   -1.177969e+01 -1.080658e+01 1.030634e+01
      vertex   -1.184612e+01 -1.080658e+01 1.008740e+01
    endloop
  endfacet
  facet normal -7.220355e-01 -6.562611e-01 2.190575e-01
    outer loop
      vertex   -1.184612e+01 -1.080658e+01 1.008740e+01
      vertex   -1.177969e+01 -1.080658e+01 1.030634e+01
      vertex   -1.181110e+01 -1.076831e+01 1.031745e+01
    endloop
  endfacet
  facet normal -7.220355e-01 -6.562611e-01 2.190575e-01
    outer loop
      vertex   -1.184612e+01 -1.080658e+01 1.008740e+01
      vertex   -1.181110e+01 -1.076831e+01 1.031745e+01
      vertex   -1.187844e+01 -1.076831e+01 1.009549e+01
    endloop
  endfacet
  facet normal -7.542053e-01 -6.154811e-01 2.288175e-01
    outer loop
      vertex   -1.187844e+01 -1.076831e+01 1.009549e+01
      vertex   -1.181110e+01 -1.076831e+01 1.031745e+01
      vertex   -1.184706e+01 -1.071951e+01 1.033017e+01
    endloop
  endfacet
  facet normal -7.542053e-01 -6.154811e-01 2.288175e-01
    outer loop
      vertex   -1.187844e+01 -1.076831e+01 1.009549e+01
      vertex   -1.184706e+01 -1.071951e+01 1.033017e+01
      vertex   -1.191545e+01 -1.071951e+01 1.010476e+01
    endloop
  endfacet
  facet normal -6.175470e-01 -7.447646e-01 2.529059e-01
    outer loop
      vertex   -1.137526e+01 -1.115203e+01 1.037065e+01
      vertex   -1.145290e+01 -1.107542e+01 1.040669e+01
      vertex   -1.144943e+01 -1.115203e+01 1.018953e+01
    endloop
  endfacet
  facet normal -6.175470e-01 -7.447646e-01 2.529059e-01
    outer loop
      vertex   -1.144943e+01 -1.115203e+01 1.018953e+01
      vertex   -1.145290e+01 -1.107542e+01 1.040669e+01
      vertex   -1.153014e+01 -1.107542e+01 1.021808e+01
    endloop
  endfacet
  facet normal -6.385296e-01 -7.448164e-01 1.937228e-01
    outer loop
      vertex   -1.144943e+01 -1.115203e+01 1.018953e+01
      vertex   -1.153014e+01 -1.107542e+01 1.021808e+01
      vertex   -1.150623e+01 -1.115203e+01 1.000230e+01
    endloop
  endfacet
  facet normal -6.439473e-01 -7.181816e-01 2.637177e-01
    outer loop
      vertex   -1.153014e+01 -1.107542e+01 1.021808e+01
      vertex   -1.145290e+01 -1.107542e+01 1.040669e+01
      vertex   -1.155495e+01 -1.096651e+01 1.045408e+01
    endloop
  endfacet
  facet normal -6.019078e-01 -7.170102e-01 3.515728e-01
    outer loop
      vertex   -1.155495e+01 -1.096651e+01 1.045408e+01
      vertex   -1.145290e+01 -1.107542e+01 1.040669e+01
      vertex   -1.133881e+01 -1.096651e+01 1.082412e+01
    endloop
  endfacet
  facet normal -6.170540e-01 -6.995298e-01 3.604197e-01
    outer loop
      vertex   -1.155495e+01 -1.096651e+01 1.045408e+01
      vertex   -1.133881e+01 -1.096651e+01 1.082412e+01
      vertex   -1.138515e+01 -1.090844e+01 1.085749e+01
    endloop
  endfacet
  facet normal -5.383801e-01 -6.995993e-01 4.697954e-01
    outer loop
      vertex   -1.138515e+01 -1.090844e+01 1.085749e+01
      vertex   -1.133881e+01 -1.096651e+01 1.082412e+01
      vertex   -1.109636e+01 -1.090844e+01 1.118844e+01
    endloop
  endfacet
  facet normal -5.473627e-01 -6.872119e-01 4.776337e-01
    outer loop
      vertex   -1.138515e+01 -1.090844e+01 1.085749e+01
      vertex   -1.109636e+01 -1.090844e+01 1.118844e+01
      vertex   -1.113194e+01 -1.085394e+01 1.122608e+01
    endloop
  endfacet
  facet normal -4.465668e-01 -6.872337e-01 5.729641e-01
    outer loop
      vertex   -1.113194e+01 -1.085394e+01 1.122608e+01
      vertex   -1.109636e+01 -1.090844e+01 1.118844e+01
      vertex   -1.077778e+01 -1.085394e+01 1.150211e+01
    endloop
  endfacet
  facet normal -4.546966e-01 -6.729794e-01 5.833950e-01
    outer loop
      vertex   -1.113194e+01 -1.085394e+01 1.122608e+01
      vertex   -1.077778e+01 -1.085394e+01 1.150211e+01
      vertex   -1.080106e+01 -1.080658e+01 1.153860e+01
    endloop
  endfacet
  facet normal -3.675316e-01 -6.741982e-01 6.406070e-01
    outer loop
      vertex   -1.080106e+01 -1.080658e+01 1.153860e+01
      vertex   -1.077778e+01 -1.085394e+01 1.150211e+01
      vertex   -1.060254e+01 -1.080658e+01 1.165250e+01
    endloop
  endfacet
  facet normal -3.754782e-01 -6.562781e-01 6.544579e-01
    outer loop
      vertex   -1.080106e+01 -1.080658e+01 1.153860e+01
      vertex   -1.060254e+01 -1.080658e+01 1.165250e+01
      vertex   -1.061773e+01 -1.076831e+01 1.168215e+01
    endloop
  endfacet
  facet normal -3.123396e-01 -6.562946e-01 6.868197e-01
    outer loop
      vertex   -1.061773e+01 -1.076831e+01 1.168215e+01
      vertex   -1.060254e+01 -1.080658e+01 1.165250e+01
      vertex   -1.040651e+01 -1.076831e+01 1.177821e+01
    endloop
  endfacet
  facet normal -3.262572e-01 -6.155154e-01 7.174239e-01
    outer loop
      vertex   -1.061773e+01 -1.076831e+01 1.168215e+01
      vertex   -1.040651e+01 -1.076831e+01 1.177821e+01
      vertex   -1.042062e+01 -1.071951e+01 1.181366e+01
    endloop
  endfacet
  facet normal -2.567003e-01 -6.155369e-01 7.451304e-01
    outer loop
      vertex   -1.042062e+01 -1.071951e+01 1.181366e+01
      vertex   -1.040651e+01 -1.076831e+01 1.177821e+01
      vertex   -1.019778e+01 -1.071951e+01 1.189043e+01
    endloop
  endfacet
  facet normal -6.019078e-01 -7.170102e-01 3.515728e-01
    outer loop
      vertex   -1.133881e+01 -1.096651e+01 1.082412e+01
      vertex   -1.145290e+01 -1.107542e+01 1.040669e+01
      vertex   -1.124749e+01 -1.107542e+01 1.075836e+01
    endloop
  endfacet
  facet normal -5.773065e-01 -7.436472e-01 3.372033e-01
    outer loop
      vertex   -1.124749e+01 -1.107542e+01 1.075836e+01
      vertex   -1.145290e+01 -1.107542e+01 1.040669e+01
      vertex   -1.137526e+01 -1.115203e+01 1.037065e+01
    endloop
  endfacet
  facet normal -6.712582e-01 -6.883611e-01 2.749024e-01
    outer loop
      vertex   -1.173889e+01 -1.085394e+01 1.029191e+01
      vertex   -1.169007e+01 -1.090844e+01 1.027464e+01
      vertex   -1.165370e+01 -1.085394e+01 1.049992e+01
    endloop
  endfacet
  facet normal -6.835198e-01 -6.741241e-01 2.799239e-01
    outer loop
      vertex   -1.177969e+01 -1.080658e+01 1.030634e+01
      vertex   -1.173889e+01 -1.085394e+01 1.029191e+01
      vertex   -1.169295e+01 -1.080658e+01 1.051815e+01
    endloop
  endfacet
  facet normal -6.835198e-01 -6.741241e-01 2.799239e-01
    outer loop
      vertex   -1.169295e+01 -1.080658e+01 1.051815e+01
      vertex   -1.173889e+01 -1.085394e+01 1.029191e+01
      vertex   -1.165370e+01 -1.085394e+01 1.049992e+01
    endloop
  endfacet
  facet normal -6.387649e-01 -6.728856e-01 3.731010e-01
    outer loop
      vertex   -1.169295e+01 -1.080658e+01 1.051815e+01
      vertex   -1.165370e+01 -1.085394e+01 1.049992e+01
      vertex   -1.146229e+01 -1.080658e+01 1.091304e+01
    endloop
  endfacet
  facet normal -6.982952e-01 -6.562028e-01 2.859749e-01
    outer loop
      vertex   -1.181110e+01 -1.076831e+01 1.031745e+01
      vertex   -1.177969e+01 -1.080658e+01 1.030634e+01
      vertex   -1.172316e+01 -1.076831e+01 1.053217e+01
    endloop
  endfacet
  facet normal -6.982952e-01 -6.562028e-01 2.859749e-01
    outer loop
      vertex   -1.172316e+01 -1.076831e+01 1.053217e+01
      vertex   -1.177969e+01 -1.080658e+01 1.030634e+01
      vertex   -1.169295e+01 -1.080658e+01 1.051815e+01
    endloop
  endfacet
  facet normal -6.525206e-01 -6.549447e-01 3.811356e-01
    outer loop
      vertex   -1.172316e+01 -1.076831e+01 1.053217e+01
      vertex   -1.169295e+01 -1.080658e+01 1.051815e+01
      vertex   -1.148933e+01 -1.076831e+01 1.093251e+01
    endloop
  endfacet
  facet normal -6.525206e-01 -6.549447e-01 3.811356e-01
    outer loop
      vertex   -1.148933e+01 -1.076831e+01 1.093251e+01
      vertex   -1.169295e+01 -1.080658e+01 1.051815e+01
      vertex   -1.146229e+01 -1.080658e+01 1.091304e+01
    endloop
  endfacet
  facet normal -5.693314e-01 -6.550174e-01 4.968038e-01
    outer loop
      vertex   -1.148933e+01 -1.076831e+01 1.093251e+01
      vertex   -1.146229e+01 -1.080658e+01 1.091304e+01
      vertex   -1.118458e+01 -1.076831e+01 1.128175e+01
    endloop
  endfacet
  facet normal -7.294014e-01 -6.154214e-01 2.987139e-01
    outer loop
      vertex   -1.184706e+01 -1.071951e+01 1.033017e+01
      vertex   -1.181110e+01 -1.076831e+01 1.031745e+01
      vertex   -1.175776e+01 -1.071951e+01 1.054824e+01
    endloop
  endfacet
  facet normal -7.294014e-01 -6.154214e-01 2.987139e-01
    outer loop
      vertex   -1.175776e+01 -1.071951e+01 1.054824e+01
      vertex   -1.181110e+01 -1.076831e+01 1.031745e+01
      vertex   -1.172316e+01 -1.076831e+01 1.053217e+01
    endloop
  endfacet
  facet normal -6.814688e-01 -6.141344e-01 3.980442e-01
    outer loop
      vertex   -1.175776e+01 -1.071951e+01 1.054824e+01
      vertex   -1.172316e+01 -1.076831e+01 1.053217e+01
      vertex   -1.152029e+01 -1.071951e+01 1.095480e+01
    endloop
  endfacet
  facet normal -6.814688e-01 -6.141344e-01 3.980442e-01
    outer loop
      vertex   -1.152029e+01 -1.071951e+01 1.095480e+01
      vertex   -1.172316e+01 -1.076831e+01 1.053217e+01
      vertex   -1.148933e+01 -1.076831e+01 1.093251e+01
    endloop
  endfacet
  facet normal -5.945950e-01 -6.142088e-01 5.188491e-01
    outer loop
      vertex   -1.152029e+01 -1.071951e+01 1.095480e+01
      vertex   -1.148933e+01 -1.076831e+01 1.093251e+01
      vertex   -1.121079e+01 -1.071951e+01 1.130948e+01
    endloop
  endfacet
  facet normal -5.945950e-01 -6.142088e-01 5.188491e-01
    outer loop
      vertex   -1.121079e+01 -1.071951e+01 1.130948e+01
      vertex   -1.148933e+01 -1.076831e+01 1.093251e+01
      vertex   -1.118458e+01 -1.076831e+01 1.128175e+01
    endloop
  endfacet
  facet normal -4.851041e-01 -6.142318e-01 6.224092e-01
    outer loop
      vertex   -1.121079e+01 -1.071951e+01 1.130948e+01
      vertex   -1.118458e+01 -1.076831e+01 1.128175e+01
      vertex   -1.083951e+01 -1.071951e+01 1.159885e+01
    endloop
  endfacet
  facet normal -5.334743e-01 -7.863269e-01 3.116010e-01
    outer loop
      vertex   -1.133101e+01 -1.119019e+01 1.035010e+01
      vertex   -1.113842e+01 -1.119019e+01 1.067982e+01
      vertex   -1.117802e+01 -1.115203e+01 1.070833e+01
    endloop
  endfacet
  facet normal -4.654451e-01 -7.863852e-01 4.061516e-01
    outer loop
      vertex   -1.117802e+01 -1.115203e+01 1.070833e+01
      vertex   -1.113842e+01 -1.119019e+01 1.067982e+01
      vertex   -1.092096e+01 -1.115203e+01 1.100292e+01
    endloop
  endfacet
  facet normal -5.036941e-01 -7.437118e-01 4.395281e-01
    outer loop
      vertex   -1.117802e+01 -1.115203e+01 1.070833e+01
      vertex   -1.092096e+01 -1.115203e+01 1.100292e+01
      vertex   -1.097979e+01 -1.107542e+01 1.106514e+01
    endloop
  endfacet
  facet normal -4.109377e-01 -7.437318e-01 5.272505e-01
    outer loop
      vertex   -1.097979e+01 -1.107542e+01 1.106514e+01
      vertex   -1.092096e+01 -1.115203e+01 1.100292e+01
      vertex   -1.065864e+01 -1.107542e+01 1.131544e+01
    endloop
  endfacet
  facet normal -4.284536e-01 -7.170990e-01 5.497241e-01
    outer loop
      vertex   -1.097979e+01 -1.107542e+01 1.106514e+01
      vertex   -1.065864e+01 -1.107542e+01 1.131544e+01
      vertex   -1.071919e+01 -1.096651e+01 1.141032e+01
    endloop
  endfacet
  facet normal -3.462490e-01 -7.182517e-01 6.035115e-01
    outer loop
      vertex   -1.071919e+01 -1.096651e+01 1.141032e+01
      vertex   -1.065864e+01 -1.107542e+01 1.131544e+01
      vertex   -1.053316e+01 -1.096651e+01 1.151705e+01
    endloop
  endfacet
  facet normal -3.549933e-01 -7.008030e-01 6.187527e-01
    outer loop
      vertex   -1.071919e+01 -1.096651e+01 1.141032e+01
      vertex   -1.053316e+01 -1.096651e+01 1.151705e+01
      vertex   -1.055920e+01 -1.090844e+01 1.156788e+01
    endloop
  endfacet
  facet normal -2.952986e-01 -7.008187e-01 6.493472e-01
    outer loop
      vertex   -1.055920e+01 -1.090844e+01 1.156788e+01
      vertex   -1.053316e+01 -1.096651e+01 1.151705e+01
      vertex   -1.035904e+01 -1.090844e+01 1.165890e+01
    endloop
  endfacet
  facet normal -3.002431e-01 -6.884501e-01 6.602200e-01
    outer loop
      vertex   -1.055920e+01 -1.090844e+01 1.156788e+01
      vertex   -1.035904e+01 -1.090844e+01 1.165890e+01
      vertex   -1.037818e+01 -1.085394e+01 1.170703e+01
    endloop
  endfacet
  facet normal -2.362310e-01 -6.884705e-01 6.857137e-01
    outer loop
      vertex   -1.037818e+01 -1.085394e+01 1.170703e+01
      vertex   -1.035904e+01 -1.090844e+01 1.165890e+01
      vertex   -1.016562e+01 -1.085394e+01 1.178026e+01
    endloop
  endfacet
  facet normal -2.405476e-01 -6.742351e-01 6.982434e-01
    outer loop
      vertex   -1.037818e+01 -1.085394e+01 1.170703e+01
      vertex   -1.016562e+01 -1.085394e+01 1.178026e+01
      vertex   -1.017775e+01 -1.080658e+01 1.182181e+01
    endloop
  endfacet
  facet normal -1.730797e-01 -6.742405e-01 7.179437e-01
    outer loop
      vertex   -1.017775e+01 -1.080658e+01 1.182181e+01
      vertex   -1.016562e+01 -1.085394e+01 1.178026e+01
      vertex   -9.955265e+00 -1.080658e+01 1.187545e+01
    endloop
  endfacet
  facet normal -1.768224e-01 -6.563210e-01 7.334689e-01
    outer loop
      vertex   -1.017775e+01 -1.080658e+01 1.182181e+01
      vertex   -9.955265e+00 -1.080658e+01 1.187545e+01
      vertex   -9.961537e+00 -1.076831e+01 1.190818e+01
    endloop
  endfacet
  facet normal -1.068153e-01 -6.563192e-01 7.468839e-01
    outer loop
      vertex   -9.961537e+00 -1.076831e+01 1.190818e+01
      vertex   -9.955265e+00 -1.080658e+01 1.187545e+01
      vertex   -9.731880e+00 -1.076831e+01 1.194102e+01
    endloop
  endfacet
  facet normal -1.115753e-01 -6.155406e-01 7.801671e-01
    outer loop
      vertex   -9.961537e+00 -1.076831e+01 1.190818e+01
      vertex   -9.731880e+00 -1.076831e+01 1.194102e+01
      vertex   -9.735488e+00 -1.071951e+01 1.197901e+01
    endloop
  endfacet
  facet normal -5.383801e-01 -6.995993e-01 4.697954e-01
    outer loop
      vertex   -1.109636e+01 -1.090844e+01 1.118844e+01
      vertex   -1.133881e+01 -1.096651e+01 1.082412e+01
      vertex   -1.105712e+01 -1.096651e+01 1.114694e+01
    endloop
  endfacet
  facet normal -5.251624e-01 -7.170780e-01 4.582615e-01
    outer loop
      vertex   -1.105712e+01 -1.096651e+01 1.114694e+01
      vertex   -1.133881e+01 -1.096651e+01 1.082412e+01
      vertex   -1.124749e+01 -1.107542e+01 1.075836e+01
    endloop
  endfacet
  facet normal -4.654451e-01 -7.863852e-01 4.061516e-01
    outer loop
      vertex   -1.113842e+01 -1.119019e+01 1.067982e+01
      vertex   -1.088743e+01 -1.119019e+01 1.096746e+01
      vertex   -1.092096e+01 -1.115203e+01 1.100292e+01
    endloop
  endfacet
  facet normal -3.797308e-01 -7.864033e-01 4.872108e-01
    outer loop
      vertex   -1.092096e+01 -1.115203e+01 1.100292e+01
      vertex   -1.088743e+01 -1.119019e+01 1.096746e+01
      vertex   -1.061258e+01 -1.115203e+01 1.124327e+01
    endloop
  endfacet
  facet normal -4.109377e-01 -7.437318e-01 5.272505e-01
    outer loop
      vertex   -1.092096e+01 -1.115203e+01 1.100292e+01
      vertex   -1.061258e+01 -1.115203e+01 1.124327e+01
      vertex   -1.065864e+01 -1.107542e+01 1.131544e+01
    endloop
  endfacet
  facet normal -3.320510e-01 -7.448315e-01 5.787644e-01
    outer loop
      vertex   -1.065864e+01 -1.107542e+01 1.131544e+01
      vertex   -1.061258e+01 -1.115203e+01 1.124327e+01
      vertex   -1.048185e+01 -1.107542e+01 1.141687e+01
    endloop
  endfacet
  facet normal -3.462490e-01 -7.182517e-01 6.035115e-01
    outer loop
      vertex   -1.065864e+01 -1.107542e+01 1.131544e+01
      vertex   -1.048185e+01 -1.107542e+01 1.141687e+01
      vertex   -1.053316e+01 -1.096651e+01 1.151705e+01
    endloop
  endfacet
  facet normal -2.880244e-01 -7.182671e-01 6.333517e-01
    outer loop
      vertex   -1.053316e+01 -1.096651e+01 1.151705e+01
      vertex   -1.048185e+01 -1.107542e+01 1.141687e+01
      vertex   -1.033792e+01 -1.096651e+01 1.160584e+01
    endloop
  endfacet
  facet normal -2.952986e-01 -7.008187e-01 6.493472e-01
    outer loop
      vertex   -1.053316e+01 -1.096651e+01 1.151705e+01
      vertex   -1.033792e+01 -1.096651e+01 1.160584e+01
      vertex   -1.035904e+01 -1.090844e+01 1.165890e+01
    endloop
  endfacet
  facet normal -2.323405e-01 -7.008388e-01 6.744204e-01
    outer loop
      vertex   -1.035904e+01 -1.090844e+01 1.165890e+01
      vertex   -1.033792e+01 -1.096651e+01 1.160584e+01
      vertex   -1.015111e+01 -1.090844e+01 1.173054e+01
    endloop
  endfacet
  facet normal -2.362310e-01 -6.884705e-01 6.857137e-01
    outer loop
      vertex   -1.035904e+01 -1.090844e+01 1.165890e+01
      vertex   -1.015111e+01 -1.090844e+01 1.173054e+01
      vertex   -1.016562e+01 -1.085394e+01 1.178026e+01
    endloop
  endfacet
  facet normal -1.699738e-01 -6.884757e-01 7.050603e-01
    outer loop
      vertex   -1.016562e+01 -1.085394e+01 1.178026e+01
      vertex   -1.015111e+01 -1.090844e+01 1.173054e+01
      vertex   -9.947116e+00 -1.085394e+01 1.183293e+01
    endloop
  endfacet
  facet normal -1.730797e-01 -6.742405e-01 7.179437e-01
    outer loop
      vertex   -1.016562e+01 -1.085394e+01 1.178026e+01
      vertex   -9.947116e+00 -1.085394e+01 1.183293e+01
      vertex   -9.955265e+00 -1.080658e+01 1.187545e+01
    endloop
  endfacet
  facet normal -1.045544e-01 -6.742387e-01 7.310749e-01
    outer loop
      vertex   -9.955265e+00 -1.080658e+01 1.187545e+01
      vertex   -9.947116e+00 -1.085394e+01 1.183293e+01
      vertex   -9.728729e+00 -1.080658e+01 1.190785e+01
    endloop
  endfacet
  facet normal -1.068153e-01 -6.563192e-01 7.468839e-01
    outer loop
      vertex   -9.955265e+00 -1.080658e+01 1.187545e+01
      vertex   -9.728729e+00 -1.080658e+01 1.190785e+01
      vertex   -9.731880e+00 -1.076831e+01 1.194102e+01
    endloop
  endfacet
  facet normal -4.465668e-01 -6.872337e-01 5.729641e-01
    outer loop
      vertex   -1.077778e+01 -1.085394e+01 1.150211e+01
      vertex   -1.109636e+01 -1.090844e+01 1.118844e+01
      vertex   -1.074991e+01 -1.090844e+01 1.145846e+01
    endloop
  endfacet
  facet normal -4.392378e-01 -6.996208e-01 5.635608e-01
    outer loop
      vertex   -1.074991e+01 -1.090844e+01 1.145846e+01
      vertex   -1.109636e+01 -1.090844e+01 1.118844e+01
      vertex   -1.105712e+01 -1.096651e+01 1.114694e+01
    endloop
  endfacet
  facet normal -3.797308e-01 -7.864033e-01 4.872108e-01
    outer loop
      vertex   -1.088743e+01 -1.119019e+01 1.096746e+01
      vertex   -1.058633e+01 -1.119019e+01 1.120214e+01
      vertex   -1.061258e+01 -1.115203e+01 1.124327e+01
    endloop
  endfacet
  facet normal -3.067685e-01 -7.873958e-01 5.346970e-01
    outer loop
      vertex   -1.061258e+01 -1.115203e+01 1.124327e+01
      vertex   -1.058633e+01 -1.119019e+01 1.120214e+01
      vertex   -1.044282e+01 -1.115203e+01 1.134067e+01
    endloop
  endfacet
  facet normal -3.320510e-01 -7.448315e-01 5.787644e-01
    outer loop
      vertex   -1.061258e+01 -1.115203e+01 1.124327e+01
      vertex   -1.044282e+01 -1.115203e+01 1.134067e+01
      vertex   -1.048185e+01 -1.107542e+01 1.141687e+01
    endloop
  endfacet
  facet normal -2.762134e-01 -7.448461e-01 6.073799e-01
    outer loop
      vertex   -1.048185e+01 -1.107542e+01 1.141687e+01
      vertex   -1.044282e+01 -1.115203e+01 1.134067e+01
      vertex   -1.029631e+01 -1.107542e+01 1.150125e+01
    endloop
  endfacet
  facet normal -2.880244e-01 -7.182671e-01 6.333517e-01
    outer loop
      vertex   -1.048185e+01 -1.107542e+01 1.141687e+01
      vertex   -1.029631e+01 -1.107542e+01 1.150125e+01
      vertex   -1.033792e+01 -1.096651e+01 1.160584e+01
    endloop
  endfacet
  facet normal -2.266168e-01 -7.182866e-01 6.578063e-01
    outer loop
      vertex   -1.033792e+01 -1.096651e+01 1.160584e+01
      vertex   -1.029631e+01 -1.107542e+01 1.150125e+01
      vertex   -1.013510e+01 -1.096651e+01 1.167571e+01
    endloop
  endfacet
  facet normal -2.323405e-01 -7.008388e-01 6.744204e-01
    outer loop
      vertex   -1.033792e+01 -1.096651e+01 1.160584e+01
      vertex   -1.013510e+01 -1.096651e+01 1.167571e+01
      vertex   -1.015111e+01 -1.090844e+01 1.173054e+01
    endloop
  endfacet
  facet normal -1.671744e-01 -7.008439e-01 6.934483e-01
    outer loop
      vertex   -1.015111e+01 -1.090844e+01 1.173054e+01
      vertex   -1.013510e+01 -1.096651e+01 1.167571e+01
      vertex   -9.937367e+00 -1.090844e+01 1.178206e+01
    endloop
  endfacet
  facet normal -1.699738e-01 -6.884757e-01 7.050603e-01
    outer loop
      vertex   -1.015111e+01 -1.090844e+01 1.173054e+01
      vertex   -9.937367e+00 -1.090844e+01 1.178206e+01
      vertex   -9.947116e+00 -1.085394e+01 1.183293e+01
    endloop
  endfacet
  facet normal -1.026782e-01 -6.884740e-01 7.179560e-01
    outer loop
      vertex   -9.947116e+00 -1.085394e+01 1.183293e+01
      vertex   -9.937367e+00 -1.090844e+01 1.178206e+01
      vertex   -9.724635e+00 -1.085394e+01 1.186475e+01
    endloop
  endfacet
  facet normal -1.045544e-01 -6.742387e-01 7.310749e-01
    outer loop
      vertex   -9.947116e+00 -1.085394e+01 1.183293e+01
      vertex   -9.724635e+00 -1.085394e+01 1.186475e+01
      vertex   -9.728729e+00 -1.080658e+01 1.190785e+01
    endloop
  endfacet
  facet normal -3.675316e-01 -6.741982e-01 6.406070e-01
    outer loop
      vertex   -1.060254e+01 -1.080658e+01 1.165250e+01
      vertex   -1.077778e+01 -1.085394e+01 1.150211e+01
      vertex   -1.058281e+01 -1.085394e+01 1.161397e+01
    endloop
  endfacet
  facet normal -3.609371e-01 -6.884341e-01 6.291128e-01
    outer loop
      vertex   -1.058281e+01 -1.085394e+01 1.161397e+01
      vertex   -1.077778e+01 -1.085394e+01 1.150211e+01
      vertex   -1.074991e+01 -1.090844e+01 1.145846e+01
    endloop
  endfacet
  facet normal -3.057289e-01 -6.742145e-01 6.722831e-01
    outer loop
      vertex   -1.060254e+01 -1.080658e+01 1.165250e+01
      vertex   -1.058281e+01 -1.085394e+01 1.161397e+01
      vertex   -1.039419e+01 -1.080658e+01 1.174725e+01
    endloop
  endfacet
  facet normal -3.123396e-01 -6.562946e-01 6.868197e-01
    outer loop
      vertex   -1.060254e+01 -1.080658e+01 1.165250e+01
      vertex   -1.039419e+01 -1.080658e+01 1.174725e+01
      vertex   -1.040651e+01 -1.076831e+01 1.177821e+01
    endloop
  endfacet
  facet normal -2.457492e-01 -6.563156e-01 7.133423e-01
    outer loop
      vertex   -1.040651e+01 -1.076831e+01 1.177821e+01
      vertex   -1.039419e+01 -1.080658e+01 1.174725e+01
      vertex   -1.018709e+01 -1.076831e+01 1.185380e+01
    endloop
  endfacet
  facet normal -2.567003e-01 -6.155369e-01 7.451304e-01
    outer loop
      vertex   -1.040651e+01 -1.076831e+01 1.177821e+01
      vertex   -1.018709e+01 -1.076831e+01 1.185380e+01
      vertex   -1.019778e+01 -1.071951e+01 1.189043e+01
    endloop
  endfacet
  facet normal -1.847022e-01 -6.155424e-01 7.661545e-01
    outer loop
      vertex   -1.019778e+01 -1.071951e+01 1.189043e+01
      vertex   -1.018709e+01 -1.076831e+01 1.185380e+01
      vertex   -9.968720e+00 -1.071951e+01 1.194565e+01
    endloop
  endfacet
  facet normal -1.444621e-01 -7.874302e-01 5.992365e-01
    outer loop
      vertex   -9.880125e+00 -1.119019e+01 1.148339e+01
      vertex   -9.889311e+00 -1.115203e+01 1.153132e+01
      vertex   -1.006589e+01 -1.119019e+01 1.143861e+01
    endloop
  endfacet
  facet normal -1.444621e-01 -7.874302e-01 5.992365e-01
    outer loop
      vertex   -1.006589e+01 -1.119019e+01 1.143861e+01
      vertex   -9.889311e+00 -1.115203e+01 1.153132e+01
      vertex   -1.007957e+01 -1.115203e+01 1.148545e+01
    endloop
  endfacet
  facet normal -2.007751e-01 -7.874258e-01 5.827949e-01
    outer loop
      vertex   -1.006589e+01 -1.119019e+01 1.143861e+01
      vertex   -1.007957e+01 -1.115203e+01 1.148545e+01
      vertex   -1.024661e+01 -1.119019e+01 1.137635e+01
    endloop
  endfacet
  facet normal -1.563692e-01 -7.448695e-01 6.486278e-01
    outer loop
      vertex   -1.007957e+01 -1.115203e+01 1.148545e+01
      vertex   -9.889311e+00 -1.115203e+01 1.153132e+01
      vertex   -9.905429e+00 -1.107542e+01 1.161542e+01
    endloop
  endfacet
  facet normal -9.445995e-02 -7.448679e-01 6.604915e-01
    outer loop
      vertex   -9.905429e+00 -1.107542e+01 1.161542e+01
      vertex   -9.889311e+00 -1.115203e+01 1.153132e+01
      vertex   -9.703690e+00 -1.107542e+01 1.164427e+01
    endloop
  endfacet
  facet normal -9.849934e-02 -7.182900e-01 6.887361e-01
    outer loop
      vertex   -9.905429e+00 -1.107542e+01 1.161542e+01
      vertex   -9.703690e+00 -1.107542e+01 1.164427e+01
      vertex   -9.714335e+00 -1.096651e+01 1.175633e+01
    endloop
  endfacet
  facet normal -9.445995e-02 -7.448679e-01 6.604915e-01
    outer loop
      vertex   -9.703690e+00 -1.107542e+01 1.164427e+01
      vertex   -9.889311e+00 -1.115203e+01 1.153132e+01
      vertex   -9.695593e+00 -1.115203e+01 1.155902e+01
    endloop
  endfacet
  facet normal -8.726711e-02 -7.874287e-01 6.101970e-01
    outer loop
      vertex   -9.695593e+00 -1.115203e+01 1.155902e+01
      vertex   -9.889311e+00 -1.115203e+01 1.153132e+01
      vertex   -9.880125e+00 -1.119019e+01 1.148339e+01
    endloop
  endfacet
  facet normal -9.523198e-01 -3.051016e-01 -8.903473e-17
    outer loop
      vertex   -1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   -1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
    endloop
  endfacet
  facet normal -8.571656e-01 -5.150409e-01 8.657003e-05
    outer loop
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   -1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -8.177242e-01 -5.756102e-01 1.691309e-04
    outer loop
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -7.062675e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 8.310975e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -6.681428e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
      vertex   -1.195203e+01 -1.076831e+01 8.310975e+00
      vertex   -1.187542e+01 -1.085394e+01 8.310975e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -2.696938e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 8.310975e+00
      vertex   -1.195203e+01 -1.076831e+01 8.310975e+00
      vertex   -1.187542e+01 -1.085394e+01 7.716772e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -2.288072e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 8.310975e+00
      vertex   -1.187542e+01 -1.085394e+01 7.716772e+00
      vertex   -1.176651e+01 -1.096651e+01 7.716772e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -2.358563e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 7.716772e+00
      vertex   -1.187542e+01 -1.085394e+01 7.716772e+00
      vertex   -1.176651e+01 -1.096651e+01 7.122746e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.869876e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 7.716772e+00
      vertex   -1.176651e+01 -1.096651e+01 7.122746e+00
      vertex   -1.165394e+01 -1.107542e+01 7.122746e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -2.509788e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.122746e+00
      vertex   -1.176651e+01 -1.096651e+01 7.122746e+00
      vertex   -1.165394e+01 -1.107542e+01 6.528873e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -2.440296e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.122746e+00
      vertex   -1.165394e+01 -1.107542e+01 6.528873e+00
      vertex   -1.156831e+01 -1.115203e+01 6.528873e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -3.238801e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 6.528873e+00
      vertex   -1.165394e+01 -1.107542e+01 6.528873e+00
      vertex   -1.156831e+01 -1.115203e+01 5.935131e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -3.051386e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 6.528873e+00
      vertex   -1.156831e+01 -1.115203e+01 5.935131e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -1.581819e-14
    outer loop
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 5.935131e+00
      vertex   -1.156831e+01 -1.115203e+01 4.747953e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -2.279019e-14
    outer loop
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   -1.156831e+01 -1.115203e+01 3.561030e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -2.483076e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 3.561030e+00
      vertex   -1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 4.747953e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -1.473602e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 3.561030e+00
      vertex   -1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 3.561030e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.553983e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 3.561030e+00
      vertex   -1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   -1.176651e+01 -1.096651e+01 4.747953e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.353023e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 3.561030e+00
      vertex   -1.176651e+01 -1.096651e+01 4.747953e+00
      vertex   -1.176651e+01 -1.096651e+01 3.561030e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -1.398262e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 3.561030e+00
      vertex   -1.176651e+01 -1.096651e+01 4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 4.747953e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -8.640686e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 3.561030e+00
      vertex   -1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 3.561030e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -9.040097e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 3.561030e+00
      vertex   -1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   -1.195203e+01 -1.076831e+01 4.747953e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 8.776740e-16
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 3.561030e+00
      vertex   -1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   -1.195203e+01 -1.076831e+01 3.561030e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 6.647617e-16
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 3.561030e+00
      vertex   -1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -2.358107e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 3.561030e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 2.374183e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -3.279358e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 2.374183e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 4.808019e-16
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -3.228139e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 2.374183e+00
      vertex   -1.195203e+01 -1.076831e+01 4.808019e-16
      vertex   -1.187542e+01 -1.085394e+01 3.729229e-16
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 2.787943e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 3.729229e-16
      vertex   -1.195203e+01 -1.076831e+01 4.808019e-16
      vertex   -1.187542e+01 -1.085394e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 2.688583e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 3.729229e-16
      vertex   -1.187542e+01 -1.085394e+01 -2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -1.613432e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 -2.374183e+00
      vertex   -1.187542e+01 -1.085394e+01 -2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.561021e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 -2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 -4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -2.686501e-16
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   -1.176651e+01 -1.096651e+01 -4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -2.785784e-16
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -4.605123e-16
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -2.357834e-15
    outer loop
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   -1.195203e+01 -1.076831e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 2.947147e-15
    outer loop
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 -2.374183e+00
      vertex   -1.195203e+01 -1.076831e+01 4.808019e-16
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 2.787943e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 4.808019e-16
      vertex   -1.195203e+01 -1.076831e+01 -2.374183e+00
      vertex   -1.187542e+01 -1.085394e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -4.985061e-16
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   -1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 2.859357e-17
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   -1.187542e+01 -1.085394e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -2.230743e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   -1.195203e+01 -1.076831e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -2.232416e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 -2.374183e+00
      vertex   -1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 8.726863e-18
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   -1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   -1.187542e+01 -1.085394e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 8.040777e-16
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   -1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   -1.176651e+01 -1.096651e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -2.151242e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   -1.176651e+01 -1.096651e+01 -4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 7.797697e-16
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   -1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   -1.176651e+01 -1.096651e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -5.273925e-16
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   -1.156831e+01 -1.115203e+01 -9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -5.247304e-16
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   -1.156831e+01 -1.115203e+01 -9.500000e+00
      vertex   -1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -5.150402e-01 -8.571645e-01 1.593807e-03
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   -1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   -1.150684e+01 -1.119781e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -3.050974e-01 -9.523068e-01 5.226111e-03
    outer loop
      vertex   -1.150684e+01 -1.119781e+01 -9.500000e+00
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
    endloop
  endfacet
  facet normal -5.829516e-01 -8.125069e-01 -1.793632e-04
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -9.218993e-16
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 1.382608e-15
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 -2.374183e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 -1.510629e-17
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 1.496677e-15
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 -2.374183e+00
      vertex   -1.156831e+01 -1.115203e+01 -1.510629e-17
      vertex   -1.165394e+01 -1.107542e+01 7.660904e-17
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -7.982279e-15
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.660904e-17
      vertex   -1.156831e+01 -1.115203e+01 -1.510629e-17
      vertex   -1.165394e+01 -1.107542e+01 2.374183e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -8.323991e-15
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.660904e-17
      vertex   -1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 2.374183e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.245362e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 2.374183e+00
      vertex   -1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 3.561030e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -1.294281e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 3.561030e+00
      vertex   -1.187542e+01 -1.085394e+01 3.561030e+00
    endloop
  endfacet
  facet normal -3.051016e-01 -9.523198e-01 -4.421329e-15
    outer loop
      vertex   -1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   -1.150684e+01 -1.119781e+01 9.500000e+00
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -5.150409e-01 -8.571656e-01 -8.657003e-05
    outer loop
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.150684e+01 -1.119781e+01 9.500000e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 2.539390e-13
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 8.905377e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -9.204117e-15
    outer loop
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 8.905377e+00
      vertex   -1.156831e+01 -1.115203e+01 8.310975e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -1.473269e-14
    outer loop
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 8.310975e+00
      vertex   -1.156831e+01 -1.115203e+01 7.716772e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -1.594690e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 7.716772e+00
      vertex   -1.156831e+01 -1.115203e+01 8.310975e+00
      vertex   -1.165394e+01 -1.107542e+01 8.310975e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -1.419041e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 7.716772e+00
      vertex   -1.165394e+01 -1.107542e+01 8.310975e+00
      vertex   -1.165394e+01 -1.107542e+01 7.716772e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.462067e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.716772e+00
      vertex   -1.165394e+01 -1.107542e+01 8.310975e+00
      vertex   -1.176651e+01 -1.096651e+01 8.310975e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -8.313037e-15
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.716772e+00
      vertex   -1.176651e+01 -1.096651e+01 8.310975e+00
      vertex   -1.176651e+01 -1.096651e+01 7.716772e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -8.593952e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 7.716772e+00
      vertex   -1.176651e+01 -1.096651e+01 8.310975e+00
      vertex   -1.187542e+01 -1.085394e+01 8.310975e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 2.748898e-13
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   -1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 8.905377e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 2.144323e-13
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 8.905377e+00
      vertex   -1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   -1.165394e+01 -1.107542e+01 8.905377e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -9.963481e-15
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 8.905377e+00
      vertex   -1.165394e+01 -1.107542e+01 8.905377e+00
      vertex   -1.156831e+01 -1.115203e+01 8.310975e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -9.956635e-15
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 8.310975e+00
      vertex   -1.165394e+01 -1.107542e+01 8.905377e+00
      vertex   -1.165394e+01 -1.107542e+01 8.310975e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 2.241314e-13
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   -1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   -1.165394e+01 -1.107542e+01 8.905377e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 1.494917e-13
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 8.905377e+00
      vertex   -1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   -1.176651e+01 -1.096651e+01 8.905377e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.039001e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 8.905377e+00
      vertex   -1.176651e+01 -1.096651e+01 8.905377e+00
      vertex   -1.165394e+01 -1.107542e+01 8.310975e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -8.384789e-15
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 8.310975e+00
      vertex   -1.176651e+01 -1.096651e+01 8.905377e+00
      vertex   -1.176651e+01 -1.096651e+01 8.310975e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 1.546516e-13
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   -1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   -1.176651e+01 -1.096651e+01 8.905377e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 7.113243e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 8.905377e+00
      vertex   -1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   -1.187542e+01 -1.085394e+01 8.905377e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -8.521310e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 8.905377e+00
      vertex   -1.187542e+01 -1.085394e+01 8.905377e+00
      vertex   -1.176651e+01 -1.096651e+01 8.310975e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 2.068248e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 8.310975e+00
      vertex   -1.187542e+01 -1.085394e+01 8.905377e+00
      vertex   -1.187542e+01 -1.085394e+01 8.310975e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 7.440580e-14
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   -1.187542e+01 -1.085394e+01 8.905377e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 3.515263e-14
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 8.905377e+00
      vertex   -1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 1.992696e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 8.905377e+00
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
      vertex   -1.187542e+01 -1.085394e+01 8.310975e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 3.662716e-14
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   -1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
    endloop
  endfacet
  facet normal -8.570961e-01 -5.149991e-01 -1.273621e-02
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
      vertex   -1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   -1.199781e+01 -1.070684e+01 9.500000e+00
    endloop
  endfacet
  facet normal -9.514903e-01 -3.048358e-01 -4.172969e-02
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 8.905377e+00
      vertex   -1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -2.393500e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.122746e+00
      vertex   -1.156831e+01 -1.115203e+01 6.528873e+00
      vertex   -1.156831e+01 -1.115203e+01 7.122746e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -2.210954e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 7.122746e+00
      vertex   -1.156831e+01 -1.115203e+01 6.528873e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -1.473588e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 7.122746e+00
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 7.716772e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -2.330482e-14
    outer loop
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 3.561030e+00
      vertex   -1.156831e+01 -1.115203e+01 2.374183e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -2.506719e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 2.374183e+00
      vertex   -1.156831e+01 -1.115203e+01 3.561030e+00
      vertex   -1.165394e+01 -1.107542e+01 3.561030e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -2.207047e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 2.374183e+00
      vertex   -1.165394e+01 -1.107542e+01 3.561030e+00
      vertex   -1.165394e+01 -1.107542e+01 2.374183e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -2.293065e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   -1.165394e+01 -1.107542e+01 3.561030e+00
      vertex   -1.176651e+01 -1.096651e+01 3.561030e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -9.417755e-15
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   -1.156831e+01 -1.115203e+01 -1.510629e-17
      vertex   -1.156831e+01 -1.115203e+01 2.374183e+00
    endloop
  endfacet
  facet normal -6.159732e-01 -7.877671e-01 -8.627980e-15
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 2.374183e+00
      vertex   -1.156831e+01 -1.115203e+01 -1.510629e-17
      vertex   -1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 7.881666e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 7.716772e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 7.122746e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -8.397568e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 7.122746e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 6.528873e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -8.447195e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 7.122746e+00
      vertex   -1.195203e+01 -1.076831e+01 6.528873e+00
      vertex   -1.187542e+01 -1.085394e+01 6.528873e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -2.135737e-14
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 6.528873e+00
      vertex   -1.195203e+01 -1.076831e+01 6.528873e+00
      vertex   -1.187542e+01 -1.085394e+01 5.935131e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -2.122220e-14
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 6.528873e+00
      vertex   -1.187542e+01 -1.085394e+01 5.935131e+00
      vertex   -1.176651e+01 -1.096651e+01 5.935131e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -1.078848e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 5.935131e+00
      vertex   -1.187542e+01 -1.085394e+01 5.935131e+00
      vertex   -1.176651e+01 -1.096651e+01 4.747953e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.036929e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 5.935131e+00
      vertex   -1.176651e+01 -1.096651e+01 4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 4.747953e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -4.989795e-16
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -9.985453e-16
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   -1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   -1.156831e+01 -1.115203e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 9.977849e-16
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   -1.156831e+01 -1.115203e+01 -2.374183e+00
      vertex   -1.165394e+01 -1.107542e+01 7.660904e-17
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -5.203402e-16
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 -2.374183e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 1.560748e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 -2.374183e+00
      vertex   -1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 2.214875e-16
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 1.613150e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 -2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 2.214875e-16
      vertex   -1.187542e+01 -1.085394e+01 3.729229e-16
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -4.266799e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 3.729229e-16
      vertex   -1.176651e+01 -1.096651e+01 2.214875e-16
      vertex   -1.187542e+01 -1.085394e+01 2.374183e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -4.343316e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 3.729229e-16
      vertex   -1.187542e+01 -1.085394e+01 2.374183e+00
      vertex   -1.195203e+01 -1.076831e+01 2.374183e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -2.230815e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 2.374183e+00
      vertex   -1.187542e+01 -1.085394e+01 2.374183e+00
      vertex   -1.195203e+01 -1.076831e+01 3.561030e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 1.040280e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 2.214875e-16
      vertex   -1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   -1.165394e+01 -1.107542e+01 7.660904e-17
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -7.491883e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 2.214875e-16
      vertex   -1.176651e+01 -1.096651e+01 2.374183e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -7.318427e-15
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 2.214875e-16
      vertex   -1.165394e+01 -1.107542e+01 7.660904e-17
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -2.565112e-16
    outer loop
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   -1.195203e+01 -1.076831e+01 5.935131e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -1.173837e-16
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 5.935131e+00
      vertex   -1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 4.747953e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 1.875783e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 5.935131e+00
      vertex   -1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   -1.187542e+01 -1.085394e+01 5.935131e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 2.045913e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 5.935131e+00
      vertex   -1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   -1.176651e+01 -1.096651e+01 4.747953e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -8.802745e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 3.561030e+00
      vertex   -1.187542e+01 -1.085394e+01 2.374183e+00
      vertex   -1.187542e+01 -1.085394e+01 3.561030e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -8.570303e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 3.561030e+00
      vertex   -1.187542e+01 -1.085394e+01 2.374183e+00
      vertex   -1.176651e+01 -1.096651e+01 2.374183e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -6.445954e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 5.935131e+00
      vertex   -1.195203e+01 -1.076831e+01 6.528873e+00
      vertex   -1.195203e+01 -1.076831e+01 5.935131e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -6.556556e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 5.935131e+00
      vertex   -1.195203e+01 -1.076831e+01 6.528873e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -8.206808e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 7.716772e+00
      vertex   -1.195203e+01 -1.076831e+01 8.310975e+00
      vertex   -1.195203e+01 -1.076831e+01 7.716772e+00
    endloop
  endfacet
  facet normal -7.877671e-01 -6.159732e-01 -7.879328e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 7.716772e+00
      vertex   -1.195203e+01 -1.076831e+01 8.310975e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -1.772405e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   -1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 5.935131e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -1.760692e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 5.935131e+00
      vertex   -1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   -1.156831e+01 -1.115203e+01 5.935131e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -2.393895e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 5.935131e+00
      vertex   -1.156831e+01 -1.115203e+01 5.935131e+00
      vertex   -1.165394e+01 -1.107542e+01 6.528873e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.865774e-14
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   -1.165394e+01 -1.107542e+01 5.935131e+00
      vertex   -1.176651e+01 -1.096651e+01 5.935131e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -1.248187e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 5.935131e+00
      vertex   -1.165394e+01 -1.107542e+01 5.935131e+00
      vertex   -1.176651e+01 -1.096651e+01 6.528873e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -1.290095e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 5.935131e+00
      vertex   -1.176651e+01 -1.096651e+01 6.528873e+00
      vertex   -1.187542e+01 -1.085394e+01 6.528873e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -6.658539e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 6.528873e+00
      vertex   -1.176651e+01 -1.096651e+01 6.528873e+00
      vertex   -1.187542e+01 -1.085394e+01 7.122746e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -7.391345e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 6.528873e+00
      vertex   -1.187542e+01 -1.085394e+01 7.122746e+00
      vertex   -1.195203e+01 -1.076831e+01 7.122746e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 8.210413e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 7.122746e+00
      vertex   -1.187542e+01 -1.085394e+01 7.122746e+00
      vertex   -1.195203e+01 -1.076831e+01 7.716772e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -2.495850e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 6.528873e+00
      vertex   -1.165394e+01 -1.107542e+01 5.935131e+00
      vertex   -1.165394e+01 -1.107542e+01 6.528873e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -2.142823e-14
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 7.122746e+00
      vertex   -1.176651e+01 -1.096651e+01 6.528873e+00
      vertex   -1.176651e+01 -1.096651e+01 7.122746e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -2.086835e-14
    outer loop
      vertex   -1.176651e+01 -1.096651e+01 7.122746e+00
      vertex   -1.176651e+01 -1.096651e+01 6.528873e+00
      vertex   -1.165394e+01 -1.107542e+01 6.528873e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -1.595164e-14
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 7.716772e+00
      vertex   -1.165394e+01 -1.107542e+01 7.716772e+00
      vertex   -1.156831e+01 -1.115203e+01 7.122746e+00
    endloop
  endfacet
  facet normal -6.667929e-01 -7.452430e-01 -3.278615e-15
    outer loop
      vertex   -1.156831e+01 -1.115203e+01 7.122746e+00
      vertex   -1.165394e+01 -1.107542e+01 7.716772e+00
      vertex   -1.165394e+01 -1.107542e+01 7.122746e+00
    endloop
  endfacet
  facet normal -6.953375e-01 -7.186833e-01 -3.949189e-15
    outer loop
      vertex   -1.165394e+01 -1.107542e+01 7.716772e+00
      vertex   -1.176651e+01 -1.096651e+01 7.716772e+00
      vertex   -1.165394e+01 -1.107542e+01 7.122746e+00
    endloop
  endfacet
  facet normal -7.452430e-01 -6.667929e-01 -8.437985e-15
    outer loop
      vertex   -1.195203e+01 -1.076831e+01 7.716772e+00
      vertex   -1.187542e+01 -1.085394e+01 7.122746e+00
      vertex   -1.187542e+01 -1.085394e+01 7.716772e+00
    endloop
  endfacet
  facet normal -7.186833e-01 -6.953375e-01 -8.456878e-15
    outer loop
      vertex   -1.187542e+01 -1.085394e+01 7.716772e+00
      vertex   -1.187542e+01 -1.085394e+01 7.122746e+00
      vertex   -1.176651e+01 -1.096651e+01 7.122746e+00
    endloop
  endfacet
  facet normal -9.342319e-02 -3.037672e-01 -9.481548e-01
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   -9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
    endloop
  endfacet
  facet normal -9.408344e-02 -3.790053e-02 -9.948426e-01
    outer loop
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
      vertex   -9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   -9.873870e+00 -1.071951e+01 -1.196197e+01
    endloop
  endfacet
  facet normal -1.657253e-01 -5.439417e-01 -8.225950e-01
    outer loop
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
      vertex   -9.873870e+00 -1.071951e+01 -1.196197e+01
      vertex   -1.010476e+01 -1.071951e+01 -1.191545e+01
    endloop
  endfacet
  facet normal -1.556509e-01 -6.155307e-01 -7.725896e-01
    outer loop
      vertex   -1.010476e+01 -1.071951e+01 -1.191545e+01
      vertex   -9.873870e+00 -1.071951e+01 -1.196197e+01
      vertex   -9.868141e+00 -1.076831e+01 -1.192424e+01
    endloop
  endfacet
  facet normal -1.556509e-01 -6.155307e-01 -7.725896e-01
    outer loop
      vertex   -1.010476e+01 -1.071951e+01 -1.191545e+01
      vertex   -9.868141e+00 -1.076831e+01 -1.192424e+01
      vertex   -1.009549e+01 -1.076831e+01 -1.187844e+01
    endloop
  endfacet
  facet normal -1.490108e-01 -6.563096e-01 -7.396306e-01
    outer loop
      vertex   -1.009549e+01 -1.076831e+01 -1.187844e+01
      vertex   -9.868141e+00 -1.076831e+01 -1.192424e+01
      vertex   -9.863138e+00 -1.080658e+01 -1.189130e+01
    endloop
  endfacet
  facet normal -1.490108e-01 -6.563096e-01 -7.396306e-01
    outer loop
      vertex   -1.009549e+01 -1.076831e+01 -1.187844e+01
      vertex   -9.863138e+00 -1.080658e+01 -1.189130e+01
      vertex   -1.008740e+01 -1.080658e+01 -1.184612e+01
    endloop
  endfacet
  facet normal -1.458568e-01 -6.742293e-01 -7.239756e-01
    outer loop
      vertex   -1.008740e+01 -1.080658e+01 -1.184612e+01
      vertex   -9.863138e+00 -1.080658e+01 -1.189130e+01
      vertex   -9.856638e+00 -1.085394e+01 -1.184849e+01
    endloop
  endfacet
  facet normal -1.458568e-01 -6.742293e-01 -7.239756e-01
    outer loop
      vertex   -1.008740e+01 -1.080658e+01 -1.184612e+01
      vertex   -9.856638e+00 -1.085394e+01 -1.184849e+01
      vertex   -1.007689e+01 -1.085394e+01 -1.180412e+01
    endloop
  endfacet
  facet normal -1.432395e-01 -6.884647e-01 -7.109844e-01
    outer loop
      vertex   -1.007689e+01 -1.085394e+01 -1.180412e+01
      vertex   -9.856638e+00 -1.085394e+01 -1.184849e+01
      vertex   -9.848862e+00 -1.090844e+01 -1.179729e+01
    endloop
  endfacet
  facet normal -1.432395e-01 -6.884647e-01 -7.109844e-01
    outer loop
      vertex   -1.007689e+01 -1.085394e+01 -1.180412e+01
      vertex   -9.848862e+00 -1.090844e+01 -1.179729e+01
      vertex   -1.006431e+01 -1.090844e+01 -1.175388e+01
    endloop
  endfacet
  facet normal -1.408805e-01 -7.008331e-01 -6.992751e-01
    outer loop
      vertex   -1.006431e+01 -1.090844e+01 -1.175388e+01
      vertex   -9.848862e+00 -1.090844e+01 -1.179729e+01
      vertex   -9.840287e+00 -1.096651e+01 -1.174082e+01
    endloop
  endfacet
  facet normal -1.408805e-01 -7.008331e-01 -6.992751e-01
    outer loop
      vertex   -1.006431e+01 -1.090844e+01 -1.175388e+01
      vertex   -9.840287e+00 -1.096651e+01 -1.174082e+01
      vertex   -1.005044e+01 -1.096651e+01 -1.169848e+01
    endloop
  endfacet
  facet normal -1.374100e-01 -7.182811e-01 -6.820490e-01
    outer loop
      vertex   -1.005044e+01 -1.096651e+01 -1.169848e+01
      vertex   -9.840287e+00 -1.096651e+01 -1.174082e+01
      vertex   -9.823386e+00 -1.107542e+01 -1.162953e+01
    endloop
  endfacet
  facet normal -1.374100e-01 -7.182811e-01 -6.820490e-01
    outer loop
      vertex   -1.005044e+01 -1.096651e+01 -1.169848e+01
      vertex   -9.823386e+00 -1.107542e+01 -1.162953e+01
      vertex   -1.002310e+01 -1.107542e+01 -1.158929e+01
    endloop
  endfacet
  facet normal -1.317751e-01 -7.448594e-01 -6.540793e-01
    outer loop
      vertex   -1.002310e+01 -1.107542e+01 -1.158929e+01
      vertex   -9.823386e+00 -1.107542e+01 -1.162953e+01
      vertex   -9.810530e+00 -1.115203e+01 -1.154487e+01
    endloop
  endfacet
  facet normal -1.317751e-01 -7.448594e-01 -6.540793e-01
    outer loop
      vertex   -1.002310e+01 -1.107542e+01 -1.158929e+01
      vertex   -9.810530e+00 -1.115203e+01 -1.154487e+01
      vertex   -1.000230e+01 -1.115203e+01 -1.150623e+01
    endloop
  endfacet
  facet normal -1.217410e-01 -7.874211e-01 -6.042741e-01
    outer loop
      vertex   -1.000230e+01 -1.115203e+01 -1.150623e+01
      vertex   -9.810530e+00 -1.115203e+01 -1.154487e+01
      vertex   -9.803203e+00 -1.119019e+01 -1.149662e+01
    endloop
  endfacet
  facet normal -1.217410e-01 -7.874211e-01 -6.042741e-01
    outer loop
      vertex   -1.000230e+01 -1.115203e+01 -1.150623e+01
      vertex   -9.803203e+00 -1.119019e+01 -1.149662e+01
      vertex   -9.990452e+00 -1.119019e+01 -1.145890e+01
    endloop
  endfacet
  facet normal -9.778547e-02 -8.688242e-01 -4.853684e-01
    outer loop
      vertex   -9.990452e+00 -1.119019e+01 -1.145890e+01
      vertex   -9.803203e+00 -1.119019e+01 -1.149662e+01
      vertex   -9.890099e+00 -1.120000e+01 -1.146156e+01
    endloop
  endfacet
  facet normal -1.004701e-01 -9.382106e-01 -3.311594e-01
    outer loop
      vertex   -9.990452e+00 -1.119019e+01 -1.145890e+01
      vertex   -9.890099e+00 -1.120000e+01 -1.146156e+01
      vertex   -1.017326e+01 -1.119019e+01 -1.140344e+01
    endloop
  endfacet
  facet normal -9.949641e-02 -9.400847e-01 -3.261002e-01
    outer loop
      vertex   -1.017326e+01 -1.119019e+01 -1.140344e+01
      vertex   -9.890099e+00 -1.120000e+01 -1.146156e+01
      vertex   -1.026495e+01 -1.120000e+01 -1.134719e+01
    endloop
  endfacet
  facet normal -1.868833e-01 -8.699627e-01 -4.563328e-01
    outer loop
      vertex   -1.017326e+01 -1.119019e+01 -1.140344e+01
      vertex   -1.026495e+01 -1.120000e+01 -1.134719e+01
      vertex   -1.035010e+01 -1.119019e+01 -1.133101e+01
    endloop
  endfacet
  facet normal -1.670974e-01 -9.350133e-01 -3.127757e-01
    outer loop
      vertex   -1.035010e+01 -1.119019e+01 -1.133101e+01
      vertex   -1.026495e+01 -1.120000e+01 -1.134719e+01
      vertex   -1.061079e+01 -1.120000e+01 -1.116243e+01
    endloop
  endfacet
  facet normal -2.881172e-01 -8.207765e-01 -4.932691e-01
    outer loop
      vertex   -1.035010e+01 -1.119019e+01 -1.133101e+01
      vertex   -1.061079e+01 -1.120000e+01 -1.116243e+01
      vertex   -1.067982e+01 -1.119019e+01 -1.113842e+01
    endloop
  endfacet
  facet normal -2.301717e-01 -9.315879e-01 -2.813627e-01
    outer loop
      vertex   -1.067982e+01 -1.119019e+01 -1.113842e+01
      vertex   -1.061079e+01 -1.120000e+01 -1.116243e+01
      vertex   -1.091421e+01 -1.120000e+01 -1.091421e+01
    endloop
  endfacet
  facet normal -3.626466e-01 -8.341303e-01 -4.155888e-01
    outer loop
      vertex   -1.067982e+01 -1.119019e+01 -1.113842e+01
      vertex   -1.091421e+01 -1.120000e+01 -1.091421e+01
      vertex   -1.096746e+01 -1.119019e+01 -1.088743e+01
    endloop
  endfacet
  facet normal -2.904112e-01 -9.268216e-01 -2.380402e-01
    outer loop
      vertex   -1.096746e+01 -1.119019e+01 -1.088743e+01
      vertex   -1.091421e+01 -1.120000e+01 -1.091421e+01
      vertex   -1.116272e+01 -1.120000e+01 -1.061103e+01
    endloop
  endfacet
  facet normal -4.139428e-01 -8.512132e-01 -3.226260e-01
    outer loop
      vertex   -1.096746e+01 -1.119019e+01 -1.088743e+01
      vertex   -1.116272e+01 -1.120000e+01 -1.061103e+01
      vertex   -1.120214e+01 -1.119019e+01 -1.058633e+01
    endloop
  endfacet
  facet normal -3.545041e-01 -9.126666e-01 -2.033875e-01
    outer loop
      vertex   -1.120214e+01 -1.119019e+01 -1.058633e+01
      vertex   -1.116272e+01 -1.120000e+01 -1.061103e+01
      vertex   -1.129724e+01 -1.119019e+01 -1.042057e+01
    endloop
  endfacet
  facet normal -5.346970e-01 -7.873958e-01 -3.067685e-01
    outer loop
      vertex   -1.120214e+01 -1.119019e+01 -1.058633e+01
      vertex   -1.129724e+01 -1.119019e+01 -1.042057e+01
      vertex   -1.134067e+01 -1.115203e+01 -1.044282e+01
    endloop
  endfacet
  facet normal -5.611322e-01 -7.874090e-01 -2.551817e-01
    outer loop
      vertex   -1.134067e+01 -1.115203e+01 -1.044282e+01
      vertex   -1.129724e+01 -1.119019e+01 -1.042057e+01
      vertex   -1.142169e+01 -1.115203e+01 -1.026465e+01
    endloop
  endfacet
  facet normal -6.073799e-01 -7.448461e-01 -2.762134e-01
    outer loop
      vertex   -1.134067e+01 -1.115203e+01 -1.044282e+01
      vertex   -1.142169e+01 -1.115203e+01 -1.026465e+01
      vertex   -1.150125e+01 -1.107542e+01 -1.029631e+01
    endloop
  endfacet
  facet normal -6.308304e-01 -7.448647e-01 -2.173235e-01
    outer loop
      vertex   -1.150125e+01 -1.107542e+01 -1.029631e+01
      vertex   -1.142169e+01 -1.115203e+01 -1.026465e+01
      vertex   -1.156765e+01 -1.107542e+01 -1.010356e+01
    endloop
  endfacet
  facet normal -6.578063e-01 -7.182866e-01 -2.266168e-01
    outer loop
      vertex   -1.150125e+01 -1.107542e+01 -1.029631e+01
      vertex   -1.156765e+01 -1.107542e+01 -1.010356e+01
      vertex   -1.167571e+01 -1.096651e+01 -1.013510e+01
    endloop
  endfacet
  facet normal -6.763651e-01 -7.182917e-01 -1.630560e-01
    outer loop
      vertex   -1.167571e+01 -1.096651e+01 -1.013510e+01
      vertex   -1.156765e+01 -1.107542e+01 -1.010356e+01
      vertex   -1.172597e+01 -1.096651e+01 -9.926617e+00
    endloop
  endfacet
  facet normal -6.934483e-01 -7.008439e-01 -1.671744e-01
    outer loop
      vertex   -1.167571e+01 -1.096651e+01 -1.013510e+01
      vertex   -1.172597e+01 -1.096651e+01 -9.926617e+00
      vertex   -1.178206e+01 -1.090844e+01 -9.937367e+00
    endloop
  endfacet
  facet normal -7.061316e-01 -7.008422e-01 -1.009871e-01
    outer loop
      vertex   -1.178206e+01 -1.090844e+01 -9.937367e+00
      vertex   -1.172597e+01 -1.096651e+01 -9.926617e+00
      vertex   -1.181319e+01 -1.090844e+01 -9.719737e+00
    endloop
  endfacet
  facet normal -7.179560e-01 -6.884740e-01 -1.026782e-01
    outer loop
      vertex   -1.178206e+01 -1.090844e+01 -9.937367e+00
      vertex   -1.181319e+01 -1.090844e+01 -9.719737e+00
      vertex   -1.186475e+01 -1.085394e+01 -9.724635e+00
    endloop
  endfacet
  facet normal -7.244426e-01 -6.884757e-01 -3.441191e-02
    outer loop
      vertex   -1.186475e+01 -1.085394e+01 -9.724635e+00
      vertex   -1.181319e+01 -1.090844e+01 -9.719737e+00
      vertex   -1.187542e+01 -1.085394e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.376801e-01 -6.742404e-01 -3.504071e-02
    outer loop
      vertex   -1.186475e+01 -1.085394e+01 -9.724635e+00
      vertex   -1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   -1.190785e+01 -1.080658e+01 -9.728729e+00
    endloop
  endfacet
  facet normal -7.448516e-01 -6.664427e-01 -3.240909e-02
    outer loop
      vertex   -1.190785e+01 -1.080658e+01 -9.728729e+00
      vertex   -1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   -1.195203e+01 -1.076831e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.536321e-01 -6.563209e-01 -3.579845e-02
    outer loop
      vertex   -1.190785e+01 -1.080658e+01 -9.728729e+00
      vertex   -1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   -1.194102e+01 -1.076831e+01 -9.731880e+00
    endloop
  endfacet
  facet normal -7.872162e-01 -6.155424e-01 -3.739373e-02
    outer loop
      vertex   -1.194102e+01 -1.076831e+01 -9.731880e+00
      vertex   -1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.872162e-01 -6.155424e-01 -3.739373e-02
    outer loop
      vertex   -1.194102e+01 -1.076831e+01 -9.731880e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.197901e+01 -1.071951e+01 -9.735488e+00
    endloop
  endfacet
  facet normal -8.564560e-01 -5.146145e-01 -4.068271e-02
    outer loop
      vertex   -1.197901e+01 -1.071951e+01 -9.735488e+00
      vertex   -1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   -1.199781e+01 -1.070684e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -9.506323e-01 -3.045610e-01 -5.950433e-02
    outer loop
      vertex   -1.197901e+01 -1.071951e+01 -9.735488e+00
      vertex   -1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   -1.200000e+01 -1.070000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -1.005396e-01 2.256693e-01 -9.690021e-01
    outer loop
      vertex   -9.873870e+00 -1.071951e+01 -1.196197e+01
      vertex   -9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   -9.639563e+00 -1.071951e+01 -1.198628e+01
    endloop
  endfacet
  facet normal -2.404018e-02 -5.148920e-01 -8.569179e-01
    outer loop
      vertex   -9.639563e+00 -1.071951e+01 -1.198628e+01
      vertex   -9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   -9.500000e+00 -1.071951e+01 -1.199019e+01
    endloop
  endfacet
  facet normal -2.209481e-02 -6.158228e-01 -7.875748e-01
    outer loop
      vertex   -9.639563e+00 -1.071951e+01 -1.198628e+01
      vertex   -9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -9.500000e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal -1.588740e-02 -6.667088e-01 -7.451490e-01
    outer loop
      vertex   -9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   -9.635557e+00 -1.080658e+01 -1.191491e+01
      vertex   -9.500000e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal -2.115140e-02 -6.565950e-01 -7.539467e-01
    outer loop
      vertex   -9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   -9.635557e+00 -1.080658e+01 -1.191491e+01
      vertex   -9.637424e+00 -1.076831e+01 -1.194818e+01
    endloop
  endfacet
  facet normal -2.209481e-02 -6.158228e-01 -7.875748e-01
    outer loop
      vertex   -9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   -9.637424e+00 -1.076831e+01 -1.194818e+01
      vertex   -9.639563e+00 -1.071951e+01 -1.198628e+01
    endloop
  endfacet
  facet normal -8.133355e-02 -6.155449e-01 -7.838937e-01
    outer loop
      vertex   -9.639563e+00 -1.071951e+01 -1.198628e+01
      vertex   -9.637424e+00 -1.076831e+01 -1.194818e+01
      vertex   -9.873870e+00 -1.071951e+01 -1.196197e+01
    endloop
  endfacet
  facet normal -1.499825e-02 -6.952593e-01 -7.186025e-01
    outer loop
      vertex   -9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   -9.630228e+00 -1.090844e+01 -1.181997e+01
      vertex   -9.500000e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -2.033153e-02 -6.887413e-01 -7.247221e-01
    outer loop
      vertex   -9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   -9.630228e+00 -1.090844e+01 -1.181997e+01
      vertex   -9.633131e+00 -1.085394e+01 -1.187168e+01
    endloop
  endfacet
  facet normal -2.070334e-02 -6.745101e-01 -7.379752e-01
    outer loop
      vertex   -9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   -9.633131e+00 -1.085394e+01 -1.187168e+01
      vertex   -9.635557e+00 -1.080658e+01 -1.191491e+01
    endloop
  endfacet
  facet normal -7.621555e-02 -6.742429e-01 -7.345663e-01
    outer loop
      vertex   -9.635557e+00 -1.080658e+01 -1.191491e+01
      vertex   -9.633131e+00 -1.085394e+01 -1.187168e+01
      vertex   -9.863138e+00 -1.080658e+01 -1.189130e+01
    endloop
  endfacet
  facet normal -7.786368e-02 -6.563235e-01 -7.504510e-01
    outer loop
      vertex   -9.635557e+00 -1.080658e+01 -1.191491e+01
      vertex   -9.863138e+00 -1.080658e+01 -1.189130e+01
      vertex   -9.868141e+00 -1.076831e+01 -1.192424e+01
    endloop
  endfacet
  facet normal -1.999642e-02 -7.011054e-01 -7.127772e-01
    outer loop
      vertex   -9.630228e+00 -1.090844e+01 -1.181997e+01
      vertex   -9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   -9.627027e+00 -1.096651e+01 -1.176295e+01
    endloop
  endfacet
  facet normal -1.950346e-02 -7.185466e-01 -6.952053e-01
    outer loop
      vertex   -9.627027e+00 -1.096651e+01 -1.176295e+01
      vertex   -9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   -9.500000e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal -1.950346e-02 -7.185466e-01 -6.952053e-01
    outer loop
      vertex   -9.627027e+00 -1.096651e+01 -1.176295e+01
      vertex   -9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   -9.620718e+00 -1.107542e+01 -1.165056e+01
    endloop
  endfacet
  facet normal -1.870310e-02 -7.451127e-01 -6.666763e-01
    outer loop
      vertex   -9.620718e+00 -1.107542e+01 -1.165056e+01
      vertex   -9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   -9.500000e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal -1.870310e-02 -7.451127e-01 -6.666763e-01
    outer loop
      vertex   -9.620718e+00 -1.107542e+01 -1.165056e+01
      vertex   -9.500000e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.615919e+00 -1.115203e+01 -1.156506e+01
    endloop
  endfacet
  facet normal -1.727808e-02 -7.876495e-01 -6.158812e-01
    outer loop
      vertex   -9.615919e+00 -1.115203e+01 -1.156506e+01
      vertex   -9.500000e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal -1.727808e-02 -7.876495e-01 -6.158812e-01
    outer loop
      vertex   -9.615919e+00 -1.115203e+01 -1.156506e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -9.613184e+00 -1.119019e+01 -1.151634e+01
    endloop
  endfacet
  facet normal -1.444757e-02 -8.570762e-01 -5.149871e-01
    outer loop
      vertex   -9.613184e+00 -1.119019e+01 -1.151634e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -9.500000e+00 -1.119781e+01 -1.150684e+01
    endloop
  endfacet
  facet normal -3.843645e-02 -9.516161e-01 -3.048761e-01
    outer loop
      vertex   -9.613184e+00 -1.119019e+01 -1.151634e+01
      vertex   -9.500000e+00 -1.119781e+01 -1.150684e+01
      vertex   -9.500000e+00 -1.120000e+01 -1.150000e+01
    endloop
  endfacet
  facet normal -3.308564e-02 -9.413566e-01 -3.357872e-01
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   -9.890099e+00 -1.120000e+01 -1.146156e+01
      vertex   -9.613184e+00 -1.119019e+01 -1.151634e+01
    endloop
  endfacet
  facet normal -3.653608e-02 -9.352358e-01 -3.521352e-01
    outer loop
      vertex   -9.613184e+00 -1.119019e+01 -1.151634e+01
      vertex   -9.890099e+00 -1.120000e+01 -1.146156e+01
      vertex   -9.803203e+00 -1.119019e+01 -1.149662e+01
    endloop
  endfacet
  facet normal -6.361374e-02 -7.874322e-01 -6.131100e-01
    outer loop
      vertex   -9.613184e+00 -1.119019e+01 -1.151634e+01
      vertex   -9.803203e+00 -1.119019e+01 -1.149662e+01
      vertex   -9.810530e+00 -1.115203e+01 -1.154487e+01
    endloop
  endfacet
  facet normal -2.845023e-01 -9.465158e-01 -1.522045e-01
    outer loop
      vertex   -1.116272e+01 -1.120000e+01 -1.061103e+01
      vertex   -1.134765e+01 -1.120000e+01 -1.026535e+01
      vertex   -1.129724e+01 -1.119019e+01 -1.042057e+01
    endloop
  endfacet
  facet normal -4.288166e-01 -8.820927e-01 -1.950096e-01
    outer loop
      vertex   -1.129724e+01 -1.119019e+01 -1.042057e+01
      vertex   -1.134765e+01 -1.120000e+01 -1.026535e+01
      vertex   -1.137635e+01 -1.119019e+01 -1.024661e+01
    endloop
  endfacet
  facet normal -5.611322e-01 -7.874090e-01 -2.551817e-01
    outer loop
      vertex   -1.129724e+01 -1.119019e+01 -1.042057e+01
      vertex   -1.137635e+01 -1.119019e+01 -1.024661e+01
      vertex   -1.142169e+01 -1.115203e+01 -1.026465e+01
    endloop
  endfacet
  facet normal -5.827949e-01 -7.874258e-01 -2.007751e-01
    outer loop
      vertex   -1.142169e+01 -1.115203e+01 -1.026465e+01
      vertex   -1.137635e+01 -1.119019e+01 -1.024661e+01
      vertex   -1.148545e+01 -1.115203e+01 -1.007957e+01
    endloop
  endfacet
  facet normal -6.308304e-01 -7.448647e-01 -2.173235e-01
    outer loop
      vertex   -1.142169e+01 -1.115203e+01 -1.026465e+01
      vertex   -1.148545e+01 -1.115203e+01 -1.007957e+01
      vertex   -1.156765e+01 -1.107542e+01 -1.010356e+01
    endloop
  endfacet
  facet normal -6.486278e-01 -7.448695e-01 -1.563692e-01
    outer loop
      vertex   -1.156765e+01 -1.107542e+01 -1.010356e+01
      vertex   -1.148545e+01 -1.115203e+01 -1.007957e+01
      vertex   -1.161542e+01 -1.107542e+01 -9.905429e+00
    endloop
  endfacet
  facet normal -6.763651e-01 -7.182917e-01 -1.630560e-01
    outer loop
      vertex   -1.156765e+01 -1.107542e+01 -1.010356e+01
      vertex   -1.161542e+01 -1.107542e+01 -9.905429e+00
      vertex   -1.172597e+01 -1.096651e+01 -9.926617e+00
    endloop
  endfacet
  facet normal -6.887361e-01 -7.182900e-01 -9.849934e-02
    outer loop
      vertex   -1.172597e+01 -1.096651e+01 -9.926617e+00
      vertex   -1.161542e+01 -1.107542e+01 -9.905429e+00
      vertex   -1.175633e+01 -1.096651e+01 -9.714335e+00
    endloop
  endfacet
  facet normal -7.061316e-01 -7.008422e-01 -1.009871e-01
    outer loop
      vertex   -1.172597e+01 -1.096651e+01 -9.926617e+00
      vertex   -1.175633e+01 -1.096651e+01 -9.714335e+00
      vertex   -1.181319e+01 -1.090844e+01 -9.719737e+00
    endloop
  endfacet
  facet normal -7.125113e-01 -7.008439e-01 -3.384516e-02
    outer loop
      vertex   -1.181319e+01 -1.090844e+01 -9.719737e+00
      vertex   -1.175633e+01 -1.096651e+01 -9.714335e+00
      vertex   -1.176651e+01 -1.096651e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -7.183365e-01 -6.950020e-01 -3.106396e-02
    outer loop
      vertex   -1.181319e+01 -1.090844e+01 -9.719737e+00
      vertex   -1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   -1.187542e+01 -1.085394e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -3.996311e-01 -9.062785e-01 -1.376745e-01
    outer loop
      vertex   -1.137635e+01 -1.119019e+01 -1.024661e+01
      vertex   -1.134765e+01 -1.120000e+01 -1.026535e+01
      vertex   -1.143861e+01 -1.119019e+01 -1.006589e+01
    endloop
  endfacet
  facet normal -3.056615e-01 -9.476078e-01 -9.279314e-02
    outer loop
      vertex   -1.143861e+01 -1.119019e+01 -1.006589e+01
      vertex   -1.134765e+01 -1.120000e+01 -1.026535e+01
      vertex   -1.146154e+01 -1.120000e+01 -9.890201e+00
    endloop
  endfacet
  facet normal -4.481226e-01 -8.874206e-01 -1.080320e-01
    outer loop
      vertex   -1.143861e+01 -1.119019e+01 -1.006589e+01
      vertex   -1.146154e+01 -1.120000e+01 -9.890201e+00
      vertex   -1.148339e+01 -1.119019e+01 -9.880125e+00
    endloop
  endfacet
  facet normal -4.322850e-01 -8.996153e-01 -6.182307e-02
    outer loop
      vertex   -1.148339e+01 -1.119019e+01 -9.880125e+00
      vertex   -1.146154e+01 -1.120000e+01 -9.890201e+00
      vertex   -1.151044e+01 -1.119019e+01 -9.690978e+00
    endloop
  endfacet
  facet normal -6.101970e-01 -7.874287e-01 -8.726711e-02
    outer loop
      vertex   -1.148339e+01 -1.119019e+01 -9.880125e+00
      vertex   -1.151044e+01 -1.119019e+01 -9.690978e+00
      vertex   -1.155902e+01 -1.115203e+01 -9.695593e+00
    endloop
  endfacet
  facet normal -6.157097e-01 -7.874301e-01 -2.924696e-02
    outer loop
      vertex   -1.155902e+01 -1.115203e+01 -9.695593e+00
      vertex   -1.151044e+01 -1.119019e+01 -9.690978e+00
      vertex   -1.156831e+01 -1.115203e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -6.664587e-01 -7.448695e-01 -3.165761e-02
    outer loop
      vertex   -1.155902e+01 -1.115203e+01 -9.695593e+00
      vertex   -1.156831e+01 -1.115203e+01 -9.500000e+00
      vertex   -1.165394e+01 -1.107542e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -3.049638e-01 -9.518896e-01 -3.005630e-02
    outer loop
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.150684e+01 -1.119781e+01 -9.500000e+00
      vertex   -1.146154e+01 -1.120000e+01 -9.890201e+00
    endloop
  endfacet
  facet normal -3.192603e-01 -9.471353e-01 -3.174269e-02
    outer loop
      vertex   -1.146154e+01 -1.120000e+01 -9.890201e+00
      vertex   -1.150684e+01 -1.119781e+01 -9.500000e+00
      vertex   -1.151044e+01 -1.119019e+01 -9.690978e+00
    endloop
  endfacet
  facet normal -5.148868e-01 -8.569092e-01 -2.445775e-02
    outer loop
      vertex   -1.150684e+01 -1.119781e+01 -9.500000e+00
      vertex   -1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   -1.151044e+01 -1.119019e+01 -9.690978e+00
    endloop
  endfacet
  facet normal -6.157097e-01 -7.874301e-01 -2.924696e-02
    outer loop
      vertex   -1.151044e+01 -1.119019e+01 -9.690978e+00
      vertex   -1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   -1.156831e+01 -1.115203e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -6.664587e-01 -7.448695e-01 -3.165761e-02
    outer loop
      vertex   -1.155902e+01 -1.115203e+01 -9.695593e+00
      vertex   -1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   -1.164427e+01 -1.107542e+01 -9.703690e+00
    endloop
  endfacet
  facet normal -6.949586e-01 -7.182916e-01 -3.301138e-02
    outer loop
      vertex   -1.164427e+01 -1.107542e+01 -9.703690e+00
      vertex   -1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   -1.176651e+01 -1.096651e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -6.949586e-01 -7.182916e-01 -3.301138e-02
    outer loop
      vertex   -1.164427e+01 -1.107542e+01 -9.703690e+00
      vertex   -1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   -1.175633e+01 -1.096651e+01 -9.714335e+00
    endloop
  endfacet
  facet normal -9.888763e-01 1.123611e-01 -9.746066e-02
    outer loop
      vertex   -1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   -1.195193e+01 -1.070000e+01 -9.987751e+00
      vertex   -1.197901e+01 -1.071951e+01 -9.735488e+00
    endloop
  endfacet
  facet normal -9.005422e-01 -4.152551e-01 -1.287907e-01
    outer loop
      vertex   -1.197901e+01 -1.071951e+01 -9.735488e+00
      vertex   -1.195193e+01 -1.070000e+01 -9.987751e+00
      vertex   -1.194565e+01 -1.071951e+01 -9.968720e+00
    endloop
  endfacet
  facet normal -7.801671e-01 -6.155406e-01 -1.115753e-01
    outer loop
      vertex   -1.197901e+01 -1.071951e+01 -9.735488e+00
      vertex   -1.194565e+01 -1.071951e+01 -9.968720e+00
      vertex   -1.190818e+01 -1.076831e+01 -9.961537e+00
    endloop
  endfacet
  facet normal -7.661545e-01 -6.155424e-01 -1.847022e-01
    outer loop
      vertex   -1.190818e+01 -1.076831e+01 -9.961537e+00
      vertex   -1.194565e+01 -1.071951e+01 -9.968720e+00
      vertex   -1.185380e+01 -1.076831e+01 -1.018709e+01
    endloop
  endfacet
  facet normal -7.334689e-01 -6.563210e-01 -1.768224e-01
    outer loop
      vertex   -1.190818e+01 -1.076831e+01 -9.961537e+00
      vertex   -1.185380e+01 -1.076831e+01 -1.018709e+01
      vertex   -1.182181e+01 -1.080658e+01 -1.017775e+01
    endloop
  endfacet
  facet normal -7.133423e-01 -6.563156e-01 -2.457492e-01
    outer loop
      vertex   -1.182181e+01 -1.080658e+01 -1.017775e+01
      vertex   -1.185380e+01 -1.076831e+01 -1.018709e+01
      vertex   -1.174725e+01 -1.080658e+01 -1.039419e+01
    endloop
  endfacet
  facet normal -6.982434e-01 -6.742351e-01 -2.405476e-01
    outer loop
      vertex   -1.182181e+01 -1.080658e+01 -1.017775e+01
      vertex   -1.174725e+01 -1.080658e+01 -1.039419e+01
      vertex   -1.170703e+01 -1.085394e+01 -1.037818e+01
    endloop
  endfacet
  facet normal -6.722831e-01 -6.742145e-01 -3.057289e-01
    outer loop
      vertex   -1.170703e+01 -1.085394e+01 -1.037818e+01
      vertex   -1.174725e+01 -1.080658e+01 -1.039419e+01
      vertex   -1.161397e+01 -1.085394e+01 -1.058281e+01
    endloop
  endfacet
  facet normal -6.602200e-01 -6.884501e-01 -3.002431e-01
    outer loop
      vertex   -1.170703e+01 -1.085394e+01 -1.037818e+01
      vertex   -1.161397e+01 -1.085394e+01 -1.058281e+01
      vertex   -1.156788e+01 -1.090844e+01 -1.055920e+01
    endloop
  endfacet
  facet normal -6.291128e-01 -6.884341e-01 -3.609371e-01
    outer loop
      vertex   -1.156788e+01 -1.090844e+01 -1.055920e+01
      vertex   -1.161397e+01 -1.085394e+01 -1.058281e+01
      vertex   -1.145846e+01 -1.090844e+01 -1.074991e+01
    endloop
  endfacet
  facet normal -6.187527e-01 -7.008030e-01 -3.549933e-01
    outer loop
      vertex   -1.156788e+01 -1.090844e+01 -1.055920e+01
      vertex   -1.145846e+01 -1.090844e+01 -1.074991e+01
      vertex   -1.141032e+01 -1.096651e+01 -1.071919e+01
    endloop
  endfacet
  facet normal -5.635608e-01 -6.996208e-01 -4.392378e-01
    outer loop
      vertex   -1.141032e+01 -1.096651e+01 -1.071919e+01
      vertex   -1.145846e+01 -1.090844e+01 -1.074991e+01
      vertex   -1.114694e+01 -1.096651e+01 -1.105712e+01
    endloop
  endfacet
  facet normal -5.497241e-01 -7.170990e-01 -4.284536e-01
    outer loop
      vertex   -1.141032e+01 -1.096651e+01 -1.071919e+01
      vertex   -1.114694e+01 -1.096651e+01 -1.105712e+01
      vertex   -1.106514e+01 -1.107542e+01 -1.097979e+01
    endloop
  endfacet
  facet normal -4.582615e-01 -7.170780e-01 -5.251624e-01
    outer loop
      vertex   -1.106514e+01 -1.107542e+01 -1.097979e+01
      vertex   -1.114694e+01 -1.096651e+01 -1.105712e+01
      vertex   -1.075836e+01 -1.107542e+01 -1.124749e+01
    endloop
  endfacet
  facet normal -4.395281e-01 -7.437118e-01 -5.036941e-01
    outer loop
      vertex   -1.106514e+01 -1.107542e+01 -1.097979e+01
      vertex   -1.075836e+01 -1.107542e+01 -1.124749e+01
      vertex   -1.070833e+01 -1.115203e+01 -1.117802e+01
    endloop
  endfacet
  facet normal -3.372033e-01 -7.436472e-01 -5.773065e-01
    outer loop
      vertex   -1.070833e+01 -1.115203e+01 -1.117802e+01
      vertex   -1.075836e+01 -1.107542e+01 -1.124749e+01
      vertex   -1.037065e+01 -1.115203e+01 -1.137526e+01
    endloop
  endfacet
  facet normal -3.116010e-01 -7.863269e-01 -5.334743e-01
    outer loop
      vertex   -1.070833e+01 -1.115203e+01 -1.117802e+01
      vertex   -1.037065e+01 -1.115203e+01 -1.137526e+01
      vertex   -1.035010e+01 -1.119019e+01 -1.133101e+01
    endloop
  endfacet
  facet normal -2.336526e-01 -7.873355e-01 -5.705342e-01
    outer loop
      vertex   -1.035010e+01 -1.119019e+01 -1.133101e+01
      vertex   -1.037065e+01 -1.115203e+01 -1.137526e+01
      vertex   -1.017326e+01 -1.119019e+01 -1.140344e+01
    endloop
  endfacet
  facet normal -8.549511e-01 -4.760019e-01 -2.061090e-01
    outer loop
      vertex   -1.194565e+01 -1.071951e+01 -9.968720e+00
      vertex   -1.195193e+01 -1.070000e+01 -9.987751e+00
      vertex   -1.189043e+01 -1.071951e+01 -1.019778e+01
    endloop
  endfacet
  facet normal -9.510367e-01 1.103256e-01 -2.887170e-01
    outer loop
      vertex   -1.189043e+01 -1.071951e+01 -1.019778e+01
      vertex   -1.195193e+01 -1.070000e+01 -9.987751e+00
      vertex   -1.180957e+01 -1.070000e+01 -1.045669e+01
    endloop
  endfacet
  facet normal -8.767262e-01 -3.743336e-01 -3.020356e-01
    outer loop
      vertex   -1.189043e+01 -1.071951e+01 -1.019778e+01
      vertex   -1.180957e+01 -1.070000e+01 -1.045669e+01
      vertex   -1.181366e+01 -1.071951e+01 -1.042062e+01
    endloop
  endfacet
  facet normal -7.894107e-01 -4.979499e-01 -3.589941e-01
    outer loop
      vertex   -1.181366e+01 -1.071951e+01 -1.042062e+01
      vertex   -1.180957e+01 -1.070000e+01 -1.045669e+01
      vertex   -1.171611e+01 -1.071951e+01 -1.063512e+01
    endloop
  endfacet
  facet normal -7.174239e-01 -6.155154e-01 -3.262572e-01
    outer loop
      vertex   -1.181366e+01 -1.071951e+01 -1.042062e+01
      vertex   -1.171611e+01 -1.071951e+01 -1.063512e+01
      vertex   -1.168215e+01 -1.076831e+01 -1.061773e+01
    endloop
  endfacet
  facet normal -6.836185e-01 -6.154985e-01 -3.922083e-01
    outer loop
      vertex   -1.168215e+01 -1.076831e+01 -1.061773e+01
      vertex   -1.171611e+01 -1.071951e+01 -1.063512e+01
      vertex   -1.156669e+01 -1.076831e+01 -1.081899e+01
    endloop
  endfacet
  facet normal -6.544579e-01 -6.562781e-01 -3.754782e-01
    outer loop
      vertex   -1.168215e+01 -1.076831e+01 -1.061773e+01
      vertex   -1.156669e+01 -1.076831e+01 -1.081899e+01
      vertex   -1.153860e+01 -1.080658e+01 -1.080106e+01
    endloop
  endfacet
  facet normal -5.959619e-01 -6.550400e-01 -4.644912e-01
    outer loop
      vertex   -1.153860e+01 -1.080658e+01 -1.080106e+01
      vertex   -1.156669e+01 -1.076831e+01 -1.081899e+01
      vertex   -1.125754e+01 -1.080658e+01 -1.116169e+01
    endloop
  endfacet
  facet normal -5.833950e-01 -6.729794e-01 -4.546966e-01
    outer loop
      vertex   -1.153860e+01 -1.080658e+01 -1.080106e+01
      vertex   -1.125754e+01 -1.080658e+01 -1.116169e+01
      vertex   -1.122608e+01 -1.085394e+01 -1.113194e+01
    endloop
  endfacet
  facet normal -4.863285e-01 -6.729572e-01 -5.573268e-01
    outer loop
      vertex   -1.122608e+01 -1.085394e+01 -1.113194e+01
      vertex   -1.125754e+01 -1.080658e+01 -1.116169e+01
      vertex   -1.088775e+01 -1.085394e+01 -1.142717e+01
    endloop
  endfacet
  facet normal -4.776337e-01 -6.872119e-01 -5.473627e-01
    outer loop
      vertex   -1.122608e+01 -1.085394e+01 -1.113194e+01
      vertex   -1.088775e+01 -1.085394e+01 -1.142717e+01
      vertex   -1.085749e+01 -1.090844e+01 -1.138515e+01
    endloop
  endfacet
  facet normal -3.664319e-01 -6.871413e-01 -6.273472e-01
    outer loop
      vertex   -1.085749e+01 -1.090844e+01 -1.138515e+01
      vertex   -1.088775e+01 -1.085394e+01 -1.142717e+01
      vertex   -1.047812e+01 -1.090844e+01 -1.160674e+01
    endloop
  endfacet
  facet normal -3.604197e-01 -6.995298e-01 -6.170540e-01
    outer loop
      vertex   -1.085749e+01 -1.090844e+01 -1.138515e+01
      vertex   -1.047812e+01 -1.090844e+01 -1.160674e+01
      vertex   -1.045408e+01 -1.096651e+01 -1.155495e+01
    endloop
  endfacet
  facet normal -2.703763e-01 -7.007311e-01 -6.602065e-01
    outer loop
      vertex   -1.045408e+01 -1.096651e+01 -1.155495e+01
      vertex   -1.047812e+01 -1.090844e+01 -1.160674e+01
      vertex   -1.025560e+01 -1.096651e+01 -1.163624e+01
    endloop
  endfacet
  facet normal -2.637177e-01 -7.181816e-01 -6.439473e-01
    outer loop
      vertex   -1.045408e+01 -1.096651e+01 -1.155495e+01
      vertex   -1.025560e+01 -1.096651e+01 -1.163624e+01
      vertex   -1.021808e+01 -1.107542e+01 -1.153014e+01
    endloop
  endfacet
  facet normal -2.020057e-01 -7.182359e-01 -6.658310e-01
    outer loop
      vertex   -1.021808e+01 -1.107542e+01 -1.153014e+01
      vertex   -1.025560e+01 -1.096651e+01 -1.163624e+01
      vertex   -1.002310e+01 -1.107542e+01 -1.158929e+01
    endloop
  endfacet
  facet normal -1.937228e-01 -7.448164e-01 -6.385296e-01
    outer loop
      vertex   -1.021808e+01 -1.107542e+01 -1.153014e+01
      vertex   -1.002310e+01 -1.107542e+01 -1.158929e+01
      vertex   -1.000230e+01 -1.115203e+01 -1.150623e+01
    endloop
  endfacet
  facet normal -8.781467e-01 9.028051e-02 -4.697954e-01
    outer loop
      vertex   -1.180957e+01 -1.070000e+01 -1.045669e+01
      vertex   -1.157840e+01 -1.070000e+01 -1.088879e+01
      vertex   -1.171611e+01 -1.071951e+01 -1.063512e+01
    endloop
  endfacet
  facet normal -8.192907e-01 -3.283578e-01 -4.700467e-01
    outer loop
      vertex   -1.171611e+01 -1.071951e+01 -1.063512e+01
      vertex   -1.157840e+01 -1.070000e+01 -1.088879e+01
      vertex   -1.159885e+01 -1.071951e+01 -1.083951e+01
    endloop
  endfacet
  facet normal -6.836185e-01 -6.154985e-01 -3.922083e-01
    outer loop
      vertex   -1.171611e+01 -1.071951e+01 -1.063512e+01
      vertex   -1.159885e+01 -1.071951e+01 -1.083951e+01
      vertex   -1.156669e+01 -1.076831e+01 -1.081899e+01
    endloop
  endfacet
  facet normal -6.224092e-01 -6.142318e-01 -4.851041e-01
    outer loop
      vertex   -1.156669e+01 -1.076831e+01 -1.081899e+01
      vertex   -1.159885e+01 -1.071951e+01 -1.083951e+01
      vertex   -1.128175e+01 -1.076831e+01 -1.118458e+01
    endloop
  endfacet
  facet normal -5.959619e-01 -6.550400e-01 -4.644912e-01
    outer loop
      vertex   -1.156669e+01 -1.076831e+01 -1.081899e+01
      vertex   -1.128175e+01 -1.076831e+01 -1.118458e+01
      vertex   -1.125754e+01 -1.080658e+01 -1.116169e+01
    endloop
  endfacet
  facet normal -4.968038e-01 -6.550174e-01 -5.693314e-01
    outer loop
      vertex   -1.125754e+01 -1.080658e+01 -1.116169e+01
      vertex   -1.128175e+01 -1.076831e+01 -1.118458e+01
      vertex   -1.091304e+01 -1.080658e+01 -1.146229e+01
    endloop
  endfacet
  facet normal -4.863285e-01 -6.729572e-01 -5.573268e-01
    outer loop
      vertex   -1.125754e+01 -1.080658e+01 -1.116169e+01
      vertex   -1.091304e+01 -1.080658e+01 -1.146229e+01
      vertex   -1.088775e+01 -1.085394e+01 -1.142717e+01
    endloop
  endfacet
  facet normal -3.731010e-01 -6.728856e-01 -6.387649e-01
    outer loop
      vertex   -1.088775e+01 -1.085394e+01 -1.142717e+01
      vertex   -1.091304e+01 -1.080658e+01 -1.146229e+01
      vertex   -1.049992e+01 -1.085394e+01 -1.165370e+01
    endloop
  endfacet
  facet normal -3.664319e-01 -6.871413e-01 -6.273472e-01
    outer loop
      vertex   -1.088775e+01 -1.085394e+01 -1.142717e+01
      vertex   -1.049992e+01 -1.085394e+01 -1.165370e+01
      vertex   -1.047812e+01 -1.090844e+01 -1.160674e+01
    endloop
  endfacet
  facet normal -2.749024e-01 -6.883611e-01 -6.712582e-01
    outer loop
      vertex   -1.047812e+01 -1.090844e+01 -1.160674e+01
      vertex   -1.049992e+01 -1.085394e+01 -1.165370e+01
      vertex   -1.027464e+01 -1.090844e+01 -1.169007e+01
    endloop
  endfacet
  facet normal -2.703763e-01 -7.007311e-01 -6.602065e-01
    outer loop
      vertex   -1.047812e+01 -1.090844e+01 -1.160674e+01
      vertex   -1.027464e+01 -1.090844e+01 -1.169007e+01
      vertex   -1.025560e+01 -1.096651e+01 -1.163624e+01
    endloop
  endfacet
  facet normal -2.071070e-01 -7.007867e-01 -6.826453e-01
    outer loop
      vertex   -1.025560e+01 -1.096651e+01 -1.163624e+01
      vertex   -1.027464e+01 -1.090844e+01 -1.169007e+01
      vertex   -1.005044e+01 -1.096651e+01 -1.169848e+01
    endloop
  endfacet
  facet normal -2.020057e-01 -7.182359e-01 -6.658310e-01
    outer loop
      vertex   -1.025560e+01 -1.096651e+01 -1.163624e+01
      vertex   -1.005044e+01 -1.096651e+01 -1.169848e+01
      vertex   -1.002310e+01 -1.107542e+01 -1.158929e+01
    endloop
  endfacet
  facet normal -6.383397e-01 -5.873635e-01 -4.975203e-01
    outer loop
      vertex   -1.159885e+01 -1.071951e+01 -1.083951e+01
      vertex   -1.157840e+01 -1.070000e+01 -1.088879e+01
      vertex   -1.130948e+01 -1.071951e+01 -1.121079e+01
    endloop
  endfacet
  facet normal -7.587087e-01 -1.939507e-01 -6.218877e-01
    outer loop
      vertex   -1.130948e+01 -1.071951e+01 -1.121079e+01
      vertex   -1.157840e+01 -1.070000e+01 -1.088879e+01
      vertex   -1.126777e+01 -1.070000e+01 -1.126777e+01
    endloop
  endfacet
  facet normal -5.147863e-01 -6.220667e-01 -5.899391e-01
    outer loop
      vertex   -1.130948e+01 -1.071951e+01 -1.121079e+01
      vertex   -1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   -1.095480e+01 -1.071951e+01 -1.152029e+01
    endloop
  endfacet
  facet normal -6.271531e-01 -1.376630e-01 -7.666342e-01
    outer loop
      vertex   -1.095480e+01 -1.071951e+01 -1.152029e+01
      vertex   -1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   -1.088849e+01 -1.070000e+01 -1.157804e+01
    endloop
  endfacet
  facet normal -3.858935e-01 -6.438992e-01 -6.606663e-01
    outer loop
      vertex   -1.095480e+01 -1.071951e+01 -1.152029e+01
      vertex   -1.088849e+01 -1.070000e+01 -1.157804e+01
      vertex   -1.054824e+01 -1.071951e+01 -1.175776e+01
    endloop
  endfacet
  facet normal -4.691936e-01 -9.243396e-02 -8.782445e-01
    outer loop
      vertex   -1.054824e+01 -1.071951e+01 -1.175776e+01
      vertex   -1.088849e+01 -1.070000e+01 -1.157804e+01
      vertex   -1.045619e+01 -1.070000e+01 -1.180899e+01
    endloop
  endfacet
  facet normal -3.189461e-01 -5.401268e-01 -7.788045e-01
    outer loop
      vertex   -1.054824e+01 -1.071951e+01 -1.175776e+01
      vertex   -1.045619e+01 -1.070000e+01 -1.180899e+01
      vertex   -1.033017e+01 -1.071951e+01 -1.184706e+01
    endloop
  endfacet
  facet normal -2.917795e-01 -1.836045e-02 -9.563094e-01
    outer loop
      vertex   -1.033017e+01 -1.071951e+01 -1.184706e+01
      vertex   -1.045619e+01 -1.070000e+01 -1.180899e+01
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
    endloop
  endfacet
  facet normal -2.899976e-01 -4.723248e-02 -9.558611e-01
    outer loop
      vertex   -1.033017e+01 -1.071951e+01 -1.184706e+01
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
      vertex   -1.010476e+01 -1.071951e+01 -1.191545e+01
    endloop
  endfacet
  facet normal -6.361374e-02 -7.874322e-01 -6.131100e-01
    outer loop
      vertex   -9.613184e+00 -1.119019e+01 -1.151634e+01
      vertex   -9.810530e+00 -1.115203e+01 -1.154487e+01
      vertex   -9.615919e+00 -1.115203e+01 -1.156506e+01
    endloop
  endfacet
  facet normal -6.885705e-02 -7.448717e-01 -6.636451e-01
    outer loop
      vertex   -9.615919e+00 -1.115203e+01 -1.156506e+01
      vertex   -9.810530e+00 -1.115203e+01 -1.154487e+01
      vertex   -9.823386e+00 -1.107542e+01 -1.162953e+01
    endloop
  endfacet
  facet normal -6.885705e-02 -7.448717e-01 -6.636451e-01
    outer loop
      vertex   -9.615919e+00 -1.115203e+01 -1.156506e+01
      vertex   -9.823386e+00 -1.107542e+01 -1.162953e+01
      vertex   -9.620718e+00 -1.107542e+01 -1.165056e+01
    endloop
  endfacet
  facet normal -7.180161e-02 -7.182940e-01 -6.920248e-01
    outer loop
      vertex   -9.620718e+00 -1.107542e+01 -1.165056e+01
      vertex   -9.823386e+00 -1.107542e+01 -1.162953e+01
      vertex   -9.840287e+00 -1.096651e+01 -1.174082e+01
    endloop
  endfacet
  facet normal -7.180161e-02 -7.182940e-01 -6.920248e-01
    outer loop
      vertex   -9.620718e+00 -1.107542e+01 -1.165056e+01
      vertex   -9.840287e+00 -1.096651e+01 -1.174082e+01
      vertex   -9.627027e+00 -1.096651e+01 -1.176295e+01
    endloop
  endfacet
  facet normal -7.361514e-02 -7.008463e-01 -7.095035e-01
    outer loop
      vertex   -9.627027e+00 -1.096651e+01 -1.176295e+01
      vertex   -9.840287e+00 -1.096651e+01 -1.174082e+01
      vertex   -9.848862e+00 -1.090844e+01 -1.179729e+01
    endloop
  endfacet
  facet normal -7.361514e-02 -7.008463e-01 -7.095035e-01
    outer loop
      vertex   -9.627027e+00 -1.096651e+01 -1.176295e+01
      vertex   -9.848862e+00 -1.090844e+01 -1.179729e+01
      vertex   -9.630228e+00 -1.090844e+01 -1.181997e+01
    endloop
  endfacet
  facet normal -7.484786e-02 -6.884781e-01 -7.213845e-01
    outer loop
      vertex   -9.630228e+00 -1.090844e+01 -1.181997e+01
      vertex   -9.848862e+00 -1.090844e+01 -1.179729e+01
      vertex   -9.856638e+00 -1.085394e+01 -1.184849e+01
    endloop
  endfacet
  facet normal -7.484786e-02 -6.884781e-01 -7.213845e-01
    outer loop
      vertex   -9.630228e+00 -1.090844e+01 -1.181997e+01
      vertex   -9.856638e+00 -1.085394e+01 -1.184849e+01
      vertex   -9.633131e+00 -1.085394e+01 -1.187168e+01
    endloop
  endfacet
  facet normal -7.621555e-02 -6.742429e-01 -7.345663e-01
    outer loop
      vertex   -9.633131e+00 -1.085394e+01 -1.187168e+01
      vertex   -9.856638e+00 -1.085394e+01 -1.184849e+01
      vertex   -9.863138e+00 -1.080658e+01 -1.189130e+01
    endloop
  endfacet
  facet normal -8.133355e-02 -6.155449e-01 -7.838937e-01
    outer loop
      vertex   -9.873870e+00 -1.071951e+01 -1.196197e+01
      vertex   -9.637424e+00 -1.076831e+01 -1.194818e+01
      vertex   -9.868141e+00 -1.076831e+01 -1.192424e+01
    endloop
  endfacet
  facet normal -7.786368e-02 -6.563235e-01 -7.504510e-01
    outer loop
      vertex   -9.868141e+00 -1.076831e+01 -1.192424e+01
      vertex   -9.637424e+00 -1.076831e+01 -1.194818e+01
      vertex   -9.635557e+00 -1.080658e+01 -1.191491e+01
    endloop
  endfacet
  facet normal -1.789732e-01 -7.873822e-01 -5.899135e-01
    outer loop
      vertex   -1.000230e+01 -1.115203e+01 -1.150623e+01
      vertex   -9.990452e+00 -1.119019e+01 -1.145890e+01
      vertex   -1.018953e+01 -1.115203e+01 -1.144943e+01
    endloop
  endfacet
  facet normal -1.789732e-01 -7.873822e-01 -5.899135e-01
    outer loop
      vertex   -1.018953e+01 -1.115203e+01 -1.144943e+01
      vertex   -9.990452e+00 -1.119019e+01 -1.145890e+01
      vertex   -1.017326e+01 -1.119019e+01 -1.140344e+01
    endloop
  endfacet
  facet normal -2.336526e-01 -7.873355e-01 -5.705342e-01
    outer loop
      vertex   -1.018953e+01 -1.115203e+01 -1.144943e+01
      vertex   -1.017326e+01 -1.119019e+01 -1.140344e+01
      vertex   -1.037065e+01 -1.115203e+01 -1.137526e+01
    endloop
  endfacet
  facet normal -2.071070e-01 -7.007867e-01 -6.826453e-01
    outer loop
      vertex   -1.005044e+01 -1.096651e+01 -1.169848e+01
      vertex   -1.027464e+01 -1.090844e+01 -1.169007e+01
      vertex   -1.006431e+01 -1.090844e+01 -1.175388e+01
    endloop
  endfacet
  facet normal -2.105745e-01 -6.884176e-01 -6.940746e-01
    outer loop
      vertex   -1.006431e+01 -1.090844e+01 -1.175388e+01
      vertex   -1.027464e+01 -1.090844e+01 -1.169007e+01
      vertex   -1.029191e+01 -1.085394e+01 -1.173889e+01
    endloop
  endfacet
  facet normal -2.105745e-01 -6.884176e-01 -6.940746e-01
    outer loop
      vertex   -1.006431e+01 -1.090844e+01 -1.175388e+01
      vertex   -1.029191e+01 -1.085394e+01 -1.173889e+01
      vertex   -1.007689e+01 -1.085394e+01 -1.180412e+01
    endloop
  endfacet
  facet normal -2.144216e-01 -6.741815e-01 -7.067551e-01
    outer loop
      vertex   -1.007689e+01 -1.085394e+01 -1.180412e+01
      vertex   -1.029191e+01 -1.085394e+01 -1.173889e+01
      vertex   -1.030634e+01 -1.080658e+01 -1.177969e+01
    endloop
  endfacet
  facet normal -2.144216e-01 -6.741815e-01 -7.067551e-01
    outer loop
      vertex   -1.007689e+01 -1.085394e+01 -1.180412e+01
      vertex   -1.030634e+01 -1.080658e+01 -1.177969e+01
      vertex   -1.008740e+01 -1.080658e+01 -1.184612e+01
    endloop
  endfacet
  facet normal -2.190575e-01 -6.562611e-01 -7.220355e-01
    outer loop
      vertex   -1.008740e+01 -1.080658e+01 -1.184612e+01
      vertex   -1.030634e+01 -1.080658e+01 -1.177969e+01
      vertex   -1.031745e+01 -1.076831e+01 -1.181110e+01
    endloop
  endfacet
  facet normal -2.190575e-01 -6.562611e-01 -7.220355e-01
    outer loop
      vertex   -1.008740e+01 -1.080658e+01 -1.184612e+01
      vertex   -1.031745e+01 -1.076831e+01 -1.181110e+01
      vertex   -1.009549e+01 -1.076831e+01 -1.187844e+01
    endloop
  endfacet
  facet normal -2.288175e-01 -6.154811e-01 -7.542053e-01
    outer loop
      vertex   -1.009549e+01 -1.076831e+01 -1.187844e+01
      vertex   -1.031745e+01 -1.076831e+01 -1.181110e+01
      vertex   -1.033017e+01 -1.071951e+01 -1.184706e+01
    endloop
  endfacet
  facet normal -2.288175e-01 -6.154811e-01 -7.542053e-01
    outer loop
      vertex   -1.009549e+01 -1.076831e+01 -1.187844e+01
      vertex   -1.033017e+01 -1.071951e+01 -1.184706e+01
      vertex   -1.010476e+01 -1.071951e+01 -1.191545e+01
    endloop
  endfacet
  facet normal -2.529059e-01 -7.447646e-01 -6.175470e-01
    outer loop
      vertex   -1.037065e+01 -1.115203e+01 -1.137526e+01
      vertex   -1.040669e+01 -1.107542e+01 -1.145290e+01
      vertex   -1.018953e+01 -1.115203e+01 -1.144943e+01
    endloop
  endfacet
  facet normal -2.529059e-01 -7.447646e-01 -6.175470e-01
    outer loop
      vertex   -1.018953e+01 -1.115203e+01 -1.144943e+01
      vertex   -1.040669e+01 -1.107542e+01 -1.145290e+01
      vertex   -1.021808e+01 -1.107542e+01 -1.153014e+01
    endloop
  endfacet
  facet normal -1.937228e-01 -7.448164e-01 -6.385296e-01
    outer loop
      vertex   -1.018953e+01 -1.115203e+01 -1.144943e+01
      vertex   -1.021808e+01 -1.107542e+01 -1.153014e+01
      vertex   -1.000230e+01 -1.115203e+01 -1.150623e+01
    endloop
  endfacet
  facet normal -2.637177e-01 -7.181816e-01 -6.439473e-01
    outer loop
      vertex   -1.021808e+01 -1.107542e+01 -1.153014e+01
      vertex   -1.040669e+01 -1.107542e+01 -1.145290e+01
      vertex   -1.045408e+01 -1.096651e+01 -1.155495e+01
    endloop
  endfacet
  facet normal -3.515728e-01 -7.170102e-01 -6.019078e-01
    outer loop
      vertex   -1.045408e+01 -1.096651e+01 -1.155495e+01
      vertex   -1.040669e+01 -1.107542e+01 -1.145290e+01
      vertex   -1.082412e+01 -1.096651e+01 -1.133881e+01
    endloop
  endfacet
  facet normal -3.604197e-01 -6.995298e-01 -6.170540e-01
    outer loop
      vertex   -1.045408e+01 -1.096651e+01 -1.155495e+01
      vertex   -1.082412e+01 -1.096651e+01 -1.133881e+01
      vertex   -1.085749e+01 -1.090844e+01 -1.138515e+01
    endloop
  endfacet
  facet normal -4.697954e-01 -6.995993e-01 -5.383801e-01
    outer loop
      vertex   -1.085749e+01 -1.090844e+01 -1.138515e+01
      vertex   -1.082412e+01 -1.096651e+01 -1.133881e+01
      vertex   -1.118844e+01 -1.090844e+01 -1.109636e+01
    endloop
  endfacet
  facet normal -4.776337e-01 -6.872119e-01 -5.473627e-01
    outer loop
      vertex   -1.085749e+01 -1.090844e+01 -1.138515e+01
      vertex   -1.118844e+01 -1.090844e+01 -1.109636e+01
      vertex   -1.122608e+01 -1.085394e+01 -1.113194e+01
    endloop
  endfacet
  facet normal -5.729641e-01 -6.872337e-01 -4.465668e-01
    outer loop
      vertex   -1.122608e+01 -1.085394e+01 -1.113194e+01
      vertex   -1.118844e+01 -1.090844e+01 -1.109636e+01
      vertex   -1.150211e+01 -1.085394e+01 -1.077778e+01
    endloop
  endfacet
  facet normal -5.833950e-01 -6.729794e-01 -4.546966e-01
    outer loop
      vertex   -1.122608e+01 -1.085394e+01 -1.113194e+01
      vertex   -1.150211e+01 -1.085394e+01 -1.077778e+01
      vertex   -1.153860e+01 -1.080658e+01 -1.080106e+01
    endloop
  endfacet
  facet normal -6.406070e-01 -6.741982e-01 -3.675316e-01
    outer loop
      vertex   -1.153860e+01 -1.080658e+01 -1.080106e+01
      vertex   -1.150211e+01 -1.085394e+01 -1.077778e+01
      vertex   -1.165250e+01 -1.080658e+01 -1.060254e+01
    endloop
  endfacet
  facet normal -6.544579e-01 -6.562781e-01 -3.754782e-01
    outer loop
      vertex   -1.153860e+01 -1.080658e+01 -1.080106e+01
      vertex   -1.165250e+01 -1.080658e+01 -1.060254e+01
      vertex   -1.168215e+01 -1.076831e+01 -1.061773e+01
    endloop
  endfacet
  facet normal -6.868197e-01 -6.562946e-01 -3.123396e-01
    outer loop
      vertex   -1.168215e+01 -1.076831e+01 -1.061773e+01
      vertex   -1.165250e+01 -1.080658e+01 -1.060254e+01
      vertex   -1.177821e+01 -1.076831e+01 -1.040651e+01
    endloop
  endfacet
  facet normal -7.174239e-01 -6.155154e-01 -3.262572e-01
    outer loop
      vertex   -1.168215e+01 -1.076831e+01 -1.061773e+01
      vertex   -1.177821e+01 -1.076831e+01 -1.040651e+01
      vertex   -1.181366e+01 -1.071951e+01 -1.042062e+01
    endloop
  endfacet
  facet normal -7.451304e-01 -6.155369e-01 -2.567003e-01
    outer loop
      vertex   -1.181366e+01 -1.071951e+01 -1.042062e+01
      vertex   -1.177821e+01 -1.076831e+01 -1.040651e+01
      vertex   -1.189043e+01 -1.071951e+01 -1.019778e+01
    endloop
  endfacet
  facet normal -3.515728e-01 -7.170102e-01 -6.019078e-01
    outer loop
      vertex   -1.082412e+01 -1.096651e+01 -1.133881e+01
      vertex   -1.040669e+01 -1.107542e+01 -1.145290e+01
      vertex   -1.075836e+01 -1.107542e+01 -1.124749e+01
    endloop
  endfacet
  facet normal -3.372033e-01 -7.436472e-01 -5.773065e-01
    outer loop
      vertex   -1.075836e+01 -1.107542e+01 -1.124749e+01
      vertex   -1.040669e+01 -1.107542e+01 -1.145290e+01
      vertex   -1.037065e+01 -1.115203e+01 -1.137526e+01
    endloop
  endfacet
  facet normal -2.749024e-01 -6.883611e-01 -6.712582e-01
    outer loop
      vertex   -1.029191e+01 -1.085394e+01 -1.173889e+01
      vertex   -1.027464e+01 -1.090844e+01 -1.169007e+01
      vertex   -1.049992e+01 -1.085394e+01 -1.165370e+01
    endloop
  endfacet
  facet normal -2.799239e-01 -6.741241e-01 -6.835198e-01
    outer loop
      vertex   -1.030634e+01 -1.080658e+01 -1.177969e+01
      vertex   -1.029191e+01 -1.085394e+01 -1.173889e+01
      vertex   -1.051815e+01 -1.080658e+01 -1.169295e+01
    endloop
  endfacet
  facet normal -2.799239e-01 -6.741241e-01 -6.835198e-01
    outer loop
      vertex   -1.051815e+01 -1.080658e+01 -1.169295e+01
      vertex   -1.029191e+01 -1.085394e+01 -1.173889e+01
      vertex   -1.049992e+01 -1.085394e+01 -1.165370e+01
    endloop
  endfacet
  facet normal -3.731010e-01 -6.728856e-01 -6.387649e-01
    outer loop
      vertex   -1.051815e+01 -1.080658e+01 -1.169295e+01
      vertex   -1.049992e+01 -1.085394e+01 -1.165370e+01
      vertex   -1.091304e+01 -1.080658e+01 -1.146229e+01
    endloop
  endfacet
  facet normal -2.859749e-01 -6.562028e-01 -6.982952e-01
    outer loop
      vertex   -1.031745e+01 -1.076831e+01 -1.181110e+01
      vertex   -1.030634e+01 -1.080658e+01 -1.177969e+01
      vertex   -1.053217e+01 -1.076831e+01 -1.172316e+01
    endloop
  endfacet
  facet normal -2.859749e-01 -6.562028e-01 -6.982952e-01
    outer loop
      vertex   -1.053217e+01 -1.076831e+01 -1.172316e+01
      vertex   -1.030634e+01 -1.080658e+01 -1.177969e+01
      vertex   -1.051815e+01 -1.080658e+01 -1.169295e+01
    endloop
  endfacet
  facet normal -3.811356e-01 -6.549447e-01 -6.525206e-01
    outer loop
      vertex   -1.053217e+01 -1.076831e+01 -1.172316e+01
      vertex   -1.051815e+01 -1.080658e+01 -1.169295e+01
      vertex   -1.093251e+01 -1.076831e+01 -1.148933e+01
    endloop
  endfacet
  facet normal -3.811356e-01 -6.549447e-01 -6.525206e-01
    outer loop
      vertex   -1.093251e+01 -1.076831e+01 -1.148933e+01
      vertex   -1.051815e+01 -1.080658e+01 -1.169295e+01
      vertex   -1.091304e+01 -1.080658e+01 -1.146229e+01
    endloop
  endfacet
  facet normal -4.968038e-01 -6.550174e-01 -5.693314e-01
    outer loop
      vertex   -1.093251e+01 -1.076831e+01 -1.148933e+01
      vertex   -1.091304e+01 -1.080658e+01 -1.146229e+01
      vertex   -1.128175e+01 -1.076831e+01 -1.118458e+01
    endloop
  endfacet
  facet normal -2.987139e-01 -6.154214e-01 -7.294014e-01
    outer loop
      vertex   -1.033017e+01 -1.071951e+01 -1.184706e+01
      vertex   -1.031745e+01 -1.076831e+01 -1.181110e+01
      vertex   -1.054824e+01 -1.071951e+01 -1.175776e+01
    endloop
  endfacet
  facet normal -2.987139e-01 -6.154214e-01 -7.294014e-01
    outer loop
      vertex   -1.054824e+01 -1.071951e+01 -1.175776e+01
      vertex   -1.031745e+01 -1.076831e+01 -1.181110e+01
      vertex   -1.053217e+01 -1.076831e+01 -1.172316e+01
    endloop
  endfacet
  facet normal -3.980442e-01 -6.141344e-01 -6.814688e-01
    outer loop
      vertex   -1.054824e+01 -1.071951e+01 -1.175776e+01
      vertex   -1.053217e+01 -1.076831e+01 -1.172316e+01
      vertex   -1.095480e+01 -1.071951e+01 -1.152029e+01
    endloop
  endfacet
  facet normal -3.980442e-01 -6.141344e-01 -6.814688e-01
    outer loop
      vertex   -1.095480e+01 -1.071951e+01 -1.152029e+01
      vertex   -1.053217e+01 -1.076831e+01 -1.172316e+01
      vertex   -1.093251e+01 -1.076831e+01 -1.148933e+01
    endloop
  endfacet
  facet normal -5.188491e-01 -6.142088e-01 -5.945950e-01
    outer loop
      vertex   -1.095480e+01 -1.071951e+01 -1.152029e+01
      vertex   -1.093251e+01 -1.076831e+01 -1.148933e+01
      vertex   -1.130948e+01 -1.071951e+01 -1.121079e+01
    endloop
  endfacet
  facet normal -5.188491e-01 -6.142088e-01 -5.945950e-01
    outer loop
      vertex   -1.130948e+01 -1.071951e+01 -1.121079e+01
      vertex   -1.093251e+01 -1.076831e+01 -1.148933e+01
      vertex   -1.128175e+01 -1.076831e+01 -1.118458e+01
    endloop
  endfacet
  facet normal -6.224092e-01 -6.142318e-01 -4.851041e-01
    outer loop
      vertex   -1.130948e+01 -1.071951e+01 -1.121079e+01
      vertex   -1.128175e+01 -1.076831e+01 -1.118458e+01
      vertex   -1.159885e+01 -1.071951e+01 -1.083951e+01
    endloop
  endfacet
  facet normal -3.116010e-01 -7.863269e-01 -5.334743e-01
    outer loop
      vertex   -1.035010e+01 -1.119019e+01 -1.133101e+01
      vertex   -1.067982e+01 -1.119019e+01 -1.113842e+01
      vertex   -1.070833e+01 -1.115203e+01 -1.117802e+01
    endloop
  endfacet
  facet normal -4.061516e-01 -7.863852e-01 -4.654451e-01
    outer loop
      vertex   -1.070833e+01 -1.115203e+01 -1.117802e+01
      vertex   -1.067982e+01 -1.119019e+01 -1.113842e+01
      vertex   -1.100292e+01 -1.115203e+01 -1.092096e+01
    endloop
  endfacet
  facet normal -4.395281e-01 -7.437118e-01 -5.036941e-01
    outer loop
      vertex   -1.070833e+01 -1.115203e+01 -1.117802e+01
      vertex   -1.100292e+01 -1.115203e+01 -1.092096e+01
      vertex   -1.106514e+01 -1.107542e+01 -1.097979e+01
    endloop
  endfacet
  facet normal -5.272505e-01 -7.437318e-01 -4.109377e-01
    outer loop
      vertex   -1.106514e+01 -1.107542e+01 -1.097979e+01
      vertex   -1.100292e+01 -1.115203e+01 -1.092096e+01
      vertex   -1.131544e+01 -1.107542e+01 -1.065864e+01
    endloop
  endfacet
  facet normal -5.497241e-01 -7.170990e-01 -4.284536e-01
    outer loop
      vertex   -1.106514e+01 -1.107542e+01 -1.097979e+01
      vertex   -1.131544e+01 -1.107542e+01 -1.065864e+01
      vertex   -1.141032e+01 -1.096651e+01 -1.071919e+01
    endloop
  endfacet
  facet normal -6.035115e-01 -7.182517e-01 -3.462490e-01
    outer loop
      vertex   -1.141032e+01 -1.096651e+01 -1.071919e+01
      vertex   -1.131544e+01 -1.107542e+01 -1.065864e+01
      vertex   -1.151705e+01 -1.096651e+01 -1.053316e+01
    endloop
  endfacet
  facet normal -6.187527e-01 -7.008030e-01 -3.549933e-01
    outer loop
      vertex   -1.141032e+01 -1.096651e+01 -1.071919e+01
      vertex   -1.151705e+01 -1.096651e+01 -1.053316e+01
      vertex   -1.156788e+01 -1.090844e+01 -1.055920e+01
    endloop
  endfacet
  facet normal -6.493472e-01 -7.008187e-01 -2.952986e-01
    outer loop
      vertex   -1.156788e+01 -1.090844e+01 -1.055920e+01
      vertex   -1.151705e+01 -1.096651e+01 -1.053316e+01
      vertex   -1.165890e+01 -1.090844e+01 -1.035904e+01
    endloop
  endfacet
  facet normal -6.602200e-01 -6.884501e-01 -3.002431e-01
    outer loop
      vertex   -1.156788e+01 -1.090844e+01 -1.055920e+01
      vertex   -1.165890e+01 -1.090844e+01 -1.035904e+01
      vertex   -1.170703e+01 -1.085394e+01 -1.037818e+01
    endloop
  endfacet
  facet normal -6.857137e-01 -6.884705e-01 -2.362310e-01
    outer loop
      vertex   -1.170703e+01 -1.085394e+01 -1.037818e+01
      vertex   -1.165890e+01 -1.090844e+01 -1.035904e+01
      vertex   -1.178026e+01 -1.085394e+01 -1.016562e+01
    endloop
  endfacet
  facet normal -6.982434e-01 -6.742351e-01 -2.405476e-01
    outer loop
      vertex   -1.170703e+01 -1.085394e+01 -1.037818e+01
      vertex   -1.178026e+01 -1.085394e+01 -1.016562e+01
      vertex   -1.182181e+01 -1.080658e+01 -1.017775e+01
    endloop
  endfacet
  facet normal -7.179437e-01 -6.742405e-01 -1.730797e-01
    outer loop
      vertex   -1.182181e+01 -1.080658e+01 -1.017775e+01
      vertex   -1.178026e+01 -1.085394e+01 -1.016562e+01
      vertex   -1.187545e+01 -1.080658e+01 -9.955265e+00
    endloop
  endfacet
  facet normal -7.334689e-01 -6.563210e-01 -1.768224e-01
    outer loop
      vertex   -1.182181e+01 -1.080658e+01 -1.017775e+01
      vertex   -1.187545e+01 -1.080658e+01 -9.955265e+00
      vertex   -1.190818e+01 -1.076831e+01 -9.961537e+00
    endloop
  endfacet
  facet normal -7.468839e-01 -6.563192e-01 -1.068153e-01
    outer loop
      vertex   -1.190818e+01 -1.076831e+01 -9.961537e+00
      vertex   -1.187545e+01 -1.080658e+01 -9.955265e+00
      vertex   -1.194102e+01 -1.076831e+01 -9.731880e+00
    endloop
  endfacet
  facet normal -7.801671e-01 -6.155406e-01 -1.115753e-01
    outer loop
      vertex   -1.190818e+01 -1.076831e+01 -9.961537e+00
      vertex   -1.194102e+01 -1.076831e+01 -9.731880e+00
      vertex   -1.197901e+01 -1.071951e+01 -9.735488e+00
    endloop
  endfacet
  facet normal -4.697954e-01 -6.995993e-01 -5.383801e-01
    outer loop
      vertex   -1.118844e+01 -1.090844e+01 -1.109636e+01
      vertex   -1.082412e+01 -1.096651e+01 -1.133881e+01
      vertex   -1.114694e+01 -1.096651e+01 -1.105712e+01
    endloop
  endfacet
  facet normal -4.582615e-01 -7.170780e-01 -5.251624e-01
    outer loop
      vertex   -1.114694e+01 -1.096651e+01 -1.105712e+01
      vertex   -1.082412e+01 -1.096651e+01 -1.133881e+01
      vertex   -1.075836e+01 -1.107542e+01 -1.124749e+01
    endloop
  endfacet
  facet normal -4.061516e-01 -7.863852e-01 -4.654451e-01
    outer loop
      vertex   -1.067982e+01 -1.119019e+01 -1.113842e+01
      vertex   -1.096746e+01 -1.119019e+01 -1.088743e+01
      vertex   -1.100292e+01 -1.115203e+01 -1.092096e+01
    endloop
  endfacet
  facet normal -4.872108e-01 -7.864033e-01 -3.797308e-01
    outer loop
      vertex   -1.100292e+01 -1.115203e+01 -1.092096e+01
      vertex   -1.096746e+01 -1.119019e+01 -1.088743e+01
      vertex   -1.124327e+01 -1.115203e+01 -1.061258e+01
    endloop
  endfacet
  facet normal -5.272505e-01 -7.437318e-01 -4.109377e-01
    outer loop
      vertex   -1.100292e+01 -1.115203e+01 -1.092096e+01
      vertex   -1.124327e+01 -1.115203e+01 -1.061258e+01
      vertex   -1.131544e+01 -1.107542e+01 -1.065864e+01
    endloop
  endfacet
  facet normal -5.787644e-01 -7.448315e-01 -3.320510e-01
    outer loop
      vertex   -1.131544e+01 -1.107542e+01 -1.065864e+01
      vertex   -1.124327e+01 -1.115203e+01 -1.061258e+01
      vertex   -1.141687e+01 -1.107542e+01 -1.048185e+01
    endloop
  endfacet
  facet normal -6.035115e-01 -7.182517e-01 -3.462490e-01
    outer loop
      vertex   -1.131544e+01 -1.107542e+01 -1.065864e+01
      vertex   -1.141687e+01 -1.107542e+01 -1.048185e+01
      vertex   -1.151705e+01 -1.096651e+01 -1.053316e+01
    endloop
  endfacet
  facet normal -6.333517e-01 -7.182671e-01 -2.880244e-01
    outer loop
      vertex   -1.151705e+01 -1.096651e+01 -1.053316e+01
      vertex   -1.141687e+01 -1.107542e+01 -1.048185e+01
      vertex   -1.160584e+01 -1.096651e+01 -1.033792e+01
    endloop
  endfacet
  facet normal -6.493472e-01 -7.008187e-01 -2.952986e-01
    outer loop
      vertex   -1.151705e+01 -1.096651e+01 -1.053316e+01
      vertex   -1.160584e+01 -1.096651e+01 -1.033792e+01
      vertex   -1.165890e+01 -1.090844e+01 -1.035904e+01
    endloop
  endfacet
  facet normal -6.744204e-01 -7.008388e-01 -2.323405e-01
    outer loop
      vertex   -1.165890e+01 -1.090844e+01 -1.035904e+01
      vertex   -1.160584e+01 -1.096651e+01 -1.033792e+01
      vertex   -1.173054e+01 -1.090844e+01 -1.015111e+01
    endloop
  endfacet
  facet normal -6.857137e-01 -6.884705e-01 -2.362310e-01
    outer loop
      vertex   -1.165890e+01 -1.090844e+01 -1.035904e+01
      vertex   -1.173054e+01 -1.090844e+01 -1.015111e+01
      vertex   -1.178026e+01 -1.085394e+01 -1.016562e+01
    endloop
  endfacet
  facet normal -7.050603e-01 -6.884757e-01 -1.699738e-01
    outer loop
      vertex   -1.178026e+01 -1.085394e+01 -1.016562e+01
      vertex   -1.173054e+01 -1.090844e+01 -1.015111e+01
      vertex   -1.183293e+01 -1.085394e+01 -9.947116e+00
    endloop
  endfacet
  facet normal -7.179437e-01 -6.742405e-01 -1.730797e-01
    outer loop
      vertex   -1.178026e+01 -1.085394e+01 -1.016562e+01
      vertex   -1.183293e+01 -1.085394e+01 -9.947116e+00
      vertex   -1.187545e+01 -1.080658e+01 -9.955265e+00
    endloop
  endfacet
  facet normal -7.310749e-01 -6.742387e-01 -1.045544e-01
    outer loop
      vertex   -1.187545e+01 -1.080658e+01 -9.955265e+00
      vertex   -1.183293e+01 -1.085394e+01 -9.947116e+00
      vertex   -1.190785e+01 -1.080658e+01 -9.728729e+00
    endloop
  endfacet
  facet normal -7.468839e-01 -6.563192e-01 -1.068153e-01
    outer loop
      vertex   -1.187545e+01 -1.080658e+01 -9.955265e+00
      vertex   -1.190785e+01 -1.080658e+01 -9.728729e+00
      vertex   -1.194102e+01 -1.076831e+01 -9.731880e+00
    endloop
  endfacet
  facet normal -5.729641e-01 -6.872337e-01 -4.465668e-01
    outer loop
      vertex   -1.150211e+01 -1.085394e+01 -1.077778e+01
      vertex   -1.118844e+01 -1.090844e+01 -1.109636e+01
      vertex   -1.145846e+01 -1.090844e+01 -1.074991e+01
    endloop
  endfacet
  facet normal -5.635608e-01 -6.996208e-01 -4.392378e-01
    outer loop
      vertex   -1.145846e+01 -1.090844e+01 -1.074991e+01
      vertex   -1.118844e+01 -1.090844e+01 -1.109636e+01
      vertex   -1.114694e+01 -1.096651e+01 -1.105712e+01
    endloop
  endfacet
  facet normal -4.872108e-01 -7.864033e-01 -3.797308e-01
    outer loop
      vertex   -1.096746e+01 -1.119019e+01 -1.088743e+01
      vertex   -1.120214e+01 -1.119019e+01 -1.058633e+01
      vertex   -1.124327e+01 -1.115203e+01 -1.061258e+01
    endloop
  endfacet
  facet normal -5.346970e-01 -7.873958e-01 -3.067685e-01
    outer loop
      vertex   -1.124327e+01 -1.115203e+01 -1.061258e+01
      vertex   -1.120214e+01 -1.119019e+01 -1.058633e+01
      vertex   -1.134067e+01 -1.115203e+01 -1.044282e+01
    endloop
  endfacet
  facet normal -5.787644e-01 -7.448315e-01 -3.320510e-01
    outer loop
      vertex   -1.124327e+01 -1.115203e+01 -1.061258e+01
      vertex   -1.134067e+01 -1.115203e+01 -1.044282e+01
      vertex   -1.141687e+01 -1.107542e+01 -1.048185e+01
    endloop
  endfacet
  facet normal -6.073799e-01 -7.448461e-01 -2.762134e-01
    outer loop
      vertex   -1.141687e+01 -1.107542e+01 -1.048185e+01
      vertex   -1.134067e+01 -1.115203e+01 -1.044282e+01
      vertex   -1.150125e+01 -1.107542e+01 -1.029631e+01
    endloop
  endfacet
  facet normal -6.333517e-01 -7.182671e-01 -2.880244e-01
    outer loop
      vertex   -1.141687e+01 -1.107542e+01 -1.048185e+01
      vertex   -1.150125e+01 -1.107542e+01 -1.029631e+01
      vertex   -1.160584e+01 -1.096651e+01 -1.033792e+01
    endloop
  endfacet
  facet normal -6.578063e-01 -7.182866e-01 -2.266168e-01
    outer loop
      vertex   -1.160584e+01 -1.096651e+01 -1.033792e+01
      vertex   -1.150125e+01 -1.107542e+01 -1.029631e+01
      vertex   -1.167571e+01 -1.096651e+01 -1.013510e+01
    endloop
  endfacet
  facet normal -6.744204e-01 -7.008388e-01 -2.323405e-01
    outer loop
      vertex   -1.160584e+01 -1.096651e+01 -1.033792e+01
      vertex   -1.167571e+01 -1.096651e+01 -1.013510e+01
      vertex   -1.173054e+01 -1.090844e+01 -1.015111e+01
    endloop
  endfacet
  facet normal -6.934483e-01 -7.008439e-01 -1.671744e-01
    outer loop
      vertex   -1.173054e+01 -1.090844e+01 -1.015111e+01
      vertex   -1.167571e+01 -1.096651e+01 -1.013510e+01
      vertex   -1.178206e+01 -1.090844e+01 -9.937367e+00
    endloop
  endfacet
  facet normal -7.050603e-01 -6.884757e-01 -1.699738e-01
    outer loop
      vertex   -1.173054e+01 -1.090844e+01 -1.015111e+01
      vertex   -1.178206e+01 -1.090844e+01 -9.937367e+00
      vertex   -1.183293e+01 -1.085394e+01 -9.947116e+00
    endloop
  endfacet
  facet normal -7.179560e-01 -6.884740e-01 -1.026782e-01
    outer loop
      vertex   -1.183293e+01 -1.085394e+01 -9.947116e+00
      vertex   -1.178206e+01 -1.090844e+01 -9.937367e+00
      vertex   -1.186475e+01 -1.085394e+01 -9.724635e+00
    endloop
  endfacet
  facet normal -7.310749e-01 -6.742387e-01 -1.045544e-01
    outer loop
      vertex   -1.183293e+01 -1.085394e+01 -9.947116e+00
      vertex   -1.186475e+01 -1.085394e+01 -9.724635e+00
      vertex   -1.190785e+01 -1.080658e+01 -9.728729e+00
    endloop
  endfacet
  facet normal -6.406070e-01 -6.741982e-01 -3.675316e-01
    outer loop
      vertex   -1.165250e+01 -1.080658e+01 -1.060254e+01
      vertex   -1.150211e+01 -1.085394e+01 -1.077778e+01
      vertex   -1.161397e+01 -1.085394e+01 -1.058281e+01
    endloop
  endfacet
  facet normal -6.291128e-01 -6.884341e-01 -3.609371e-01
    outer loop
      vertex   -1.161397e+01 -1.085394e+01 -1.058281e+01
      vertex   -1.150211e+01 -1.085394e+01 -1.077778e+01
      vertex   -1.145846e+01 -1.090844e+01 -1.074991e+01
    endloop
  endfacet
  facet normal -6.722831e-01 -6.742145e-01 -3.057289e-01
    outer loop
      vertex   -1.165250e+01 -1.080658e+01 -1.060254e+01
      vertex   -1.161397e+01 -1.085394e+01 -1.058281e+01
      vertex   -1.174725e+01 -1.080658e+01 -1.039419e+01
    endloop
  endfacet
  facet normal -6.868197e-01 -6.562946e-01 -3.123396e-01
    outer loop
      vertex   -1.165250e+01 -1.080658e+01 -1.060254e+01
      vertex   -1.174725e+01 -1.080658e+01 -1.039419e+01
      vertex   -1.177821e+01 -1.076831e+01 -1.040651e+01
    endloop
  endfacet
  facet normal -7.133423e-01 -6.563156e-01 -2.457492e-01
    outer loop
      vertex   -1.177821e+01 -1.076831e+01 -1.040651e+01
      vertex   -1.174725e+01 -1.080658e+01 -1.039419e+01
      vertex   -1.185380e+01 -1.076831e+01 -1.018709e+01
    endloop
  endfacet
  facet normal -7.451304e-01 -6.155369e-01 -2.567003e-01
    outer loop
      vertex   -1.177821e+01 -1.076831e+01 -1.040651e+01
      vertex   -1.185380e+01 -1.076831e+01 -1.018709e+01
      vertex   -1.189043e+01 -1.071951e+01 -1.019778e+01
    endloop
  endfacet
  facet normal -7.661545e-01 -6.155424e-01 -1.847022e-01
    outer loop
      vertex   -1.189043e+01 -1.071951e+01 -1.019778e+01
      vertex   -1.185380e+01 -1.076831e+01 -1.018709e+01
      vertex   -1.194565e+01 -1.071951e+01 -9.968720e+00
    endloop
  endfacet
  facet normal -5.992365e-01 -7.874302e-01 -1.444621e-01
    outer loop
      vertex   -1.148339e+01 -1.119019e+01 -9.880125e+00
      vertex   -1.153132e+01 -1.115203e+01 -9.889311e+00
      vertex   -1.143861e+01 -1.119019e+01 -1.006589e+01
    endloop
  endfacet
  facet normal -5.992365e-01 -7.874302e-01 -1.444621e-01
    outer loop
      vertex   -1.143861e+01 -1.119019e+01 -1.006589e+01
      vertex   -1.153132e+01 -1.115203e+01 -9.889311e+00
      vertex   -1.148545e+01 -1.115203e+01 -1.007957e+01
    endloop
  endfacet
  facet normal -5.827949e-01 -7.874258e-01 -2.007751e-01
    outer loop
      vertex   -1.143861e+01 -1.119019e+01 -1.006589e+01
      vertex   -1.148545e+01 -1.115203e+01 -1.007957e+01
      vertex   -1.137635e+01 -1.119019e+01 -1.024661e+01
    endloop
  endfacet
  facet normal -6.486278e-01 -7.448695e-01 -1.563692e-01
    outer loop
      vertex   -1.148545e+01 -1.115203e+01 -1.007957e+01
      vertex   -1.153132e+01 -1.115203e+01 -9.889311e+00
      vertex   -1.161542e+01 -1.107542e+01 -9.905429e+00
    endloop
  endfacet
  facet normal -6.604915e-01 -7.448679e-01 -9.445995e-02
    outer loop
      vertex   -1.161542e+01 -1.107542e+01 -9.905429e+00
      vertex   -1.153132e+01 -1.115203e+01 -9.889311e+00
      vertex   -1.164427e+01 -1.107542e+01 -9.703690e+00
    endloop
  endfacet
  facet normal -6.887361e-01 -7.182900e-01 -9.849934e-02
    outer loop
      vertex   -1.161542e+01 -1.107542e+01 -9.905429e+00
      vertex   -1.164427e+01 -1.107542e+01 -9.703690e+00
      vertex   -1.175633e+01 -1.096651e+01 -9.714335e+00
    endloop
  endfacet
  facet normal -6.604915e-01 -7.448679e-01 -9.445995e-02
    outer loop
      vertex   -1.164427e+01 -1.107542e+01 -9.703690e+00
      vertex   -1.153132e+01 -1.115203e+01 -9.889311e+00
      vertex   -1.155902e+01 -1.115203e+01 -9.695593e+00
    endloop
  endfacet
  facet normal -6.101970e-01 -7.874287e-01 -8.726711e-02
    outer loop
      vertex   -1.155902e+01 -1.115203e+01 -9.695593e+00
      vertex   -1.153132e+01 -1.115203e+01 -9.889311e+00
      vertex   -1.148339e+01 -1.119019e+01 -9.880125e+00
    endloop
  endfacet
  facet normal 8.903473e-17 -3.051016e-01 -9.523198e-01
    outer loop
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
    endloop
  endfacet
  facet normal -8.657003e-05 -5.150409e-01 -8.571656e-01
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
    endloop
  endfacet
  facet normal -1.691309e-04 -5.756102e-01 -8.177242e-01
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 5.134026e-16 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -8.310975e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 2.344465e-16 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
      vertex   -8.310975e+00 -1.076831e+01 -1.195203e+01
      vertex   -8.310975e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -1.758838e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -8.310975e+00 -1.085394e+01 -1.187542e+01
      vertex   -8.310975e+00 -1.076831e+01 -1.195203e+01
      vertex   -7.716772e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -2.008905e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -8.310975e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.716772e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.716772e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.289475e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -7.716772e+00 -1.096651e+01 -1.176651e+01
      vertex   -7.716772e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.122746e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.247588e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -7.716772e+00 -1.096651e+01 -1.176651e+01
      vertex   -7.122746e+00 -1.096651e+01 -1.176651e+01
      vertex   -7.122746e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.032943e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -7.122746e+00 -1.107542e+01 -1.165394e+01
      vertex   -7.122746e+00 -1.096651e+01 -1.176651e+01
      vertex   -6.528873e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 9.737700e-15 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -7.122746e+00 -1.107542e+01 -1.165394e+01
      vertex   -6.528873e+00 -1.107542e+01 -1.165394e+01
      vertex   -6.528873e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 1.349497e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -6.528873e+00 -1.115203e+01 -1.156831e+01
      vertex   -6.528873e+00 -1.107542e+01 -1.165394e+01
      vertex   -5.935131e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 1.187214e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -6.528873e+00 -1.115203e+01 -1.156831e+01
      vertex   -5.935131e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal 2.304179e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -5.935131e+00 -1.115203e+01 -1.156831e+01
      vertex   -4.747953e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 2.514942e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   -3.561030e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 2.706144e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -3.561030e+00 -1.115203e+01 -1.156831e+01
      vertex   -4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   -4.747953e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 2.007838e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -3.561030e+00 -1.115203e+01 -1.156831e+01
      vertex   -4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   -3.561030e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 2.084788e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -3.561030e+00 -1.107542e+01 -1.165394e+01
      vertex   -4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   -4.747953e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.669351e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -3.561030e+00 -1.107542e+01 -1.165394e+01
      vertex   -4.747953e+00 -1.096651e+01 -1.176651e+01
      vertex   -3.561030e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.717444e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -3.561030e+00 -1.096651e+01 -1.176651e+01
      vertex   -4.747953e+00 -1.096651e+01 -1.176651e+01
      vertex   -4.747953e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 1.599367e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -3.561030e+00 -1.096651e+01 -1.176651e+01
      vertex   -4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   -3.561030e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 1.626040e-14 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -3.561030e+00 -1.085394e+01 -1.187542e+01
      vertex   -4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   -4.747953e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 5.227884e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -3.561030e+00 -1.085394e+01 -1.187542e+01
      vertex   -4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   -3.561030e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 5.123565e-15 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -3.561030e+00 -1.076831e+01 -1.195203e+01
      vertex   -4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
    endloop
  endfacet
  facet normal 4.051410e-15 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -3.561030e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -2.374183e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 3.323335e-16 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -2.374183e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   1.592307e-14 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 4.401963e-16 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -2.374183e+00 -1.076831e+01 -1.195203e+01
      vertex   1.592307e-14 -1.076831e+01 -1.195203e+01
      vertex   1.583315e-14 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   1.583315e-14 -1.085394e+01 -1.187542e+01
      vertex   1.592307e-14 -1.076831e+01 -1.195203e+01
      vertex   2.374183e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   1.583315e-14 -1.085394e+01 -1.187542e+01
      vertex   2.374183e+00 -1.085394e+01 -1.187542e+01
      vertex   2.374183e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   2.374183e+00 -1.096651e+01 -1.176651e+01
      vertex   2.374183e+00 -1.085394e+01 -1.187542e+01
      vertex   4.747953e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   2.374183e+00 -1.096651e+01 -1.176651e+01
      vertex   4.747953e+00 -1.096651e+01 -1.176651e+01
      vertex   4.747953e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 5.285734e-16 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   4.747953e+00 -1.096651e+01 -1.176651e+01
      vertex   9.500000e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 5.278314e-16 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   9.500000e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 7.549865e-16 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   2.374183e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   2.374183e+00 -1.076831e+01 -1.195203e+01
      vertex   1.592307e-14 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   1.592307e-14 -1.076831e+01 -1.195203e+01
      vertex   2.374183e+00 -1.076831e+01 -1.195203e+01
      vertex   2.374183e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 7.770844e-16 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   4.747953e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 5.273925e-16 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   4.747953e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   2.374183e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   2.374183e+00 -1.076831e+01 -1.195203e+01
      vertex   4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   2.374183e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 5.285734e-16 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   4.747953e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   4.747953e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   4.747953e+00 -1.096651e+01 -1.176651e+01
      vertex   2.374183e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   4.747953e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.026191e-15 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   9.500000e+00 -1.115203e+01 -1.156831e+01
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 9.852427e-16 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   9.500000e+00 -1.115203e+01 -1.156831e+01
      vertex   9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal -1.593807e-03 -8.571645e-01 -5.150402e-01
    outer loop
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   9.500000e+00 -1.119781e+01 -1.150684e+01
    endloop
  endfacet
  facet normal -5.226111e-03 -9.523068e-01 -3.050974e-01
    outer loop
      vertex   9.500000e+00 -1.119781e+01 -1.150684e+01
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 1.793632e-04 -8.125069e-01 -5.829516e-01
    outer loop
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   2.374183e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   2.374183e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   1.592307e-14 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   2.374183e+00 -1.115203e+01 -1.156831e+01
      vertex   1.592307e-14 -1.115203e+01 -1.156831e+01
      vertex   1.583315e-14 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 7.483387e-15 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   1.583315e-14 -1.107542e+01 -1.165394e+01
      vertex   1.592307e-14 -1.115203e+01 -1.156831e+01
      vertex   -2.374183e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 7.803741e-15 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   1.583315e-14 -1.107542e+01 -1.165394e+01
      vertex   -2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   -2.374183e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.141291e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -2.374183e+00 -1.096651e+01 -1.176651e+01
      vertex   -2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   -3.561030e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.186715e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -2.374183e+00 -1.096651e+01 -1.176651e+01
      vertex   -3.561030e+00 -1.096651e+01 -1.176651e+01
      vertex   -3.561030e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 4.421329e-15 -9.523198e-01 -3.051016e-01
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   -9.500000e+00 -1.119781e+01 -1.150684e+01
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
    endloop
  endfacet
  facet normal 8.657003e-05 -8.571656e-01 -5.150409e-01
    outer loop
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   -9.500000e+00 -1.119781e+01 -1.150684e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal -2.515856e-13 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -9.500000e+00 -1.115203e+01 -1.156831e+01
      vertex   -8.905377e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal 1.288459e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -8.905377e+00 -1.115203e+01 -1.156831e+01
      vertex   -8.310975e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 1.104510e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -8.310975e+00 -1.115203e+01 -1.156831e+01
      vertex   -7.716772e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 1.196018e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -7.716772e+00 -1.115203e+01 -1.156831e+01
      vertex   -8.310975e+00 -1.115203e+01 -1.156831e+01
      vertex   -8.310975e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.020134e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -7.716772e+00 -1.115203e+01 -1.156831e+01
      vertex   -8.310975e+00 -1.107542e+01 -1.165394e+01
      vertex   -7.716772e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.046327e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -7.716772e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.310975e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.310975e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 4.081962e-15 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -7.716772e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.310975e+00 -1.096651e+01 -1.176651e+01
      vertex   -7.716772e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 4.366768e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -7.716772e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.310975e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.310975e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -2.726635e-13 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -9.500000e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.905377e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal -2.106873e-13 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -8.905377e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.905377e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.394887e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -8.905377e+00 -1.115203e+01 -1.156831e+01
      vertex   -8.905377e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.310975e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 5.740305e-15 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -8.310975e+00 -1.115203e+01 -1.156831e+01
      vertex   -8.905377e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.310975e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal -2.200467e-13 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   -9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.905377e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal -1.451891e-13 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -8.905377e+00 -1.107542e+01 -1.165394e+01
      vertex   -9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.905377e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 6.164235e-15 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -8.905377e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.905377e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.310975e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 2.012349e-15 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -8.310975e+00 -1.107542e+01 -1.165394e+01
      vertex   -8.905377e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.310975e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal -1.504972e-13 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   -9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   -8.905377e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal -7.128144e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -8.905377e+00 -1.096651e+01 -1.176651e+01
      vertex   -9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   -8.905377e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 2.217538e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -8.905377e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.905377e+00 -1.085394e+01 -1.187542e+01
      vertex   -8.310975e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 2.142779e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -8.310975e+00 -1.096651e+01 -1.176651e+01
      vertex   -8.905377e+00 -1.085394e+01 -1.187542e+01
      vertex   -8.310975e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -7.487452e-14 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   -9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   -8.905377e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -2.565672e-14 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -8.905377e+00 -1.085394e+01 -1.187542e+01
      vertex   -9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 2.227143e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -8.905377e+00 -1.085394e+01 -1.187542e+01
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
      vertex   -8.310975e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -2.845290e-14 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   -9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 1.273621e-02 -5.149991e-01 -8.570961e-01
    outer loop
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
      vertex   -9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -9.500000e+00 -1.070684e+01 -1.199781e+01
    endloop
  endfacet
  facet normal 4.172969e-02 -3.048358e-01 -9.514903e-01
    outer loop
      vertex   -8.905377e+00 -1.076831e+01 -1.195203e+01
      vertex   -9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
    endloop
  endfacet
  facet normal 2.815509e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -7.122746e+00 -1.107542e+01 -1.165394e+01
      vertex   -6.528873e+00 -1.115203e+01 -1.156831e+01
      vertex   -7.122746e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 2.630833e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -7.122746e+00 -1.115203e+01 -1.156831e+01
      vertex   -6.528873e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal 1.238017e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -7.122746e+00 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -7.716772e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 1.935875e-14 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   -3.561030e+00 -1.115203e+01 -1.156831e+01
      vertex   -2.374183e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 2.095781e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -2.374183e+00 -1.115203e+01 -1.156831e+01
      vertex   -3.561030e+00 -1.115203e+01 -1.156831e+01
      vertex   -3.561030e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.996519e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -2.374183e+00 -1.115203e+01 -1.156831e+01
      vertex   -3.561030e+00 -1.107542e+01 -1.165394e+01
      vertex   -2.374183e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 2.081428e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   -3.561030e+00 -1.107542e+01 -1.165394e+01
      vertex   -3.561030e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 9.420935e-15 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   1.592307e-14 -1.115203e+01 -1.156831e+01
      vertex   -2.374183e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 8.627980e-15 -7.877671e-01 -6.159732e-01
    outer loop
      vertex   -2.374183e+00 -1.115203e+01 -1.156831e+01
      vertex   1.592307e-14 -1.115203e+01 -1.156831e+01
      vertex   -9.500000e+00 -1.119019e+01 -1.151951e+01
    endloop
  endfacet
  facet normal -3.170243e-15 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -7.716772e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -7.122746e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 1.024003e-14 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -7.122746e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -6.528873e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 1.044167e-14 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -7.122746e+00 -1.076831e+01 -1.195203e+01
      vertex   -6.528873e+00 -1.076831e+01 -1.195203e+01
      vertex   -6.528873e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -3.755118e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -6.528873e+00 -1.085394e+01 -1.187542e+01
      vertex   -6.528873e+00 -1.076831e+01 -1.195203e+01
      vertex   -5.935131e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal -4.090778e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -6.528873e+00 -1.085394e+01 -1.187542e+01
      vertex   -5.935131e+00 -1.085394e+01 -1.187542e+01
      vertex   -5.935131e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.404947e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -5.935131e+00 -1.096651e+01 -1.176651e+01
      vertex   -5.935131e+00 -1.085394e+01 -1.187542e+01
      vertex   -4.747953e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.345563e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -5.935131e+00 -1.096651e+01 -1.176651e+01
      vertex   -4.747953e+00 -1.096651e+01 -1.176651e+01
      vertex   -4.747953e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   2.374183e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   2.374183e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   2.374183e+00 -1.115203e+01 -1.156831e+01
      vertex   1.583315e-14 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   2.374183e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   2.374183e+00 -1.096651e+01 -1.176651e+01
      vertex   2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   1.579668e-14 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal -0.000000e+00 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   2.374183e+00 -1.096651e+01 -1.176651e+01
      vertex   1.579668e-14 -1.096651e+01 -1.176651e+01
      vertex   1.583315e-14 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 3.191366e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   1.583315e-14 -1.085394e+01 -1.187542e+01
      vertex   1.579668e-14 -1.096651e+01 -1.176651e+01
      vertex   -2.374183e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 3.228139e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   1.583315e-14 -1.085394e+01 -1.187542e+01
      vertex   -2.374183e+00 -1.085394e+01 -1.187542e+01
      vertex   -2.374183e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 3.581056e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -2.374183e+00 -1.076831e+01 -1.195203e+01
      vertex   -2.374183e+00 -1.085394e+01 -1.187542e+01
      vertex   -3.561030e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   1.579668e-14 -1.096651e+01 -1.176651e+01
      vertex   2.374183e+00 -1.107542e+01 -1.165394e+01
      vertex   1.583315e-14 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 5.877816e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -2.374183e+00 -1.085394e+01 -1.187542e+01
      vertex   1.579668e-14 -1.096651e+01 -1.176651e+01
      vertex   -2.374183e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 5.757678e-15 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -2.374183e+00 -1.096651e+01 -1.176651e+01
      vertex   1.579668e-14 -1.096651e+01 -1.176651e+01
      vertex   1.583315e-14 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 7.329735e-15 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   -4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   -5.935131e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 6.807957e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -5.935131e+00 -1.076831e+01 -1.195203e+01
      vertex   -4.747953e+00 -1.076831e+01 -1.195203e+01
      vertex   -4.747953e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 7.922798e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -5.935131e+00 -1.076831e+01 -1.195203e+01
      vertex   -4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   -5.935131e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 7.562414e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -5.935131e+00 -1.085394e+01 -1.187542e+01
      vertex   -4.747953e+00 -1.085394e+01 -1.187542e+01
      vertex   -4.747953e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 2.582308e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -3.561030e+00 -1.076831e+01 -1.195203e+01
      vertex   -2.374183e+00 -1.085394e+01 -1.187542e+01
      vertex   -3.561030e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 2.256136e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -3.561030e+00 -1.085394e+01 -1.187542e+01
      vertex   -2.374183e+00 -1.085394e+01 -1.187542e+01
      vertex   -2.374183e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal -1.267577e-14 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -5.935131e+00 -1.085394e+01 -1.187542e+01
      vertex   -6.528873e+00 -1.076831e+01 -1.195203e+01
      vertex   -5.935131e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal -1.259914e-14 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -5.935131e+00 -1.076831e+01 -1.195203e+01
      vertex   -6.528873e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
    endloop
  endfacet
  facet normal 2.223207e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -7.716772e+00 -1.085394e+01 -1.187542e+01
      vertex   -8.310975e+00 -1.076831e+01 -1.195203e+01
      vertex   -7.716772e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 2.355013e-15 -6.159732e-01 -7.877671e-01
    outer loop
      vertex   -7.716772e+00 -1.076831e+01 -1.195203e+01
      vertex   -8.310975e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
    endloop
  endfacet
  facet normal 1.872176e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   -4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   -5.935131e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 2.494473e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -5.935131e+00 -1.107542e+01 -1.165394e+01
      vertex   -4.747953e+00 -1.115203e+01 -1.156831e+01
      vertex   -5.935131e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 2.217874e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -5.935131e+00 -1.107542e+01 -1.165394e+01
      vertex   -5.935131e+00 -1.115203e+01 -1.156831e+01
      vertex   -6.528873e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.969817e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -4.747953e+00 -1.107542e+01 -1.165394e+01
      vertex   -5.935131e+00 -1.107542e+01 -1.165394e+01
      vertex   -5.935131e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.040156e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -5.935131e+00 -1.096651e+01 -1.176651e+01
      vertex   -5.935131e+00 -1.107542e+01 -1.165394e+01
      vertex   -6.528873e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.075079e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -5.935131e+00 -1.096651e+01 -1.176651e+01
      vertex   -6.528873e+00 -1.096651e+01 -1.176651e+01
      vertex   -6.528873e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 8.528900e-15 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -6.528873e+00 -1.085394e+01 -1.187542e+01
      vertex   -6.528873e+00 -1.096651e+01 -1.176651e+01
      vertex   -7.122746e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 8.681850e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -6.528873e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.122746e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.122746e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal -3.753315e-15 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -7.122746e+00 -1.076831e+01 -1.195203e+01
      vertex   -7.122746e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.716772e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 2.294391e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -6.528873e+00 -1.096651e+01 -1.176651e+01
      vertex   -5.935131e+00 -1.107542e+01 -1.165394e+01
      vertex   -6.528873e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.283083e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -7.122746e+00 -1.085394e+01 -1.187542e+01
      vertex   -6.528873e+00 -1.096651e+01 -1.176651e+01
      vertex   -7.122746e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 1.254894e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -7.122746e+00 -1.096651e+01 -1.176651e+01
      vertex   -6.528873e+00 -1.096651e+01 -1.176651e+01
      vertex   -6.528873e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.372309e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -7.716772e+00 -1.115203e+01 -1.156831e+01
      vertex   -7.716772e+00 -1.107542e+01 -1.165394e+01
      vertex   -7.122746e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 1.993855e-14 -7.452430e-01 -6.667929e-01
    outer loop
      vertex   -7.122746e+00 -1.115203e+01 -1.156831e+01
      vertex   -7.716772e+00 -1.107542e+01 -1.165394e+01
      vertex   -7.122746e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 2.079313e-14 -7.186833e-01 -6.953375e-01
    outer loop
      vertex   -7.716772e+00 -1.107542e+01 -1.165394e+01
      vertex   -7.716772e+00 -1.096651e+01 -1.176651e+01
      vertex   -7.122746e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 1.513500e-14 -6.667929e-01 -7.452430e-01
    outer loop
      vertex   -7.716772e+00 -1.076831e+01 -1.195203e+01
      vertex   -7.122746e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.716772e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 1.490426e-14 -6.953375e-01 -7.186833e-01
    outer loop
      vertex   -7.716772e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.122746e+00 -1.085394e+01 -1.187542e+01
      vertex   -7.122746e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 9.481548e-01 -3.037672e-01 -9.342319e-02
    outer loop
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
    endloop
  endfacet
  facet normal 9.948426e-01 -3.790053e-02 -9.408344e-02
    outer loop
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
      vertex   1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   1.196197e+01 -1.071951e+01 -9.873870e+00
    endloop
  endfacet
  facet normal 8.225950e-01 -5.439417e-01 -1.657253e-01
    outer loop
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
      vertex   1.196197e+01 -1.071951e+01 -9.873870e+00
      vertex   1.191545e+01 -1.071951e+01 -1.010476e+01
    endloop
  endfacet
  facet normal 7.725896e-01 -6.155307e-01 -1.556509e-01
    outer loop
      vertex   1.191545e+01 -1.071951e+01 -1.010476e+01
      vertex   1.196197e+01 -1.071951e+01 -9.873870e+00
      vertex   1.192424e+01 -1.076831e+01 -9.868141e+00
    endloop
  endfacet
  facet normal 7.725896e-01 -6.155307e-01 -1.556509e-01
    outer loop
      vertex   1.191545e+01 -1.071951e+01 -1.010476e+01
      vertex   1.192424e+01 -1.076831e+01 -9.868141e+00
      vertex   1.187844e+01 -1.076831e+01 -1.009549e+01
    endloop
  endfacet
  facet normal 7.396306e-01 -6.563096e-01 -1.490108e-01
    outer loop
      vertex   1.187844e+01 -1.076831e+01 -1.009549e+01
      vertex   1.192424e+01 -1.076831e+01 -9.868141e+00
      vertex   1.189130e+01 -1.080658e+01 -9.863138e+00
    endloop
  endfacet
  facet normal 7.396306e-01 -6.563096e-01 -1.490108e-01
    outer loop
      vertex   1.187844e+01 -1.076831e+01 -1.009549e+01
      vertex   1.189130e+01 -1.080658e+01 -9.863138e+00
      vertex   1.184612e+01 -1.080658e+01 -1.008740e+01
    endloop
  endfacet
  facet normal 7.239756e-01 -6.742293e-01 -1.458568e-01
    outer loop
      vertex   1.184612e+01 -1.080658e+01 -1.008740e+01
      vertex   1.189130e+01 -1.080658e+01 -9.863138e+00
      vertex   1.184849e+01 -1.085394e+01 -9.856638e+00
    endloop
  endfacet
  facet normal 7.239756e-01 -6.742293e-01 -1.458568e-01
    outer loop
      vertex   1.184612e+01 -1.080658e+01 -1.008740e+01
      vertex   1.184849e+01 -1.085394e+01 -9.856638e+00
      vertex   1.180412e+01 -1.085394e+01 -1.007689e+01
    endloop
  endfacet
  facet normal 7.109844e-01 -6.884647e-01 -1.432395e-01
    outer loop
      vertex   1.180412e+01 -1.085394e+01 -1.007689e+01
      vertex   1.184849e+01 -1.085394e+01 -9.856638e+00
      vertex   1.179729e+01 -1.090844e+01 -9.848862e+00
    endloop
  endfacet
  facet normal 7.109844e-01 -6.884647e-01 -1.432395e-01
    outer loop
      vertex   1.180412e+01 -1.085394e+01 -1.007689e+01
      vertex   1.179729e+01 -1.090844e+01 -9.848862e+00
      vertex   1.175388e+01 -1.090844e+01 -1.006431e+01
    endloop
  endfacet
  facet normal 6.992751e-01 -7.008331e-01 -1.408805e-01
    outer loop
      vertex   1.175388e+01 -1.090844e+01 -1.006431e+01
      vertex   1.179729e+01 -1.090844e+01 -9.848862e+00
      vertex   1.174082e+01 -1.096651e+01 -9.840287e+00
    endloop
  endfacet
  facet normal 6.992751e-01 -7.008331e-01 -1.408805e-01
    outer loop
      vertex   1.175388e+01 -1.090844e+01 -1.006431e+01
      vertex   1.174082e+01 -1.096651e+01 -9.840287e+00
      vertex   1.169848e+01 -1.096651e+01 -1.005044e+01
    endloop
  endfacet
  facet normal 6.820490e-01 -7.182811e-01 -1.374100e-01
    outer loop
      vertex   1.169848e+01 -1.096651e+01 -1.005044e+01
      vertex   1.174082e+01 -1.096651e+01 -9.840287e+00
      vertex   1.162953e+01 -1.107542e+01 -9.823386e+00
    endloop
  endfacet
  facet normal 6.820490e-01 -7.182811e-01 -1.374100e-01
    outer loop
      vertex   1.169848e+01 -1.096651e+01 -1.005044e+01
      vertex   1.162953e+01 -1.107542e+01 -9.823386e+00
      vertex   1.158929e+01 -1.107542e+01 -1.002310e+01
    endloop
  endfacet
  facet normal 6.540793e-01 -7.448594e-01 -1.317751e-01
    outer loop
      vertex   1.158929e+01 -1.107542e+01 -1.002310e+01
      vertex   1.162953e+01 -1.107542e+01 -9.823386e+00
      vertex   1.154487e+01 -1.115203e+01 -9.810530e+00
    endloop
  endfacet
  facet normal 6.540793e-01 -7.448594e-01 -1.317751e-01
    outer loop
      vertex   1.158929e+01 -1.107542e+01 -1.002310e+01
      vertex   1.154487e+01 -1.115203e+01 -9.810530e+00
      vertex   1.150623e+01 -1.115203e+01 -1.000230e+01
    endloop
  endfacet
  facet normal 6.042741e-01 -7.874211e-01 -1.217410e-01
    outer loop
      vertex   1.150623e+01 -1.115203e+01 -1.000230e+01
      vertex   1.154487e+01 -1.115203e+01 -9.810530e+00
      vertex   1.149662e+01 -1.119019e+01 -9.803203e+00
    endloop
  endfacet
  facet normal 6.042741e-01 -7.874211e-01 -1.217410e-01
    outer loop
      vertex   1.150623e+01 -1.115203e+01 -1.000230e+01
      vertex   1.149662e+01 -1.119019e+01 -9.803203e+00
      vertex   1.145890e+01 -1.119019e+01 -9.990452e+00
    endloop
  endfacet
  facet normal 4.853684e-01 -8.688242e-01 -9.778547e-02
    outer loop
      vertex   1.145890e+01 -1.119019e+01 -9.990452e+00
      vertex   1.149662e+01 -1.119019e+01 -9.803203e+00
      vertex   1.146156e+01 -1.120000e+01 -9.890099e+00
    endloop
  endfacet
  facet normal 3.311594e-01 -9.382106e-01 -1.004701e-01
    outer loop
      vertex   1.145890e+01 -1.119019e+01 -9.990452e+00
      vertex   1.146156e+01 -1.120000e+01 -9.890099e+00
      vertex   1.140344e+01 -1.119019e+01 -1.017326e+01
    endloop
  endfacet
  facet normal 3.261002e-01 -9.400847e-01 -9.949641e-02
    outer loop
      vertex   1.140344e+01 -1.119019e+01 -1.017326e+01
      vertex   1.146156e+01 -1.120000e+01 -9.890099e+00
      vertex   1.134719e+01 -1.120000e+01 -1.026495e+01
    endloop
  endfacet
  facet normal 4.563328e-01 -8.699627e-01 -1.868833e-01
    outer loop
      vertex   1.140344e+01 -1.119019e+01 -1.017326e+01
      vertex   1.134719e+01 -1.120000e+01 -1.026495e+01
      vertex   1.133101e+01 -1.119019e+01 -1.035010e+01
    endloop
  endfacet
  facet normal 3.127757e-01 -9.350133e-01 -1.670974e-01
    outer loop
      vertex   1.133101e+01 -1.119019e+01 -1.035010e+01
      vertex   1.134719e+01 -1.120000e+01 -1.026495e+01
      vertex   1.116243e+01 -1.120000e+01 -1.061079e+01
    endloop
  endfacet
  facet normal 4.932691e-01 -8.207765e-01 -2.881172e-01
    outer loop
      vertex   1.133101e+01 -1.119019e+01 -1.035010e+01
      vertex   1.116243e+01 -1.120000e+01 -1.061079e+01
      vertex   1.113842e+01 -1.119019e+01 -1.067982e+01
    endloop
  endfacet
  facet normal 2.813627e-01 -9.315879e-01 -2.301717e-01
    outer loop
      vertex   1.113842e+01 -1.119019e+01 -1.067982e+01
      vertex   1.116243e+01 -1.120000e+01 -1.061079e+01
      vertex   1.091421e+01 -1.120000e+01 -1.091421e+01
    endloop
  endfacet
  facet normal 4.155888e-01 -8.341303e-01 -3.626466e-01
    outer loop
      vertex   1.113842e+01 -1.119019e+01 -1.067982e+01
      vertex   1.091421e+01 -1.120000e+01 -1.091421e+01
      vertex   1.088743e+01 -1.119019e+01 -1.096746e+01
    endloop
  endfacet
  facet normal 2.380402e-01 -9.268216e-01 -2.904112e-01
    outer loop
      vertex   1.088743e+01 -1.119019e+01 -1.096746e+01
      vertex   1.091421e+01 -1.120000e+01 -1.091421e+01
      vertex   1.061103e+01 -1.120000e+01 -1.116272e+01
    endloop
  endfacet
  facet normal 3.226260e-01 -8.512132e-01 -4.139428e-01
    outer loop
      vertex   1.088743e+01 -1.119019e+01 -1.096746e+01
      vertex   1.061103e+01 -1.120000e+01 -1.116272e+01
      vertex   1.058633e+01 -1.119019e+01 -1.120214e+01
    endloop
  endfacet
  facet normal 2.033875e-01 -9.126666e-01 -3.545041e-01
    outer loop
      vertex   1.058633e+01 -1.119019e+01 -1.120214e+01
      vertex   1.061103e+01 -1.120000e+01 -1.116272e+01
      vertex   1.042057e+01 -1.119019e+01 -1.129724e+01
    endloop
  endfacet
  facet normal 3.067685e-01 -7.873958e-01 -5.346970e-01
    outer loop
      vertex   1.058633e+01 -1.119019e+01 -1.120214e+01
      vertex   1.042057e+01 -1.119019e+01 -1.129724e+01
      vertex   1.044282e+01 -1.115203e+01 -1.134067e+01
    endloop
  endfacet
  facet normal 2.551817e-01 -7.874090e-01 -5.611322e-01
    outer loop
      vertex   1.044282e+01 -1.115203e+01 -1.134067e+01
      vertex   1.042057e+01 -1.119019e+01 -1.129724e+01
      vertex   1.026465e+01 -1.115203e+01 -1.142169e+01
    endloop
  endfacet
  facet normal 2.762134e-01 -7.448461e-01 -6.073799e-01
    outer loop
      vertex   1.044282e+01 -1.115203e+01 -1.134067e+01
      vertex   1.026465e+01 -1.115203e+01 -1.142169e+01
      vertex   1.029631e+01 -1.107542e+01 -1.150125e+01
    endloop
  endfacet
  facet normal 2.173235e-01 -7.448647e-01 -6.308304e-01
    outer loop
      vertex   1.029631e+01 -1.107542e+01 -1.150125e+01
      vertex   1.026465e+01 -1.115203e+01 -1.142169e+01
      vertex   1.010356e+01 -1.107542e+01 -1.156765e+01
    endloop
  endfacet
  facet normal 2.266168e-01 -7.182866e-01 -6.578063e-01
    outer loop
      vertex   1.029631e+01 -1.107542e+01 -1.150125e+01
      vertex   1.010356e+01 -1.107542e+01 -1.156765e+01
      vertex   1.013510e+01 -1.096651e+01 -1.167571e+01
    endloop
  endfacet
  facet normal 1.630560e-01 -7.182917e-01 -6.763651e-01
    outer loop
      vertex   1.013510e+01 -1.096651e+01 -1.167571e+01
      vertex   1.010356e+01 -1.107542e+01 -1.156765e+01
      vertex   9.926617e+00 -1.096651e+01 -1.172597e+01
    endloop
  endfacet
  facet normal 1.671744e-01 -7.008439e-01 -6.934483e-01
    outer loop
      vertex   1.013510e+01 -1.096651e+01 -1.167571e+01
      vertex   9.926617e+00 -1.096651e+01 -1.172597e+01
      vertex   9.937367e+00 -1.090844e+01 -1.178206e+01
    endloop
  endfacet
  facet normal 1.009871e-01 -7.008422e-01 -7.061316e-01
    outer loop
      vertex   9.937367e+00 -1.090844e+01 -1.178206e+01
      vertex   9.926617e+00 -1.096651e+01 -1.172597e+01
      vertex   9.719737e+00 -1.090844e+01 -1.181319e+01
    endloop
  endfacet
  facet normal 1.026782e-01 -6.884740e-01 -7.179560e-01
    outer loop
      vertex   9.937367e+00 -1.090844e+01 -1.178206e+01
      vertex   9.719737e+00 -1.090844e+01 -1.181319e+01
      vertex   9.724635e+00 -1.085394e+01 -1.186475e+01
    endloop
  endfacet
  facet normal 3.441191e-02 -6.884757e-01 -7.244426e-01
    outer loop
      vertex   9.724635e+00 -1.085394e+01 -1.186475e+01
      vertex   9.719737e+00 -1.090844e+01 -1.181319e+01
      vertex   9.500000e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 3.504071e-02 -6.742404e-01 -7.376801e-01
    outer loop
      vertex   9.724635e+00 -1.085394e+01 -1.186475e+01
      vertex   9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   9.728729e+00 -1.080658e+01 -1.190785e+01
    endloop
  endfacet
  facet normal 3.240909e-02 -6.664427e-01 -7.448516e-01
    outer loop
      vertex   9.728729e+00 -1.080658e+01 -1.190785e+01
      vertex   9.500000e+00 -1.085394e+01 -1.187542e+01
      vertex   9.500000e+00 -1.076831e+01 -1.195203e+01
    endloop
  endfacet
  facet normal 3.579845e-02 -6.563209e-01 -7.536321e-01
    outer loop
      vertex   9.728729e+00 -1.080658e+01 -1.190785e+01
      vertex   9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   9.731880e+00 -1.076831e+01 -1.194102e+01
    endloop
  endfacet
  facet normal 3.739373e-02 -6.155424e-01 -7.872162e-01
    outer loop
      vertex   9.731880e+00 -1.076831e+01 -1.194102e+01
      vertex   9.500000e+00 -1.076831e+01 -1.195203e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
    endloop
  endfacet
  facet normal 3.739373e-02 -6.155424e-01 -7.872162e-01
    outer loop
      vertex   9.731880e+00 -1.076831e+01 -1.194102e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   9.735488e+00 -1.071951e+01 -1.197901e+01
    endloop
  endfacet
  facet normal 4.068271e-02 -5.146145e-01 -8.564560e-01
    outer loop
      vertex   9.735488e+00 -1.071951e+01 -1.197901e+01
      vertex   9.500000e+00 -1.071951e+01 -1.199019e+01
      vertex   9.500000e+00 -1.070684e+01 -1.199781e+01
    endloop
  endfacet
  facet normal 5.950433e-02 -3.045610e-01 -9.506323e-01
    outer loop
      vertex   9.735488e+00 -1.071951e+01 -1.197901e+01
      vertex   9.500000e+00 -1.070684e+01 -1.199781e+01
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
    endloop
  endfacet
  facet normal 9.690021e-01 2.256693e-01 -1.005396e-01
    outer loop
      vertex   1.196197e+01 -1.071951e+01 -9.873870e+00
      vertex   1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   1.198628e+01 -1.071951e+01 -9.639563e+00
    endloop
  endfacet
  facet normal 8.569179e-01 -5.148920e-01 -2.404018e-02
    outer loop
      vertex   1.198628e+01 -1.071951e+01 -9.639563e+00
      vertex   1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   1.199019e+01 -1.071951e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 7.875748e-01 -6.158228e-01 -2.209481e-02
    outer loop
      vertex   1.198628e+01 -1.071951e+01 -9.639563e+00
      vertex   1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 7.451490e-01 -6.667088e-01 -1.588740e-02
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   1.191491e+01 -1.080658e+01 -9.635557e+00
      vertex   1.195203e+01 -1.076831e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 7.539467e-01 -6.565950e-01 -2.115140e-02
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   1.191491e+01 -1.080658e+01 -9.635557e+00
      vertex   1.194818e+01 -1.076831e+01 -9.637424e+00
    endloop
  endfacet
  facet normal 7.875748e-01 -6.158228e-01 -2.209481e-02
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   1.194818e+01 -1.076831e+01 -9.637424e+00
      vertex   1.198628e+01 -1.071951e+01 -9.639563e+00
    endloop
  endfacet
  facet normal 7.838937e-01 -6.155449e-01 -8.133355e-02
    outer loop
      vertex   1.198628e+01 -1.071951e+01 -9.639563e+00
      vertex   1.194818e+01 -1.076831e+01 -9.637424e+00
      vertex   1.196197e+01 -1.071951e+01 -9.873870e+00
    endloop
  endfacet
  facet normal 7.186025e-01 -6.952593e-01 -1.499825e-02
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   1.181997e+01 -1.090844e+01 -9.630228e+00
      vertex   1.187542e+01 -1.085394e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 7.247221e-01 -6.887413e-01 -2.033153e-02
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   1.181997e+01 -1.090844e+01 -9.630228e+00
      vertex   1.187168e+01 -1.085394e+01 -9.633131e+00
    endloop
  endfacet
  facet normal 7.379752e-01 -6.745101e-01 -2.070334e-02
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   1.187168e+01 -1.085394e+01 -9.633131e+00
      vertex   1.191491e+01 -1.080658e+01 -9.635557e+00
    endloop
  endfacet
  facet normal 7.345663e-01 -6.742429e-01 -7.621555e-02
    outer loop
      vertex   1.191491e+01 -1.080658e+01 -9.635557e+00
      vertex   1.187168e+01 -1.085394e+01 -9.633131e+00
      vertex   1.189130e+01 -1.080658e+01 -9.863138e+00
    endloop
  endfacet
  facet normal 7.504510e-01 -6.563235e-01 -7.786368e-02
    outer loop
      vertex   1.191491e+01 -1.080658e+01 -9.635557e+00
      vertex   1.189130e+01 -1.080658e+01 -9.863138e+00
      vertex   1.192424e+01 -1.076831e+01 -9.868141e+00
    endloop
  endfacet
  facet normal 7.127772e-01 -7.011054e-01 -1.999642e-02
    outer loop
      vertex   1.181997e+01 -1.090844e+01 -9.630228e+00
      vertex   1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   1.176295e+01 -1.096651e+01 -9.627027e+00
    endloop
  endfacet
  facet normal 6.952053e-01 -7.185466e-01 -1.950346e-02
    outer loop
      vertex   1.176295e+01 -1.096651e+01 -9.627027e+00
      vertex   1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   1.165394e+01 -1.107542e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.952053e-01 -7.185466e-01 -1.950346e-02
    outer loop
      vertex   1.176295e+01 -1.096651e+01 -9.627027e+00
      vertex   1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   1.165056e+01 -1.107542e+01 -9.620718e+00
    endloop
  endfacet
  facet normal 6.666763e-01 -7.451127e-01 -1.870310e-02
    outer loop
      vertex   1.165056e+01 -1.107542e+01 -9.620718e+00
      vertex   1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.666763e-01 -7.451127e-01 -1.870310e-02
    outer loop
      vertex   1.165056e+01 -1.107542e+01 -9.620718e+00
      vertex   1.156831e+01 -1.115203e+01 -9.500000e+00
      vertex   1.156506e+01 -1.115203e+01 -9.615919e+00
    endloop
  endfacet
  facet normal 6.158812e-01 -7.876495e-01 -1.727808e-02
    outer loop
      vertex   1.156506e+01 -1.115203e+01 -9.615919e+00
      vertex   1.156831e+01 -1.115203e+01 -9.500000e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.158812e-01 -7.876495e-01 -1.727808e-02
    outer loop
      vertex   1.156506e+01 -1.115203e+01 -9.615919e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.151634e+01 -1.119019e+01 -9.613184e+00
    endloop
  endfacet
  facet normal 5.149871e-01 -8.570762e-01 -1.444757e-02
    outer loop
      vertex   1.151634e+01 -1.119019e+01 -9.613184e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.150684e+01 -1.119781e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 3.048761e-01 -9.516161e-01 -3.843645e-02
    outer loop
      vertex   1.151634e+01 -1.119019e+01 -9.613184e+00
      vertex   1.150684e+01 -1.119781e+01 -9.500000e+00
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 3.357872e-01 -9.413566e-01 -3.308564e-02
    outer loop
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   1.146156e+01 -1.120000e+01 -9.890099e+00
      vertex   1.151634e+01 -1.119019e+01 -9.613184e+00
    endloop
  endfacet
  facet normal 3.521352e-01 -9.352358e-01 -3.653608e-02
    outer loop
      vertex   1.151634e+01 -1.119019e+01 -9.613184e+00
      vertex   1.146156e+01 -1.120000e+01 -9.890099e+00
      vertex   1.149662e+01 -1.119019e+01 -9.803203e+00
    endloop
  endfacet
  facet normal 6.131100e-01 -7.874322e-01 -6.361374e-02
    outer loop
      vertex   1.151634e+01 -1.119019e+01 -9.613184e+00
      vertex   1.149662e+01 -1.119019e+01 -9.803203e+00
      vertex   1.154487e+01 -1.115203e+01 -9.810530e+00
    endloop
  endfacet
  facet normal 1.522045e-01 -9.465158e-01 -2.845023e-01
    outer loop
      vertex   1.061103e+01 -1.120000e+01 -1.116272e+01
      vertex   1.026535e+01 -1.120000e+01 -1.134765e+01
      vertex   1.042057e+01 -1.119019e+01 -1.129724e+01
    endloop
  endfacet
  facet normal 1.950096e-01 -8.820927e-01 -4.288166e-01
    outer loop
      vertex   1.042057e+01 -1.119019e+01 -1.129724e+01
      vertex   1.026535e+01 -1.120000e+01 -1.134765e+01
      vertex   1.024661e+01 -1.119019e+01 -1.137635e+01
    endloop
  endfacet
  facet normal 2.551817e-01 -7.874090e-01 -5.611322e-01
    outer loop
      vertex   1.042057e+01 -1.119019e+01 -1.129724e+01
      vertex   1.024661e+01 -1.119019e+01 -1.137635e+01
      vertex   1.026465e+01 -1.115203e+01 -1.142169e+01
    endloop
  endfacet
  facet normal 2.007751e-01 -7.874258e-01 -5.827949e-01
    outer loop
      vertex   1.026465e+01 -1.115203e+01 -1.142169e+01
      vertex   1.024661e+01 -1.119019e+01 -1.137635e+01
      vertex   1.007957e+01 -1.115203e+01 -1.148545e+01
    endloop
  endfacet
  facet normal 2.173235e-01 -7.448647e-01 -6.308304e-01
    outer loop
      vertex   1.026465e+01 -1.115203e+01 -1.142169e+01
      vertex   1.007957e+01 -1.115203e+01 -1.148545e+01
      vertex   1.010356e+01 -1.107542e+01 -1.156765e+01
    endloop
  endfacet
  facet normal 1.563692e-01 -7.448695e-01 -6.486278e-01
    outer loop
      vertex   1.010356e+01 -1.107542e+01 -1.156765e+01
      vertex   1.007957e+01 -1.115203e+01 -1.148545e+01
      vertex   9.905429e+00 -1.107542e+01 -1.161542e+01
    endloop
  endfacet
  facet normal 1.630560e-01 -7.182917e-01 -6.763651e-01
    outer loop
      vertex   1.010356e+01 -1.107542e+01 -1.156765e+01
      vertex   9.905429e+00 -1.107542e+01 -1.161542e+01
      vertex   9.926617e+00 -1.096651e+01 -1.172597e+01
    endloop
  endfacet
  facet normal 9.849934e-02 -7.182900e-01 -6.887361e-01
    outer loop
      vertex   9.926617e+00 -1.096651e+01 -1.172597e+01
      vertex   9.905429e+00 -1.107542e+01 -1.161542e+01
      vertex   9.714335e+00 -1.096651e+01 -1.175633e+01
    endloop
  endfacet
  facet normal 1.009871e-01 -7.008422e-01 -7.061316e-01
    outer loop
      vertex   9.926617e+00 -1.096651e+01 -1.172597e+01
      vertex   9.714335e+00 -1.096651e+01 -1.175633e+01
      vertex   9.719737e+00 -1.090844e+01 -1.181319e+01
    endloop
  endfacet
  facet normal 3.384516e-02 -7.008439e-01 -7.125113e-01
    outer loop
      vertex   9.719737e+00 -1.090844e+01 -1.181319e+01
      vertex   9.714335e+00 -1.096651e+01 -1.175633e+01
      vertex   9.500000e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 3.106396e-02 -6.950020e-01 -7.183365e-01
    outer loop
      vertex   9.719737e+00 -1.090844e+01 -1.181319e+01
      vertex   9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   9.500000e+00 -1.085394e+01 -1.187542e+01
    endloop
  endfacet
  facet normal 1.376745e-01 -9.062785e-01 -3.996311e-01
    outer loop
      vertex   1.024661e+01 -1.119019e+01 -1.137635e+01
      vertex   1.026535e+01 -1.120000e+01 -1.134765e+01
      vertex   1.006589e+01 -1.119019e+01 -1.143861e+01
    endloop
  endfacet
  facet normal 9.279314e-02 -9.476078e-01 -3.056615e-01
    outer loop
      vertex   1.006589e+01 -1.119019e+01 -1.143861e+01
      vertex   1.026535e+01 -1.120000e+01 -1.134765e+01
      vertex   9.890201e+00 -1.120000e+01 -1.146154e+01
    endloop
  endfacet
  facet normal 1.080320e-01 -8.874206e-01 -4.481226e-01
    outer loop
      vertex   1.006589e+01 -1.119019e+01 -1.143861e+01
      vertex   9.890201e+00 -1.120000e+01 -1.146154e+01
      vertex   9.880125e+00 -1.119019e+01 -1.148339e+01
    endloop
  endfacet
  facet normal 6.182307e-02 -8.996153e-01 -4.322850e-01
    outer loop
      vertex   9.880125e+00 -1.119019e+01 -1.148339e+01
      vertex   9.890201e+00 -1.120000e+01 -1.146154e+01
      vertex   9.690978e+00 -1.119019e+01 -1.151044e+01
    endloop
  endfacet
  facet normal 8.726711e-02 -7.874287e-01 -6.101970e-01
    outer loop
      vertex   9.880125e+00 -1.119019e+01 -1.148339e+01
      vertex   9.690978e+00 -1.119019e+01 -1.151044e+01
      vertex   9.695593e+00 -1.115203e+01 -1.155902e+01
    endloop
  endfacet
  facet normal 2.924696e-02 -7.874301e-01 -6.157097e-01
    outer loop
      vertex   9.695593e+00 -1.115203e+01 -1.155902e+01
      vertex   9.690978e+00 -1.119019e+01 -1.151044e+01
      vertex   9.500000e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 3.165761e-02 -7.448695e-01 -6.664587e-01
    outer loop
      vertex   9.695593e+00 -1.115203e+01 -1.155902e+01
      vertex   9.500000e+00 -1.115203e+01 -1.156831e+01
      vertex   9.500000e+00 -1.107542e+01 -1.165394e+01
    endloop
  endfacet
  facet normal 3.005630e-02 -9.518896e-01 -3.049638e-01
    outer loop
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   9.500000e+00 -1.119781e+01 -1.150684e+01
      vertex   9.890201e+00 -1.120000e+01 -1.146154e+01
    endloop
  endfacet
  facet normal 3.174269e-02 -9.471353e-01 -3.192603e-01
    outer loop
      vertex   9.890201e+00 -1.120000e+01 -1.146154e+01
      vertex   9.500000e+00 -1.119781e+01 -1.150684e+01
      vertex   9.690978e+00 -1.119019e+01 -1.151044e+01
    endloop
  endfacet
  facet normal 2.445775e-02 -8.569092e-01 -5.148868e-01
    outer loop
      vertex   9.500000e+00 -1.119781e+01 -1.150684e+01
      vertex   9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   9.690978e+00 -1.119019e+01 -1.151044e+01
    endloop
  endfacet
  facet normal 2.924696e-02 -7.874301e-01 -6.157097e-01
    outer loop
      vertex   9.690978e+00 -1.119019e+01 -1.151044e+01
      vertex   9.500000e+00 -1.119019e+01 -1.151951e+01
      vertex   9.500000e+00 -1.115203e+01 -1.156831e+01
    endloop
  endfacet
  facet normal 3.165761e-02 -7.448695e-01 -6.664587e-01
    outer loop
      vertex   9.695593e+00 -1.115203e+01 -1.155902e+01
      vertex   9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   9.703690e+00 -1.107542e+01 -1.164427e+01
    endloop
  endfacet
  facet normal 3.301138e-02 -7.182916e-01 -6.949586e-01
    outer loop
      vertex   9.703690e+00 -1.107542e+01 -1.164427e+01
      vertex   9.500000e+00 -1.107542e+01 -1.165394e+01
      vertex   9.500000e+00 -1.096651e+01 -1.176651e+01
    endloop
  endfacet
  facet normal 3.301138e-02 -7.182916e-01 -6.949586e-01
    outer loop
      vertex   9.703690e+00 -1.107542e+01 -1.164427e+01
      vertex   9.500000e+00 -1.096651e+01 -1.176651e+01
      vertex   9.714335e+00 -1.096651e+01 -1.175633e+01
    endloop
  endfacet
  facet normal 9.746066e-02 1.123611e-01 -9.888763e-01
    outer loop
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   9.987751e+00 -1.070000e+01 -1.195193e+01
      vertex   9.735488e+00 -1.071951e+01 -1.197901e+01
    endloop
  endfacet
  facet normal 1.287907e-01 -4.152551e-01 -9.005422e-01
    outer loop
      vertex   9.735488e+00 -1.071951e+01 -1.197901e+01
      vertex   9.987751e+00 -1.070000e+01 -1.195193e+01
      vertex   9.968720e+00 -1.071951e+01 -1.194565e+01
    endloop
  endfacet
  facet normal 1.115753e-01 -6.155406e-01 -7.801671e-01
    outer loop
      vertex   9.735488e+00 -1.071951e+01 -1.197901e+01
      vertex   9.968720e+00 -1.071951e+01 -1.194565e+01
      vertex   9.961537e+00 -1.076831e+01 -1.190818e+01
    endloop
  endfacet
  facet normal 1.847022e-01 -6.155424e-01 -7.661545e-01
    outer loop
      vertex   9.961537e+00 -1.076831e+01 -1.190818e+01
      vertex   9.968720e+00 -1.071951e+01 -1.194565e+01
      vertex   1.018709e+01 -1.076831e+01 -1.185380e+01
    endloop
  endfacet
  facet normal 1.768224e-01 -6.563210e-01 -7.334689e-01
    outer loop
      vertex   9.961537e+00 -1.076831e+01 -1.190818e+01
      vertex   1.018709e+01 -1.076831e+01 -1.185380e+01
      vertex   1.017775e+01 -1.080658e+01 -1.182181e+01
    endloop
  endfacet
  facet normal 2.457492e-01 -6.563156e-01 -7.133423e-01
    outer loop
      vertex   1.017775e+01 -1.080658e+01 -1.182181e+01
      vertex   1.018709e+01 -1.076831e+01 -1.185380e+01
      vertex   1.039419e+01 -1.080658e+01 -1.174725e+01
    endloop
  endfacet
  facet normal 2.405476e-01 -6.742351e-01 -6.982434e-01
    outer loop
      vertex   1.017775e+01 -1.080658e+01 -1.182181e+01
      vertex   1.039419e+01 -1.080658e+01 -1.174725e+01
      vertex   1.037818e+01 -1.085394e+01 -1.170703e+01
    endloop
  endfacet
  facet normal 3.057289e-01 -6.742145e-01 -6.722831e-01
    outer loop
      vertex   1.037818e+01 -1.085394e+01 -1.170703e+01
      vertex   1.039419e+01 -1.080658e+01 -1.174725e+01
      vertex   1.058281e+01 -1.085394e+01 -1.161397e+01
    endloop
  endfacet
  facet normal 3.002431e-01 -6.884501e-01 -6.602200e-01
    outer loop
      vertex   1.037818e+01 -1.085394e+01 -1.170703e+01
      vertex   1.058281e+01 -1.085394e+01 -1.161397e+01
      vertex   1.055920e+01 -1.090844e+01 -1.156788e+01
    endloop
  endfacet
  facet normal 3.609371e-01 -6.884341e-01 -6.291128e-01
    outer loop
      vertex   1.055920e+01 -1.090844e+01 -1.156788e+01
      vertex   1.058281e+01 -1.085394e+01 -1.161397e+01
      vertex   1.074991e+01 -1.090844e+01 -1.145846e+01
    endloop
  endfacet
  facet normal 3.549933e-01 -7.008030e-01 -6.187527e-01
    outer loop
      vertex   1.055920e+01 -1.090844e+01 -1.156788e+01
      vertex   1.074991e+01 -1.090844e+01 -1.145846e+01
      vertex   1.071919e+01 -1.096651e+01 -1.141032e+01
    endloop
  endfacet
  facet normal 4.392378e-01 -6.996208e-01 -5.635608e-01
    outer loop
      vertex   1.071919e+01 -1.096651e+01 -1.141032e+01
      vertex   1.074991e+01 -1.090844e+01 -1.145846e+01
      vertex   1.105712e+01 -1.096651e+01 -1.114694e+01
    endloop
  endfacet
  facet normal 4.284536e-01 -7.170990e-01 -5.497241e-01
    outer loop
      vertex   1.071919e+01 -1.096651e+01 -1.141032e+01
      vertex   1.105712e+01 -1.096651e+01 -1.114694e+01
      vertex   1.097979e+01 -1.107542e+01 -1.106514e+01
    endloop
  endfacet
  facet normal 5.251624e-01 -7.170780e-01 -4.582615e-01
    outer loop
      vertex   1.097979e+01 -1.107542e+01 -1.106514e+01
      vertex   1.105712e+01 -1.096651e+01 -1.114694e+01
      vertex   1.124749e+01 -1.107542e+01 -1.075836e+01
    endloop
  endfacet
  facet normal 5.036941e-01 -7.437118e-01 -4.395281e-01
    outer loop
      vertex   1.097979e+01 -1.107542e+01 -1.106514e+01
      vertex   1.124749e+01 -1.107542e+01 -1.075836e+01
      vertex   1.117802e+01 -1.115203e+01 -1.070833e+01
    endloop
  endfacet
  facet normal 5.773065e-01 -7.436472e-01 -3.372033e-01
    outer loop
      vertex   1.117802e+01 -1.115203e+01 -1.070833e+01
      vertex   1.124749e+01 -1.107542e+01 -1.075836e+01
      vertex   1.137526e+01 -1.115203e+01 -1.037065e+01
    endloop
  endfacet
  facet normal 5.334743e-01 -7.863269e-01 -3.116010e-01
    outer loop
      vertex   1.117802e+01 -1.115203e+01 -1.070833e+01
      vertex   1.137526e+01 -1.115203e+01 -1.037065e+01
      vertex   1.133101e+01 -1.119019e+01 -1.035010e+01
    endloop
  endfacet
  facet normal 5.705342e-01 -7.873355e-01 -2.336526e-01
    outer loop
      vertex   1.133101e+01 -1.119019e+01 -1.035010e+01
      vertex   1.137526e+01 -1.115203e+01 -1.037065e+01
      vertex   1.140344e+01 -1.119019e+01 -1.017326e+01
    endloop
  endfacet
  facet normal 2.061090e-01 -4.760019e-01 -8.549511e-01
    outer loop
      vertex   9.968720e+00 -1.071951e+01 -1.194565e+01
      vertex   9.987751e+00 -1.070000e+01 -1.195193e+01
      vertex   1.019778e+01 -1.071951e+01 -1.189043e+01
    endloop
  endfacet
  facet normal 2.887170e-01 1.103256e-01 -9.510367e-01
    outer loop
      vertex   1.019778e+01 -1.071951e+01 -1.189043e+01
      vertex   9.987751e+00 -1.070000e+01 -1.195193e+01
      vertex   1.045669e+01 -1.070000e+01 -1.180957e+01
    endloop
  endfacet
  facet normal 3.020356e-01 -3.743336e-01 -8.767262e-01
    outer loop
      vertex   1.019778e+01 -1.071951e+01 -1.189043e+01
      vertex   1.045669e+01 -1.070000e+01 -1.180957e+01
      vertex   1.042062e+01 -1.071951e+01 -1.181366e+01
    endloop
  endfacet
  facet normal 3.589941e-01 -4.979499e-01 -7.894107e-01
    outer loop
      vertex   1.042062e+01 -1.071951e+01 -1.181366e+01
      vertex   1.045669e+01 -1.070000e+01 -1.180957e+01
      vertex   1.063512e+01 -1.071951e+01 -1.171611e+01
    endloop
  endfacet
  facet normal 3.262572e-01 -6.155154e-01 -7.174239e-01
    outer loop
      vertex   1.042062e+01 -1.071951e+01 -1.181366e+01
      vertex   1.063512e+01 -1.071951e+01 -1.171611e+01
      vertex   1.061773e+01 -1.076831e+01 -1.168215e+01
    endloop
  endfacet
  facet normal 3.922083e-01 -6.154985e-01 -6.836185e-01
    outer loop
      vertex   1.061773e+01 -1.076831e+01 -1.168215e+01
      vertex   1.063512e+01 -1.071951e+01 -1.171611e+01
      vertex   1.081899e+01 -1.076831e+01 -1.156669e+01
    endloop
  endfacet
  facet normal 3.754782e-01 -6.562781e-01 -6.544579e-01
    outer loop
      vertex   1.061773e+01 -1.076831e+01 -1.168215e+01
      vertex   1.081899e+01 -1.076831e+01 -1.156669e+01
      vertex   1.080106e+01 -1.080658e+01 -1.153860e+01
    endloop
  endfacet
  facet normal 4.644912e-01 -6.550400e-01 -5.959619e-01
    outer loop
      vertex   1.080106e+01 -1.080658e+01 -1.153860e+01
      vertex   1.081899e+01 -1.076831e+01 -1.156669e+01
      vertex   1.116169e+01 -1.080658e+01 -1.125754e+01
    endloop
  endfacet
  facet normal 4.546966e-01 -6.729794e-01 -5.833950e-01
    outer loop
      vertex   1.080106e+01 -1.080658e+01 -1.153860e+01
      vertex   1.116169e+01 -1.080658e+01 -1.125754e+01
      vertex   1.113194e+01 -1.085394e+01 -1.122608e+01
    endloop
  endfacet
  facet normal 5.573268e-01 -6.729572e-01 -4.863285e-01
    outer loop
      vertex   1.113194e+01 -1.085394e+01 -1.122608e+01
      vertex   1.116169e+01 -1.080658e+01 -1.125754e+01
      vertex   1.142717e+01 -1.085394e+01 -1.088775e+01
    endloop
  endfacet
  facet normal 5.473627e-01 -6.872119e-01 -4.776337e-01
    outer loop
      vertex   1.113194e+01 -1.085394e+01 -1.122608e+01
      vertex   1.142717e+01 -1.085394e+01 -1.088775e+01
      vertex   1.138515e+01 -1.090844e+01 -1.085749e+01
    endloop
  endfacet
  facet normal 6.273472e-01 -6.871413e-01 -3.664319e-01
    outer loop
      vertex   1.138515e+01 -1.090844e+01 -1.085749e+01
      vertex   1.142717e+01 -1.085394e+01 -1.088775e+01
      vertex   1.160674e+01 -1.090844e+01 -1.047812e+01
    endloop
  endfacet
  facet normal 6.170540e-01 -6.995298e-01 -3.604197e-01
    outer loop
      vertex   1.138515e+01 -1.090844e+01 -1.085749e+01
      vertex   1.160674e+01 -1.090844e+01 -1.047812e+01
      vertex   1.155495e+01 -1.096651e+01 -1.045408e+01
    endloop
  endfacet
  facet normal 6.602065e-01 -7.007311e-01 -2.703763e-01
    outer loop
      vertex   1.155495e+01 -1.096651e+01 -1.045408e+01
      vertex   1.160674e+01 -1.090844e+01 -1.047812e+01
      vertex   1.163624e+01 -1.096651e+01 -1.025560e+01
    endloop
  endfacet
  facet normal 6.439473e-01 -7.181816e-01 -2.637177e-01
    outer loop
      vertex   1.155495e+01 -1.096651e+01 -1.045408e+01
      vertex   1.163624e+01 -1.096651e+01 -1.025560e+01
      vertex   1.153014e+01 -1.107542e+01 -1.021808e+01
    endloop
  endfacet
  facet normal 6.658310e-01 -7.182359e-01 -2.020057e-01
    outer loop
      vertex   1.153014e+01 -1.107542e+01 -1.021808e+01
      vertex   1.163624e+01 -1.096651e+01 -1.025560e+01
      vertex   1.158929e+01 -1.107542e+01 -1.002310e+01
    endloop
  endfacet
  facet normal 6.385296e-01 -7.448164e-01 -1.937228e-01
    outer loop
      vertex   1.153014e+01 -1.107542e+01 -1.021808e+01
      vertex   1.158929e+01 -1.107542e+01 -1.002310e+01
      vertex   1.150623e+01 -1.115203e+01 -1.000230e+01
    endloop
  endfacet
  facet normal 4.697954e-01 9.028051e-02 -8.781467e-01
    outer loop
      vertex   1.045669e+01 -1.070000e+01 -1.180957e+01
      vertex   1.088879e+01 -1.070000e+01 -1.157840e+01
      vertex   1.063512e+01 -1.071951e+01 -1.171611e+01
    endloop
  endfacet
  facet normal 4.700467e-01 -3.283578e-01 -8.192907e-01
    outer loop
      vertex   1.063512e+01 -1.071951e+01 -1.171611e+01
      vertex   1.088879e+01 -1.070000e+01 -1.157840e+01
      vertex   1.083951e+01 -1.071951e+01 -1.159885e+01
    endloop
  endfacet
  facet normal 3.922083e-01 -6.154985e-01 -6.836185e-01
    outer loop
      vertex   1.063512e+01 -1.071951e+01 -1.171611e+01
      vertex   1.083951e+01 -1.071951e+01 -1.159885e+01
      vertex   1.081899e+01 -1.076831e+01 -1.156669e+01
    endloop
  endfacet
  facet normal 4.851041e-01 -6.142318e-01 -6.224092e-01
    outer loop
      vertex   1.081899e+01 -1.076831e+01 -1.156669e+01
      vertex   1.083951e+01 -1.071951e+01 -1.159885e+01
      vertex   1.118458e+01 -1.076831e+01 -1.128175e+01
    endloop
  endfacet
  facet normal 4.644912e-01 -6.550400e-01 -5.959619e-01
    outer loop
      vertex   1.081899e+01 -1.076831e+01 -1.156669e+01
      vertex   1.118458e+01 -1.076831e+01 -1.128175e+01
      vertex   1.116169e+01 -1.080658e+01 -1.125754e+01
    endloop
  endfacet
  facet normal 5.693314e-01 -6.550174e-01 -4.968038e-01
    outer loop
      vertex   1.116169e+01 -1.080658e+01 -1.125754e+01
      vertex   1.118458e+01 -1.076831e+01 -1.128175e+01
      vertex   1.146229e+01 -1.080658e+01 -1.091304e+01
    endloop
  endfacet
  facet normal 5.573268e-01 -6.729572e-01 -4.863285e-01
    outer loop
      vertex   1.116169e+01 -1.080658e+01 -1.125754e+01
      vertex   1.146229e+01 -1.080658e+01 -1.091304e+01
      vertex   1.142717e+01 -1.085394e+01 -1.088775e+01
    endloop
  endfacet
  facet normal 6.387649e-01 -6.728856e-01 -3.731010e-01
    outer loop
      vertex   1.142717e+01 -1.085394e+01 -1.088775e+01
      vertex   1.146229e+01 -1.080658e+01 -1.091304e+01
      vertex   1.165370e+01 -1.085394e+01 -1.049992e+01
    endloop
  endfacet
  facet normal 6.273472e-01 -6.871413e-01 -3.664319e-01
    outer loop
      vertex   1.142717e+01 -1.085394e+01 -1.088775e+01
      vertex   1.165370e+01 -1.085394e+01 -1.049992e+01
      vertex   1.160674e+01 -1.090844e+01 -1.047812e+01
    endloop
  endfacet
  facet normal 6.712582e-01 -6.883611e-01 -2.749024e-01
    outer loop
      vertex   1.160674e+01 -1.090844e+01 -1.047812e+01
      vertex   1.165370e+01 -1.085394e+01 -1.049992e+01
      vertex   1.169007e+01 -1.090844e+01 -1.027464e+01
    endloop
  endfacet
  facet normal 6.602065e-01 -7.007311e-01 -2.703763e-01
    outer loop
      vertex   1.160674e+01 -1.090844e+01 -1.047812e+01
      vertex   1.169007e+01 -1.090844e+01 -1.027464e+01
      vertex   1.163624e+01 -1.096651e+01 -1.025560e+01
    endloop
  endfacet
  facet normal 6.826453e-01 -7.007867e-01 -2.071070e-01
    outer loop
      vertex   1.163624e+01 -1.096651e+01 -1.025560e+01
      vertex   1.169007e+01 -1.090844e+01 -1.027464e+01
      vertex   1.169848e+01 -1.096651e+01 -1.005044e+01
    endloop
  endfacet
  facet normal 6.658310e-01 -7.182359e-01 -2.020057e-01
    outer loop
      vertex   1.163624e+01 -1.096651e+01 -1.025560e+01
      vertex   1.169848e+01 -1.096651e+01 -1.005044e+01
      vertex   1.158929e+01 -1.107542e+01 -1.002310e+01
    endloop
  endfacet
  facet normal 4.975203e-01 -5.873635e-01 -6.383397e-01
    outer loop
      vertex   1.083951e+01 -1.071951e+01 -1.159885e+01
      vertex   1.088879e+01 -1.070000e+01 -1.157840e+01
      vertex   1.121079e+01 -1.071951e+01 -1.130948e+01
    endloop
  endfacet
  facet normal 6.218877e-01 -1.939507e-01 -7.587087e-01
    outer loop
      vertex   1.121079e+01 -1.071951e+01 -1.130948e+01
      vertex   1.088879e+01 -1.070000e+01 -1.157840e+01
      vertex   1.126777e+01 -1.070000e+01 -1.126777e+01
    endloop
  endfacet
  facet normal 5.899391e-01 -6.220667e-01 -5.147863e-01
    outer loop
      vertex   1.121079e+01 -1.071951e+01 -1.130948e+01
      vertex   1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   1.152029e+01 -1.071951e+01 -1.095480e+01
    endloop
  endfacet
  facet normal 7.666342e-01 -1.376630e-01 -6.271531e-01
    outer loop
      vertex   1.152029e+01 -1.071951e+01 -1.095480e+01
      vertex   1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   1.157804e+01 -1.070000e+01 -1.088849e+01
    endloop
  endfacet
  facet normal 6.606663e-01 -6.438992e-01 -3.858935e-01
    outer loop
      vertex   1.152029e+01 -1.071951e+01 -1.095480e+01
      vertex   1.157804e+01 -1.070000e+01 -1.088849e+01
      vertex   1.175776e+01 -1.071951e+01 -1.054824e+01
    endloop
  endfacet
  facet normal 8.782445e-01 -9.243396e-02 -4.691936e-01
    outer loop
      vertex   1.175776e+01 -1.071951e+01 -1.054824e+01
      vertex   1.157804e+01 -1.070000e+01 -1.088849e+01
      vertex   1.180899e+01 -1.070000e+01 -1.045619e+01
    endloop
  endfacet
  facet normal 7.788045e-01 -5.401268e-01 -3.189461e-01
    outer loop
      vertex   1.175776e+01 -1.071951e+01 -1.054824e+01
      vertex   1.180899e+01 -1.070000e+01 -1.045619e+01
      vertex   1.184706e+01 -1.071951e+01 -1.033017e+01
    endloop
  endfacet
  facet normal 9.563094e-01 -1.836045e-02 -2.917795e-01
    outer loop
      vertex   1.184706e+01 -1.071951e+01 -1.033017e+01
      vertex   1.180899e+01 -1.070000e+01 -1.045619e+01
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
    endloop
  endfacet
  facet normal 9.558611e-01 -4.723248e-02 -2.899976e-01
    outer loop
      vertex   1.184706e+01 -1.071951e+01 -1.033017e+01
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
      vertex   1.191545e+01 -1.071951e+01 -1.010476e+01
    endloop
  endfacet
  facet normal 6.131100e-01 -7.874322e-01 -6.361374e-02
    outer loop
      vertex   1.151634e+01 -1.119019e+01 -9.613184e+00
      vertex   1.154487e+01 -1.115203e+01 -9.810530e+00
      vertex   1.156506e+01 -1.115203e+01 -9.615919e+00
    endloop
  endfacet
  facet normal 6.636451e-01 -7.448717e-01 -6.885705e-02
    outer loop
      vertex   1.156506e+01 -1.115203e+01 -9.615919e+00
      vertex   1.154487e+01 -1.115203e+01 -9.810530e+00
      vertex   1.162953e+01 -1.107542e+01 -9.823386e+00
    endloop
  endfacet
  facet normal 6.636451e-01 -7.448717e-01 -6.885705e-02
    outer loop
      vertex   1.156506e+01 -1.115203e+01 -9.615919e+00
      vertex   1.162953e+01 -1.107542e+01 -9.823386e+00
      vertex   1.165056e+01 -1.107542e+01 -9.620718e+00
    endloop
  endfacet
  facet normal 6.920248e-01 -7.182940e-01 -7.180161e-02
    outer loop
      vertex   1.165056e+01 -1.107542e+01 -9.620718e+00
      vertex   1.162953e+01 -1.107542e+01 -9.823386e+00
      vertex   1.174082e+01 -1.096651e+01 -9.840287e+00
    endloop
  endfacet
  facet normal 6.920248e-01 -7.182940e-01 -7.180161e-02
    outer loop
      vertex   1.165056e+01 -1.107542e+01 -9.620718e+00
      vertex   1.174082e+01 -1.096651e+01 -9.840287e+00
      vertex   1.176295e+01 -1.096651e+01 -9.627027e+00
    endloop
  endfacet
  facet normal 7.095035e-01 -7.008463e-01 -7.361514e-02
    outer loop
      vertex   1.176295e+01 -1.096651e+01 -9.627027e+00
      vertex   1.174082e+01 -1.096651e+01 -9.840287e+00
      vertex   1.179729e+01 -1.090844e+01 -9.848862e+00
    endloop
  endfacet
  facet normal 7.095035e-01 -7.008463e-01 -7.361514e-02
    outer loop
      vertex   1.176295e+01 -1.096651e+01 -9.627027e+00
      vertex   1.179729e+01 -1.090844e+01 -9.848862e+00
      vertex   1.181997e+01 -1.090844e+01 -9.630228e+00
    endloop
  endfacet
  facet normal 7.213845e-01 -6.884781e-01 -7.484786e-02
    outer loop
      vertex   1.181997e+01 -1.090844e+01 -9.630228e+00
      vertex   1.179729e+01 -1.090844e+01 -9.848862e+00
      vertex   1.184849e+01 -1.085394e+01 -9.856638e+00
    endloop
  endfacet
  facet normal 7.213845e-01 -6.884781e-01 -7.484786e-02
    outer loop
      vertex   1.181997e+01 -1.090844e+01 -9.630228e+00
      vertex   1.184849e+01 -1.085394e+01 -9.856638e+00
      vertex   1.187168e+01 -1.085394e+01 -9.633131e+00
    endloop
  endfacet
  facet normal 7.345663e-01 -6.742429e-01 -7.621555e-02
    outer loop
      vertex   1.187168e+01 -1.085394e+01 -9.633131e+00
      vertex   1.184849e+01 -1.085394e+01 -9.856638e+00
      vertex   1.189130e+01 -1.080658e+01 -9.863138e+00
    endloop
  endfacet
  facet normal 7.838937e-01 -6.155449e-01 -8.133355e-02
    outer loop
      vertex   1.196197e+01 -1.071951e+01 -9.873870e+00
      vertex   1.194818e+01 -1.076831e+01 -9.637424e+00
      vertex   1.192424e+01 -1.076831e+01 -9.868141e+00
    endloop
  endfacet
  facet normal 7.504510e-01 -6.563235e-01 -7.786368e-02
    outer loop
      vertex   1.192424e+01 -1.076831e+01 -9.868141e+00
      vertex   1.194818e+01 -1.076831e+01 -9.637424e+00
      vertex   1.191491e+01 -1.080658e+01 -9.635557e+00
    endloop
  endfacet
  facet normal 5.899135e-01 -7.873822e-01 -1.789732e-01
    outer loop
      vertex   1.150623e+01 -1.115203e+01 -1.000230e+01
      vertex   1.145890e+01 -1.119019e+01 -9.990452e+00
      vertex   1.144943e+01 -1.115203e+01 -1.018953e+01
    endloop
  endfacet
  facet normal 5.899135e-01 -7.873822e-01 -1.789732e-01
    outer loop
      vertex   1.144943e+01 -1.115203e+01 -1.018953e+01
      vertex   1.145890e+01 -1.119019e+01 -9.990452e+00
      vertex   1.140344e+01 -1.119019e+01 -1.017326e+01
    endloop
  endfacet
  facet normal 5.705342e-01 -7.873355e-01 -2.336526e-01
    outer loop
      vertex   1.144943e+01 -1.115203e+01 -1.018953e+01
      vertex   1.140344e+01 -1.119019e+01 -1.017326e+01
      vertex   1.137526e+01 -1.115203e+01 -1.037065e+01
    endloop
  endfacet
  facet normal 6.826453e-01 -7.007867e-01 -2.071070e-01
    outer loop
      vertex   1.169848e+01 -1.096651e+01 -1.005044e+01
      vertex   1.169007e+01 -1.090844e+01 -1.027464e+01
      vertex   1.175388e+01 -1.090844e+01 -1.006431e+01
    endloop
  endfacet
  facet normal 6.940746e-01 -6.884176e-01 -2.105745e-01
    outer loop
      vertex   1.175388e+01 -1.090844e+01 -1.006431e+01
      vertex   1.169007e+01 -1.090844e+01 -1.027464e+01
      vertex   1.173889e+01 -1.085394e+01 -1.029191e+01
    endloop
  endfacet
  facet normal 6.940746e-01 -6.884176e-01 -2.105745e-01
    outer loop
      vertex   1.175388e+01 -1.090844e+01 -1.006431e+01
      vertex   1.173889e+01 -1.085394e+01 -1.029191e+01
      vertex   1.180412e+01 -1.085394e+01 -1.007689e+01
    endloop
  endfacet
  facet normal 7.067551e-01 -6.741815e-01 -2.144216e-01
    outer loop
      vertex   1.180412e+01 -1.085394e+01 -1.007689e+01
      vertex   1.173889e+01 -1.085394e+01 -1.029191e+01
      vertex   1.177969e+01 -1.080658e+01 -1.030634e+01
    endloop
  endfacet
  facet normal 7.067551e-01 -6.741815e-01 -2.144216e-01
    outer loop
      vertex   1.180412e+01 -1.085394e+01 -1.007689e+01
      vertex   1.177969e+01 -1.080658e+01 -1.030634e+01
      vertex   1.184612e+01 -1.080658e+01 -1.008740e+01
    endloop
  endfacet
  facet normal 7.220355e-01 -6.562611e-01 -2.190575e-01
    outer loop
      vertex   1.184612e+01 -1.080658e+01 -1.008740e+01
      vertex   1.177969e+01 -1.080658e+01 -1.030634e+01
      vertex   1.181110e+01 -1.076831e+01 -1.031745e+01
    endloop
  endfacet
  facet normal 7.220355e-01 -6.562611e-01 -2.190575e-01
    outer loop
      vertex   1.184612e+01 -1.080658e+01 -1.008740e+01
      vertex   1.181110e+01 -1.076831e+01 -1.031745e+01
      vertex   1.187844e+01 -1.076831e+01 -1.009549e+01
    endloop
  endfacet
  facet normal 7.542053e-01 -6.154811e-01 -2.288175e-01
    outer loop
      vertex   1.187844e+01 -1.076831e+01 -1.009549e+01
      vertex   1.181110e+01 -1.076831e+01 -1.031745e+01
      vertex   1.184706e+01 -1.071951e+01 -1.033017e+01
    endloop
  endfacet
  facet normal 7.542053e-01 -6.154811e-01 -2.288175e-01
    outer loop
      vertex   1.187844e+01 -1.076831e+01 -1.009549e+01
      vertex   1.184706e+01 -1.071951e+01 -1.033017e+01
      vertex   1.191545e+01 -1.071951e+01 -1.010476e+01
    endloop
  endfacet
  facet normal 6.175470e-01 -7.447646e-01 -2.529059e-01
    outer loop
      vertex   1.137526e+01 -1.115203e+01 -1.037065e+01
      vertex   1.145290e+01 -1.107542e+01 -1.040669e+01
      vertex   1.144943e+01 -1.115203e+01 -1.018953e+01
    endloop
  endfacet
  facet normal 6.175470e-01 -7.447646e-01 -2.529059e-01
    outer loop
      vertex   1.144943e+01 -1.115203e+01 -1.018953e+01
      vertex   1.145290e+01 -1.107542e+01 -1.040669e+01
      vertex   1.153014e+01 -1.107542e+01 -1.021808e+01
    endloop
  endfacet
  facet normal 6.385296e-01 -7.448164e-01 -1.937228e-01
    outer loop
      vertex   1.144943e+01 -1.115203e+01 -1.018953e+01
      vertex   1.153014e+01 -1.107542e+01 -1.021808e+01
      vertex   1.150623e+01 -1.115203e+01 -1.000230e+01
    endloop
  endfacet
  facet normal 6.439473e-01 -7.181816e-01 -2.637177e-01
    outer loop
      vertex   1.153014e+01 -1.107542e+01 -1.021808e+01
      vertex   1.145290e+01 -1.107542e+01 -1.040669e+01
      vertex   1.155495e+01 -1.096651e+01 -1.045408e+01
    endloop
  endfacet
  facet normal 6.019078e-01 -7.170102e-01 -3.515728e-01
    outer loop
      vertex   1.155495e+01 -1.096651e+01 -1.045408e+01
      vertex   1.145290e+01 -1.107542e+01 -1.040669e+01
      vertex   1.133881e+01 -1.096651e+01 -1.082412e+01
    endloop
  endfacet
  facet normal 6.170540e-01 -6.995298e-01 -3.604197e-01
    outer loop
      vertex   1.155495e+01 -1.096651e+01 -1.045408e+01
      vertex   1.133881e+01 -1.096651e+01 -1.082412e+01
      vertex   1.138515e+01 -1.090844e+01 -1.085749e+01
    endloop
  endfacet
  facet normal 5.383801e-01 -6.995993e-01 -4.697954e-01
    outer loop
      vertex   1.138515e+01 -1.090844e+01 -1.085749e+01
      vertex   1.133881e+01 -1.096651e+01 -1.082412e+01
      vertex   1.109636e+01 -1.090844e+01 -1.118844e+01
    endloop
  endfacet
  facet normal 5.473627e-01 -6.872119e-01 -4.776337e-01
    outer loop
      vertex   1.138515e+01 -1.090844e+01 -1.085749e+01
      vertex   1.109636e+01 -1.090844e+01 -1.118844e+01
      vertex   1.113194e+01 -1.085394e+01 -1.122608e+01
    endloop
  endfacet
  facet normal 4.465668e-01 -6.872337e-01 -5.729641e-01
    outer loop
      vertex   1.113194e+01 -1.085394e+01 -1.122608e+01
      vertex   1.109636e+01 -1.090844e+01 -1.118844e+01
      vertex   1.077778e+01 -1.085394e+01 -1.150211e+01
    endloop
  endfacet
  facet normal 4.546966e-01 -6.729794e-01 -5.833950e-01
    outer loop
      vertex   1.113194e+01 -1.085394e+01 -1.122608e+01
      vertex   1.077778e+01 -1.085394e+01 -1.150211e+01
      vertex   1.080106e+01 -1.080658e+01 -1.153860e+01
    endloop
  endfacet
  facet normal 3.675316e-01 -6.741982e-01 -6.406070e-01
    outer loop
      vertex   1.080106e+01 -1.080658e+01 -1.153860e+01
      vertex   1.077778e+01 -1.085394e+01 -1.150211e+01
      vertex   1.060254e+01 -1.080658e+01 -1.165250e+01
    endloop
  endfacet
  facet normal 3.754782e-01 -6.562781e-01 -6.544579e-01
    outer loop
      vertex   1.080106e+01 -1.080658e+01 -1.153860e+01
      vertex   1.060254e+01 -1.080658e+01 -1.165250e+01
      vertex   1.061773e+01 -1.076831e+01 -1.168215e+01
    endloop
  endfacet
  facet normal 3.123396e-01 -6.562946e-01 -6.868197e-01
    outer loop
      vertex   1.061773e+01 -1.076831e+01 -1.168215e+01
      vertex   1.060254e+01 -1.080658e+01 -1.165250e+01
      vertex   1.040651e+01 -1.076831e+01 -1.177821e+01
    endloop
  endfacet
  facet normal 3.262572e-01 -6.155154e-01 -7.174239e-01
    outer loop
      vertex   1.061773e+01 -1.076831e+01 -1.168215e+01
      vertex   1.040651e+01 -1.076831e+01 -1.177821e+01
      vertex   1.042062e+01 -1.071951e+01 -1.181366e+01
    endloop
  endfacet
  facet normal 2.567003e-01 -6.155369e-01 -7.451304e-01
    outer loop
      vertex   1.042062e+01 -1.071951e+01 -1.181366e+01
      vertex   1.040651e+01 -1.076831e+01 -1.177821e+01
      vertex   1.019778e+01 -1.071951e+01 -1.189043e+01
    endloop
  endfacet
  facet normal 6.019078e-01 -7.170102e-01 -3.515728e-01
    outer loop
      vertex   1.133881e+01 -1.096651e+01 -1.082412e+01
      vertex   1.145290e+01 -1.107542e+01 -1.040669e+01
      vertex   1.124749e+01 -1.107542e+01 -1.075836e+01
    endloop
  endfacet
  facet normal 5.773065e-01 -7.436472e-01 -3.372033e-01
    outer loop
      vertex   1.124749e+01 -1.107542e+01 -1.075836e+01
      vertex   1.145290e+01 -1.107542e+01 -1.040669e+01
      vertex   1.137526e+01 -1.115203e+01 -1.037065e+01
    endloop
  endfacet
  facet normal 6.712582e-01 -6.883611e-01 -2.749024e-01
    outer loop
      vertex   1.173889e+01 -1.085394e+01 -1.029191e+01
      vertex   1.169007e+01 -1.090844e+01 -1.027464e+01
      vertex   1.165370e+01 -1.085394e+01 -1.049992e+01
    endloop
  endfacet
  facet normal 6.835198e-01 -6.741241e-01 -2.799239e-01
    outer loop
      vertex   1.177969e+01 -1.080658e+01 -1.030634e+01
      vertex   1.173889e+01 -1.085394e+01 -1.029191e+01
      vertex   1.169295e+01 -1.080658e+01 -1.051815e+01
    endloop
  endfacet
  facet normal 6.835198e-01 -6.741241e-01 -2.799239e-01
    outer loop
      vertex   1.169295e+01 -1.080658e+01 -1.051815e+01
      vertex   1.173889e+01 -1.085394e+01 -1.029191e+01
      vertex   1.165370e+01 -1.085394e+01 -1.049992e+01
    endloop
  endfacet
  facet normal 6.387649e-01 -6.728856e-01 -3.731010e-01
    outer loop
      vertex   1.169295e+01 -1.080658e+01 -1.051815e+01
      vertex   1.165370e+01 -1.085394e+01 -1.049992e+01
      vertex   1.146229e+01 -1.080658e+01 -1.091304e+01
    endloop
  endfacet
  facet normal 6.982952e-01 -6.562028e-01 -2.859749e-01
    outer loop
      vertex   1.181110e+01 -1.076831e+01 -1.031745e+01
      vertex   1.177969e+01 -1.080658e+01 -1.030634e+01
      vertex   1.172316e+01 -1.076831e+01 -1.053217e+01
    endloop
  endfacet
  facet normal 6.982952e-01 -6.562028e-01 -2.859749e-01
    outer loop
      vertex   1.172316e+01 -1.076831e+01 -1.053217e+01
      vertex   1.177969e+01 -1.080658e+01 -1.030634e+01
      vertex   1.169295e+01 -1.080658e+01 -1.051815e+01
    endloop
  endfacet
  facet normal 6.525206e-01 -6.549447e-01 -3.811356e-01
    outer loop
      vertex   1.172316e+01 -1.076831e+01 -1.053217e+01
      vertex   1.169295e+01 -1.080658e+01 -1.051815e+01
      vertex   1.148933e+01 -1.076831e+01 -1.093251e+01
    endloop
  endfacet
  facet normal 6.525206e-01 -6.549447e-01 -3.811356e-01
    outer loop
      vertex   1.148933e+01 -1.076831e+01 -1.093251e+01
      vertex   1.169295e+01 -1.080658e+01 -1.051815e+01
      vertex   1.146229e+01 -1.080658e+01 -1.091304e+01
    endloop
  endfacet
  facet normal 5.693314e-01 -6.550174e-01 -4.968038e-01
    outer loop
      vertex   1.148933e+01 -1.076831e+01 -1.093251e+01
      vertex   1.146229e+01 -1.080658e+01 -1.091304e+01
      vertex   1.118458e+01 -1.076831e+01 -1.128175e+01
    endloop
  endfacet
  facet normal 7.294014e-01 -6.154214e-01 -2.987139e-01
    outer loop
      vertex   1.184706e+01 -1.071951e+01 -1.033017e+01
      vertex   1.181110e+01 -1.076831e+01 -1.031745e+01
      vertex   1.175776e+01 -1.071951e+01 -1.054824e+01
    endloop
  endfacet
  facet normal 7.294014e-01 -6.154214e-01 -2.987139e-01
    outer loop
      vertex   1.175776e+01 -1.071951e+01 -1.054824e+01
      vertex   1.181110e+01 -1.076831e+01 -1.031745e+01
      vertex   1.172316e+01 -1.076831e+01 -1.053217e+01
    endloop
  endfacet
  facet normal 6.814688e-01 -6.141344e-01 -3.980442e-01
    outer loop
      vertex   1.175776e+01 -1.071951e+01 -1.054824e+01
      vertex   1.172316e+01 -1.076831e+01 -1.053217e+01
      vertex   1.152029e+01 -1.071951e+01 -1.095480e+01
    endloop
  endfacet
  facet normal 6.814688e-01 -6.141344e-01 -3.980442e-01
    outer loop
      vertex   1.152029e+01 -1.071951e+01 -1.095480e+01
      vertex   1.172316e+01 -1.076831e+01 -1.053217e+01
      vertex   1.148933e+01 -1.076831e+01 -1.093251e+01
    endloop
  endfacet
  facet normal 5.945950e-01 -6.142088e-01 -5.188491e-01
    outer loop
      vertex   1.152029e+01 -1.071951e+01 -1.095480e+01
      vertex   1.148933e+01 -1.076831e+01 -1.093251e+01
      vertex   1.121079e+01 -1.071951e+01 -1.130948e+01
    endloop
  endfacet
  facet normal 5.945950e-01 -6.142088e-01 -5.188491e-01
    outer loop
      vertex   1.121079e+01 -1.071951e+01 -1.130948e+01
      vertex   1.148933e+01 -1.076831e+01 -1.093251e+01
      vertex   1.118458e+01 -1.076831e+01 -1.128175e+01
    endloop
  endfacet
  facet normal 4.851041e-01 -6.142318e-01 -6.224092e-01
    outer loop
      vertex   1.121079e+01 -1.071951e+01 -1.130948e+01
      vertex   1.118458e+01 -1.076831e+01 -1.128175e+01
      vertex   1.083951e+01 -1.071951e+01 -1.159885e+01
    endloop
  endfacet
  facet normal 5.334743e-01 -7.863269e-01 -3.116010e-01
    outer loop
      vertex   1.133101e+01 -1.119019e+01 -1.035010e+01
      vertex   1.113842e+01 -1.119019e+01 -1.067982e+01
      vertex   1.117802e+01 -1.115203e+01 -1.070833e+01
    endloop
  endfacet
  facet normal 4.654451e-01 -7.863852e-01 -4.061516e-01
    outer loop
      vertex   1.117802e+01 -1.115203e+01 -1.070833e+01
      vertex   1.113842e+01 -1.119019e+01 -1.067982e+01
      vertex   1.092096e+01 -1.115203e+01 -1.100292e+01
    endloop
  endfacet
  facet normal 5.036941e-01 -7.437118e-01 -4.395281e-01
    outer loop
      vertex   1.117802e+01 -1.115203e+01 -1.070833e+01
      vertex   1.092096e+01 -1.115203e+01 -1.100292e+01
      vertex   1.097979e+01 -1.107542e+01 -1.106514e+01
    endloop
  endfacet
  facet normal 4.109377e-01 -7.437318e-01 -5.272505e-01
    outer loop
      vertex   1.097979e+01 -1.107542e+01 -1.106514e+01
      vertex   1.092096e+01 -1.115203e+01 -1.100292e+01
      vertex   1.065864e+01 -1.107542e+01 -1.131544e+01
    endloop
  endfacet
  facet normal 4.284536e-01 -7.170990e-01 -5.497241e-01
    outer loop
      vertex   1.097979e+01 -1.107542e+01 -1.106514e+01
      vertex   1.065864e+01 -1.107542e+01 -1.131544e+01
      vertex   1.071919e+01 -1.096651e+01 -1.141032e+01
    endloop
  endfacet
  facet normal 3.462490e-01 -7.182517e-01 -6.035115e-01
    outer loop
      vertex   1.071919e+01 -1.096651e+01 -1.141032e+01
      vertex   1.065864e+01 -1.107542e+01 -1.131544e+01
      vertex   1.053316e+01 -1.096651e+01 -1.151705e+01
    endloop
  endfacet
  facet normal 3.549933e-01 -7.008030e-01 -6.187527e-01
    outer loop
      vertex   1.071919e+01 -1.096651e+01 -1.141032e+01
      vertex   1.053316e+01 -1.096651e+01 -1.151705e+01
      vertex   1.055920e+01 -1.090844e+01 -1.156788e+01
    endloop
  endfacet
  facet normal 2.952986e-01 -7.008187e-01 -6.493472e-01
    outer loop
      vertex   1.055920e+01 -1.090844e+01 -1.156788e+01
      vertex   1.053316e+01 -1.096651e+01 -1.151705e+01
      vertex   1.035904e+01 -1.090844e+01 -1.165890e+01
    endloop
  endfacet
  facet normal 3.002431e-01 -6.884501e-01 -6.602200e-01
    outer loop
      vertex   1.055920e+01 -1.090844e+01 -1.156788e+01
      vertex   1.035904e+01 -1.090844e+01 -1.165890e+01
      vertex   1.037818e+01 -1.085394e+01 -1.170703e+01
    endloop
  endfacet
  facet normal 2.362310e-01 -6.884705e-01 -6.857137e-01
    outer loop
      vertex   1.037818e+01 -1.085394e+01 -1.170703e+01
      vertex   1.035904e+01 -1.090844e+01 -1.165890e+01
      vertex   1.016562e+01 -1.085394e+01 -1.178026e+01
    endloop
  endfacet
  facet normal 2.405476e-01 -6.742351e-01 -6.982434e-01
    outer loop
      vertex   1.037818e+01 -1.085394e+01 -1.170703e+01
      vertex   1.016562e+01 -1.085394e+01 -1.178026e+01
      vertex   1.017775e+01 -1.080658e+01 -1.182181e+01
    endloop
  endfacet
  facet normal 1.730797e-01 -6.742405e-01 -7.179437e-01
    outer loop
      vertex   1.017775e+01 -1.080658e+01 -1.182181e+01
      vertex   1.016562e+01 -1.085394e+01 -1.178026e+01
      vertex   9.955265e+00 -1.080658e+01 -1.187545e+01
    endloop
  endfacet
  facet normal 1.768224e-01 -6.563210e-01 -7.334689e-01
    outer loop
      vertex   1.017775e+01 -1.080658e+01 -1.182181e+01
      vertex   9.955265e+00 -1.080658e+01 -1.187545e+01
      vertex   9.961537e+00 -1.076831e+01 -1.190818e+01
    endloop
  endfacet
  facet normal 1.068153e-01 -6.563192e-01 -7.468839e-01
    outer loop
      vertex   9.961537e+00 -1.076831e+01 -1.190818e+01
      vertex   9.955265e+00 -1.080658e+01 -1.187545e+01
      vertex   9.731880e+00 -1.076831e+01 -1.194102e+01
    endloop
  endfacet
  facet normal 1.115753e-01 -6.155406e-01 -7.801671e-01
    outer loop
      vertex   9.961537e+00 -1.076831e+01 -1.190818e+01
      vertex   9.731880e+00 -1.076831e+01 -1.194102e+01
      vertex   9.735488e+00 -1.071951e+01 -1.197901e+01
    endloop
  endfacet
  facet normal 5.383801e-01 -6.995993e-01 -4.697954e-01
    outer loop
      vertex   1.109636e+01 -1.090844e+01 -1.118844e+01
      vertex   1.133881e+01 -1.096651e+01 -1.082412e+01
      vertex   1.105712e+01 -1.096651e+01 -1.114694e+01
    endloop
  endfacet
  facet normal 5.251624e-01 -7.170780e-01 -4.582615e-01
    outer loop
      vertex   1.105712e+01 -1.096651e+01 -1.114694e+01
      vertex   1.133881e+01 -1.096651e+01 -1.082412e+01
      vertex   1.124749e+01 -1.107542e+01 -1.075836e+01
    endloop
  endfacet
  facet normal 4.654451e-01 -7.863852e-01 -4.061516e-01
    outer loop
      vertex   1.113842e+01 -1.119019e+01 -1.067982e+01
      vertex   1.088743e+01 -1.119019e+01 -1.096746e+01
      vertex   1.092096e+01 -1.115203e+01 -1.100292e+01
    endloop
  endfacet
  facet normal 3.797308e-01 -7.864033e-01 -4.872108e-01
    outer loop
      vertex   1.092096e+01 -1.115203e+01 -1.100292e+01
      vertex   1.088743e+01 -1.119019e+01 -1.096746e+01
      vertex   1.061258e+01 -1.115203e+01 -1.124327e+01
    endloop
  endfacet
  facet normal 4.109377e-01 -7.437318e-01 -5.272505e-01
    outer loop
      vertex   1.092096e+01 -1.115203e+01 -1.100292e+01
      vertex   1.061258e+01 -1.115203e+01 -1.124327e+01
      vertex   1.065864e+01 -1.107542e+01 -1.131544e+01
    endloop
  endfacet
  facet normal 3.320510e-01 -7.448315e-01 -5.787644e-01
    outer loop
      vertex   1.065864e+01 -1.107542e+01 -1.131544e+01
      vertex   1.061258e+01 -1.115203e+01 -1.124327e+01
      vertex   1.048185e+01 -1.107542e+01 -1.141687e+01
    endloop
  endfacet
  facet normal 3.462490e-01 -7.182517e-01 -6.035115e-01
    outer loop
      vertex   1.065864e+01 -1.107542e+01 -1.131544e+01
      vertex   1.048185e+01 -1.107542e+01 -1.141687e+01
      vertex   1.053316e+01 -1.096651e+01 -1.151705e+01
    endloop
  endfacet
  facet normal 2.880244e-01 -7.182671e-01 -6.333517e-01
    outer loop
      vertex   1.053316e+01 -1.096651e+01 -1.151705e+01
      vertex   1.048185e+01 -1.107542e+01 -1.141687e+01
      vertex   1.033792e+01 -1.096651e+01 -1.160584e+01
    endloop
  endfacet
  facet normal 2.952986e-01 -7.008187e-01 -6.493472e-01
    outer loop
      vertex   1.053316e+01 -1.096651e+01 -1.151705e+01
      vertex   1.033792e+01 -1.096651e+01 -1.160584e+01
      vertex   1.035904e+01 -1.090844e+01 -1.165890e+01
    endloop
  endfacet
  facet normal 2.323405e-01 -7.008388e-01 -6.744204e-01
    outer loop
      vertex   1.035904e+01 -1.090844e+01 -1.165890e+01
      vertex   1.033792e+01 -1.096651e+01 -1.160584e+01
      vertex   1.015111e+01 -1.090844e+01 -1.173054e+01
    endloop
  endfacet
  facet normal 2.362310e-01 -6.884705e-01 -6.857137e-01
    outer loop
      vertex   1.035904e+01 -1.090844e+01 -1.165890e+01
      vertex   1.015111e+01 -1.090844e+01 -1.173054e+01
      vertex   1.016562e+01 -1.085394e+01 -1.178026e+01
    endloop
  endfacet
  facet normal 1.699738e-01 -6.884757e-01 -7.050603e-01
    outer loop
      vertex   1.016562e+01 -1.085394e+01 -1.178026e+01
      vertex   1.015111e+01 -1.090844e+01 -1.173054e+01
      vertex   9.947116e+00 -1.085394e+01 -1.183293e+01
    endloop
  endfacet
  facet normal 1.730797e-01 -6.742405e-01 -7.179437e-01
    outer loop
      vertex   1.016562e+01 -1.085394e+01 -1.178026e+01
      vertex   9.947116e+00 -1.085394e+01 -1.183293e+01
      vertex   9.955265e+00 -1.080658e+01 -1.187545e+01
    endloop
  endfacet
  facet normal 1.045544e-01 -6.742387e-01 -7.310749e-01
    outer loop
      vertex   9.955265e+00 -1.080658e+01 -1.187545e+01
      vertex   9.947116e+00 -1.085394e+01 -1.183293e+01
      vertex   9.728729e+00 -1.080658e+01 -1.190785e+01
    endloop
  endfacet
  facet normal 1.068153e-01 -6.563192e-01 -7.468839e-01
    outer loop
      vertex   9.955265e+00 -1.080658e+01 -1.187545e+01
      vertex   9.728729e+00 -1.080658e+01 -1.190785e+01
      vertex   9.731880e+00 -1.076831e+01 -1.194102e+01
    endloop
  endfacet
  facet normal 4.465668e-01 -6.872337e-01 -5.729641e-01
    outer loop
      vertex   1.077778e+01 -1.085394e+01 -1.150211e+01
      vertex   1.109636e+01 -1.090844e+01 -1.118844e+01
      vertex   1.074991e+01 -1.090844e+01 -1.145846e+01
    endloop
  endfacet
  facet normal 4.392378e-01 -6.996208e-01 -5.635608e-01
    outer loop
      vertex   1.074991e+01 -1.090844e+01 -1.145846e+01
      vertex   1.109636e+01 -1.090844e+01 -1.118844e+01
      vertex   1.105712e+01 -1.096651e+01 -1.114694e+01
    endloop
  endfacet
  facet normal 3.797308e-01 -7.864033e-01 -4.872108e-01
    outer loop
      vertex   1.088743e+01 -1.119019e+01 -1.096746e+01
      vertex   1.058633e+01 -1.119019e+01 -1.120214e+01
      vertex   1.061258e+01 -1.115203e+01 -1.124327e+01
    endloop
  endfacet
  facet normal 3.067685e-01 -7.873958e-01 -5.346970e-01
    outer loop
      vertex   1.061258e+01 -1.115203e+01 -1.124327e+01
      vertex   1.058633e+01 -1.119019e+01 -1.120214e+01
      vertex   1.044282e+01 -1.115203e+01 -1.134067e+01
    endloop
  endfacet
  facet normal 3.320510e-01 -7.448315e-01 -5.787644e-01
    outer loop
      vertex   1.061258e+01 -1.115203e+01 -1.124327e+01
      vertex   1.044282e+01 -1.115203e+01 -1.134067e+01
      vertex   1.048185e+01 -1.107542e+01 -1.141687e+01
    endloop
  endfacet
  facet normal 2.762134e-01 -7.448461e-01 -6.073799e-01
    outer loop
      vertex   1.048185e+01 -1.107542e+01 -1.141687e+01
      vertex   1.044282e+01 -1.115203e+01 -1.134067e+01
      vertex   1.029631e+01 -1.107542e+01 -1.150125e+01
    endloop
  endfacet
  facet normal 2.880244e-01 -7.182671e-01 -6.333517e-01
    outer loop
      vertex   1.048185e+01 -1.107542e+01 -1.141687e+01
      vertex   1.029631e+01 -1.107542e+01 -1.150125e+01
      vertex   1.033792e+01 -1.096651e+01 -1.160584e+01
    endloop
  endfacet
  facet normal 2.266168e-01 -7.182866e-01 -6.578063e-01
    outer loop
      vertex   1.033792e+01 -1.096651e+01 -1.160584e+01
      vertex   1.029631e+01 -1.107542e+01 -1.150125e+01
      vertex   1.013510e+01 -1.096651e+01 -1.167571e+01
    endloop
  endfacet
  facet normal 2.323405e-01 -7.008388e-01 -6.744204e-01
    outer loop
      vertex   1.033792e+01 -1.096651e+01 -1.160584e+01
      vertex   1.013510e+01 -1.096651e+01 -1.167571e+01
      vertex   1.015111e+01 -1.090844e+01 -1.173054e+01
    endloop
  endfacet
  facet normal 1.671744e-01 -7.008439e-01 -6.934483e-01
    outer loop
      vertex   1.015111e+01 -1.090844e+01 -1.173054e+01
      vertex   1.013510e+01 -1.096651e+01 -1.167571e+01
      vertex   9.937367e+00 -1.090844e+01 -1.178206e+01
    endloop
  endfacet
  facet normal 1.699738e-01 -6.884757e-01 -7.050603e-01
    outer loop
      vertex   1.015111e+01 -1.090844e+01 -1.173054e+01
      vertex   9.937367e+00 -1.090844e+01 -1.178206e+01
      vertex   9.947116e+00 -1.085394e+01 -1.183293e+01
    endloop
  endfacet
  facet normal 1.026782e-01 -6.884740e-01 -7.179560e-01
    outer loop
      vertex   9.947116e+00 -1.085394e+01 -1.183293e+01
      vertex   9.937367e+00 -1.090844e+01 -1.178206e+01
      vertex   9.724635e+00 -1.085394e+01 -1.186475e+01
    endloop
  endfacet
  facet normal 1.045544e-01 -6.742387e-01 -7.310749e-01
    outer loop
      vertex   9.947116e+00 -1.085394e+01 -1.183293e+01
      vertex   9.724635e+00 -1.085394e+01 -1.186475e+01
      vertex   9.728729e+00 -1.080658e+01 -1.190785e+01
    endloop
  endfacet
  facet normal 3.675316e-01 -6.741982e-01 -6.406070e-01
    outer loop
      vertex   1.060254e+01 -1.080658e+01 -1.165250e+01
      vertex   1.077778e+01 -1.085394e+01 -1.150211e+01
      vertex   1.058281e+01 -1.085394e+01 -1.161397e+01
    endloop
  endfacet
  facet normal 3.609371e-01 -6.884341e-01 -6.291128e-01
    outer loop
      vertex   1.058281e+01 -1.085394e+01 -1.161397e+01
      vertex   1.077778e+01 -1.085394e+01 -1.150211e+01
      vertex   1.074991e+01 -1.090844e+01 -1.145846e+01
    endloop
  endfacet
  facet normal 3.057289e-01 -6.742145e-01 -6.722831e-01
    outer loop
      vertex   1.060254e+01 -1.080658e+01 -1.165250e+01
      vertex   1.058281e+01 -1.085394e+01 -1.161397e+01
      vertex   1.039419e+01 -1.080658e+01 -1.174725e+01
    endloop
  endfacet
  facet normal 3.123396e-01 -6.562946e-01 -6.868197e-01
    outer loop
      vertex   1.060254e+01 -1.080658e+01 -1.165250e+01
      vertex   1.039419e+01 -1.080658e+01 -1.174725e+01
      vertex   1.040651e+01 -1.076831e+01 -1.177821e+01
    endloop
  endfacet
  facet normal 2.457492e-01 -6.563156e-01 -7.133423e-01
    outer loop
      vertex   1.040651e+01 -1.076831e+01 -1.177821e+01
      vertex   1.039419e+01 -1.080658e+01 -1.174725e+01
      vertex   1.018709e+01 -1.076831e+01 -1.185380e+01
    endloop
  endfacet
  facet normal 2.567003e-01 -6.155369e-01 -7.451304e-01
    outer loop
      vertex   1.040651e+01 -1.076831e+01 -1.177821e+01
      vertex   1.018709e+01 -1.076831e+01 -1.185380e+01
      vertex   1.019778e+01 -1.071951e+01 -1.189043e+01
    endloop
  endfacet
  facet normal 1.847022e-01 -6.155424e-01 -7.661545e-01
    outer loop
      vertex   1.019778e+01 -1.071951e+01 -1.189043e+01
      vertex   1.018709e+01 -1.076831e+01 -1.185380e+01
      vertex   9.968720e+00 -1.071951e+01 -1.194565e+01
    endloop
  endfacet
  facet normal 1.444621e-01 -7.874302e-01 -5.992365e-01
    outer loop
      vertex   9.880125e+00 -1.119019e+01 -1.148339e+01
      vertex   9.889311e+00 -1.115203e+01 -1.153132e+01
      vertex   1.006589e+01 -1.119019e+01 -1.143861e+01
    endloop
  endfacet
  facet normal 1.444621e-01 -7.874302e-01 -5.992365e-01
    outer loop
      vertex   1.006589e+01 -1.119019e+01 -1.143861e+01
      vertex   9.889311e+00 -1.115203e+01 -1.153132e+01
      vertex   1.007957e+01 -1.115203e+01 -1.148545e+01
    endloop
  endfacet
  facet normal 2.007751e-01 -7.874258e-01 -5.827949e-01
    outer loop
      vertex   1.006589e+01 -1.119019e+01 -1.143861e+01
      vertex   1.007957e+01 -1.115203e+01 -1.148545e+01
      vertex   1.024661e+01 -1.119019e+01 -1.137635e+01
    endloop
  endfacet
  facet normal 1.563692e-01 -7.448695e-01 -6.486278e-01
    outer loop
      vertex   1.007957e+01 -1.115203e+01 -1.148545e+01
      vertex   9.889311e+00 -1.115203e+01 -1.153132e+01
      vertex   9.905429e+00 -1.107542e+01 -1.161542e+01
    endloop
  endfacet
  facet normal 9.445995e-02 -7.448679e-01 -6.604915e-01
    outer loop
      vertex   9.905429e+00 -1.107542e+01 -1.161542e+01
      vertex   9.889311e+00 -1.115203e+01 -1.153132e+01
      vertex   9.703690e+00 -1.107542e+01 -1.164427e+01
    endloop
  endfacet
  facet normal 9.849934e-02 -7.182900e-01 -6.887361e-01
    outer loop
      vertex   9.905429e+00 -1.107542e+01 -1.161542e+01
      vertex   9.703690e+00 -1.107542e+01 -1.164427e+01
      vertex   9.714335e+00 -1.096651e+01 -1.175633e+01
    endloop
  endfacet
  facet normal 9.445995e-02 -7.448679e-01 -6.604915e-01
    outer loop
      vertex   9.703690e+00 -1.107542e+01 -1.164427e+01
      vertex   9.889311e+00 -1.115203e+01 -1.153132e+01
      vertex   9.695593e+00 -1.115203e+01 -1.155902e+01
    endloop
  endfacet
  facet normal 8.726711e-02 -7.874287e-01 -6.101970e-01
    outer loop
      vertex   9.695593e+00 -1.115203e+01 -1.155902e+01
      vertex   9.889311e+00 -1.115203e+01 -1.153132e+01
      vertex   9.880125e+00 -1.119019e+01 -1.148339e+01
    endloop
  endfacet
  facet normal 9.523198e-01 -3.051016e-01 8.903473e-17
    outer loop
      vertex   1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 8.571656e-01 -5.150409e-01 -8.657003e-05
    outer loop
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
    endloop
  endfacet
  facet normal 8.177242e-01 -5.756102e-01 -1.691309e-04
    outer loop
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 5.134026e-16
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 2.344465e-16
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
      vertex   1.195203e+01 -1.076831e+01 -8.310975e+00
      vertex   1.187542e+01 -1.085394e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 -1.758838e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -8.310975e+00
      vertex   1.195203e+01 -1.076831e+01 -8.310975e+00
      vertex   1.187542e+01 -1.085394e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 -2.008905e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -8.310975e+00
      vertex   1.187542e+01 -1.085394e+01 -7.716772e+00
      vertex   1.176651e+01 -1.096651e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.289475e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -7.716772e+00
      vertex   1.187542e+01 -1.085394e+01 -7.716772e+00
      vertex   1.176651e+01 -1.096651e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.247588e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -7.716772e+00
      vertex   1.176651e+01 -1.096651e+01 -7.122746e+00
      vertex   1.165394e+01 -1.107542e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.032943e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -7.122746e+00
      vertex   1.176651e+01 -1.096651e+01 -7.122746e+00
      vertex   1.165394e+01 -1.107542e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 9.737700e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -7.122746e+00
      vertex   1.165394e+01 -1.107542e+01 -6.528873e+00
      vertex   1.156831e+01 -1.115203e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.349497e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -6.528873e+00
      vertex   1.165394e+01 -1.107542e+01 -6.528873e+00
      vertex   1.156831e+01 -1.115203e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 1.187214e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -6.528873e+00
      vertex   1.156831e+01 -1.115203e+01 -5.935131e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 2.304179e-14
    outer loop
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -5.935131e+00
      vertex   1.156831e+01 -1.115203e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 2.514942e-14
    outer loop
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   1.156831e+01 -1.115203e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 2.706144e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -3.561030e+00
      vertex   1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 2.007838e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -3.561030e+00
      vertex   1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 2.084788e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -3.561030e+00
      vertex   1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   1.176651e+01 -1.096651e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.669351e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -3.561030e+00
      vertex   1.176651e+01 -1.096651e+01 -4.747953e+00
      vertex   1.176651e+01 -1.096651e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.717444e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -3.561030e+00
      vertex   1.176651e+01 -1.096651e+01 -4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.599367e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -3.561030e+00
      vertex   1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 1.626040e-14
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -3.561030e+00
      vertex   1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   1.195203e+01 -1.076831e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 5.227884e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -3.561030e+00
      vertex   1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   1.195203e+01 -1.076831e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 5.123565e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -3.561030e+00
      vertex   1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 4.051410e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -3.561030e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 3.323335e-16
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -2.374183e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -1.143957e-11
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 4.401963e-16
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -2.374183e+00
      vertex   1.195203e+01 -1.076831e+01 -1.143957e-11
      vertex   1.187542e+01 -1.085394e+01 -1.143961e-11
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 0.000000e+00
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -1.143961e-11
      vertex   1.195203e+01 -1.076831e+01 -1.143957e-11
      vertex   1.187542e+01 -1.085394e+01 2.374183e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 0.000000e+00
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -1.143961e-11
      vertex   1.187542e+01 -1.085394e+01 2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 2.374183e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 0.000000e+00
    outer loop
      vertex   1.176651e+01 -1.096651e+01 2.374183e+00
      vertex   1.187542e+01 -1.085394e+01 2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 4.747953e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 0.000000e+00
    outer loop
      vertex   1.176651e+01 -1.096651e+01 2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 4.747953e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 5.285734e-16
    outer loop
      vertex   1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   1.176651e+01 -1.096651e+01 4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 9.500000e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 5.278314e-16
    outer loop
      vertex   1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 7.549865e-16
    outer loop
      vertex   1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 0.000000e+00
    outer loop
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   1.195203e+01 -1.076831e+01 2.374183e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 0.000000e+00
    outer loop
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 2.374183e+00
      vertex   1.195203e+01 -1.076831e+01 -1.143957e-11
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 0.000000e+00
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -1.143957e-11
      vertex   1.195203e+01 -1.076831e+01 2.374183e+00
      vertex   1.187542e+01 -1.085394e+01 2.374183e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 7.770844e-16
    outer loop
      vertex   1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 4.747953e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 5.273925e-16
    outer loop
      vertex   1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   1.187542e+01 -1.085394e+01 4.747953e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 0.000000e+00
    outer loop
      vertex   1.195203e+01 -1.076831e+01 4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   1.195203e+01 -1.076831e+01 2.374183e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 0.000000e+00
    outer loop
      vertex   1.195203e+01 -1.076831e+01 2.374183e+00
      vertex   1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 2.374183e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 5.285734e-16
    outer loop
      vertex   1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   1.187542e+01 -1.085394e+01 4.747953e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 0.000000e+00
    outer loop
      vertex   1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   1.176651e+01 -1.096651e+01 4.747953e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 0.000000e+00
    outer loop
      vertex   1.187542e+01 -1.085394e+01 4.747953e+00
      vertex   1.176651e+01 -1.096651e+01 4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 2.374183e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 0.000000e+00
    outer loop
      vertex   1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   1.176651e+01 -1.096651e+01 4.747953e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.026191e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 9.852427e-16
    outer loop
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal 5.150402e-01 -8.571645e-01 -1.593807e-03
    outer loop
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   1.150684e+01 -1.119781e+01 9.500000e+00
    endloop
  endfacet
  facet normal 3.050974e-01 -9.523068e-01 -5.226111e-03
    outer loop
      vertex   1.150684e+01 -1.119781e+01 9.500000e+00
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
    endloop
  endfacet
  facet normal 5.829516e-01 -8.125069e-01 1.793632e-04
    outer loop
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 0.000000e+00
    outer loop
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 2.374183e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 0.000000e+00
    outer loop
      vertex   1.156831e+01 -1.115203e+01 2.374183e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -1.143963e-11
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 0.000000e+00
    outer loop
      vertex   1.156831e+01 -1.115203e+01 2.374183e+00
      vertex   1.156831e+01 -1.115203e+01 -1.143963e-11
      vertex   1.165394e+01 -1.107542e+01 -1.143965e-11
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 7.483387e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -1.143965e-11
      vertex   1.156831e+01 -1.115203e+01 -1.143963e-11
      vertex   1.165394e+01 -1.107542e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 7.803741e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -1.143965e-11
      vertex   1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.141291e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -2.374183e+00
      vertex   1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.186715e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -3.561030e+00
      vertex   1.187542e+01 -1.085394e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 3.051016e-01 -9.523198e-01 4.421329e-15
    outer loop
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   1.150684e+01 -1.119781e+01 -9.500000e+00
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
    endloop
  endfacet
  facet normal 5.150409e-01 -8.571656e-01 8.657003e-05
    outer loop
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   1.150684e+01 -1.119781e+01 -9.500000e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 -2.515856e-13
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -8.905377e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 1.288459e-14
    outer loop
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -8.905377e+00
      vertex   1.156831e+01 -1.115203e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 1.104510e-14
    outer loop
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -8.310975e+00
      vertex   1.156831e+01 -1.115203e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.196018e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -7.716772e+00
      vertex   1.156831e+01 -1.115203e+01 -8.310975e+00
      vertex   1.165394e+01 -1.107542e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.020134e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -7.716772e+00
      vertex   1.165394e+01 -1.107542e+01 -8.310975e+00
      vertex   1.165394e+01 -1.107542e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.046327e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -7.716772e+00
      vertex   1.165394e+01 -1.107542e+01 -8.310975e+00
      vertex   1.176651e+01 -1.096651e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 4.081962e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -7.716772e+00
      vertex   1.176651e+01 -1.096651e+01 -8.310975e+00
      vertex   1.176651e+01 -1.096651e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 4.366768e-15
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -7.716772e+00
      vertex   1.176651e+01 -1.096651e+01 -8.310975e+00
      vertex   1.187542e+01 -1.085394e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 -2.726635e-13
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -9.500000e+00
      vertex   1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 -2.106873e-13
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -8.905377e+00
      vertex   1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   1.165394e+01 -1.107542e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.394887e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -8.905377e+00
      vertex   1.165394e+01 -1.107542e+01 -8.905377e+00
      vertex   1.156831e+01 -1.115203e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 5.740305e-15
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -8.310975e+00
      vertex   1.165394e+01 -1.107542e+01 -8.905377e+00
      vertex   1.165394e+01 -1.107542e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 -2.200467e-13
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -9.500000e+00
      vertex   1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   1.165394e+01 -1.107542e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 -1.451891e-13
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -8.905377e+00
      vertex   1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   1.176651e+01 -1.096651e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 6.164235e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -8.905377e+00
      vertex   1.176651e+01 -1.096651e+01 -8.905377e+00
      vertex   1.165394e+01 -1.107542e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 2.012349e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -8.310975e+00
      vertex   1.176651e+01 -1.096651e+01 -8.905377e+00
      vertex   1.176651e+01 -1.096651e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 -1.504972e-13
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -9.500000e+00
      vertex   1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   1.176651e+01 -1.096651e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 -7.128144e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -8.905377e+00
      vertex   1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   1.187542e+01 -1.085394e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 2.217538e-15
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -8.905377e+00
      vertex   1.187542e+01 -1.085394e+01 -8.905377e+00
      vertex   1.176651e+01 -1.096651e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 2.142779e-15
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -8.310975e+00
      vertex   1.187542e+01 -1.085394e+01 -8.905377e+00
      vertex   1.187542e+01 -1.085394e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 -7.487452e-14
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   1.187542e+01 -1.085394e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 -2.565672e-14
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -8.905377e+00
      vertex   1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 2.227143e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -8.905377e+00
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
      vertex   1.187542e+01 -1.085394e+01 -8.310975e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 -2.845290e-14
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -9.500000e+00
      vertex   1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
    endloop
  endfacet
  facet normal 8.570961e-01 -5.149991e-01 1.273621e-02
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
      vertex   1.199019e+01 -1.071951e+01 -9.500000e+00
      vertex   1.199781e+01 -1.070684e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 9.514903e-01 -3.048358e-01 4.172969e-02
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -8.905377e+00
      vertex   1.199781e+01 -1.070684e+01 -9.500000e+00
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 2.815509e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -7.122746e+00
      vertex   1.156831e+01 -1.115203e+01 -6.528873e+00
      vertex   1.156831e+01 -1.115203e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 2.630833e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -7.122746e+00
      vertex   1.156831e+01 -1.115203e+01 -6.528873e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 1.238017e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -7.122746e+00
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 1.935875e-14
    outer loop
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 -3.561030e+00
      vertex   1.156831e+01 -1.115203e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 2.095781e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -2.374183e+00
      vertex   1.156831e+01 -1.115203e+01 -3.561030e+00
      vertex   1.165394e+01 -1.107542e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.996519e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -2.374183e+00
      vertex   1.165394e+01 -1.107542e+01 -3.561030e+00
      vertex   1.165394e+01 -1.107542e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 2.081428e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   1.165394e+01 -1.107542e+01 -3.561030e+00
      vertex   1.176651e+01 -1.096651e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 9.420935e-15
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -2.374183e+00
      vertex   1.156831e+01 -1.115203e+01 -1.143963e-11
      vertex   1.156831e+01 -1.115203e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 6.159732e-01 -7.877671e-01 8.627980e-15
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -2.374183e+00
      vertex   1.156831e+01 -1.115203e+01 -1.143963e-11
      vertex   1.151951e+01 -1.119019e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 -3.170243e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -7.716772e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 1.024003e-14
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -7.122746e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 1.044167e-14
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -7.122746e+00
      vertex   1.195203e+01 -1.076831e+01 -6.528873e+00
      vertex   1.187542e+01 -1.085394e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 -3.755118e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -6.528873e+00
      vertex   1.195203e+01 -1.076831e+01 -6.528873e+00
      vertex   1.187542e+01 -1.085394e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 -4.090778e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -6.528873e+00
      vertex   1.187542e+01 -1.085394e+01 -5.935131e+00
      vertex   1.176651e+01 -1.096651e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.404947e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -5.935131e+00
      vertex   1.187542e+01 -1.085394e+01 -5.935131e+00
      vertex   1.176651e+01 -1.096651e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.345563e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -5.935131e+00
      vertex   1.176651e+01 -1.096651e+01 -4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 0.000000e+00
    outer loop
      vertex   1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 2.374183e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 0.000000e+00
    outer loop
      vertex   1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   1.156831e+01 -1.115203e+01 4.747953e+00
      vertex   1.156831e+01 -1.115203e+01 2.374183e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 0.000000e+00
    outer loop
      vertex   1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   1.156831e+01 -1.115203e+01 2.374183e+00
      vertex   1.165394e+01 -1.107542e+01 -1.143965e-11
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 0.000000e+00
    outer loop
      vertex   1.165394e+01 -1.107542e+01 4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 2.374183e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 0.000000e+00
    outer loop
      vertex   1.176651e+01 -1.096651e+01 2.374183e+00
      vertex   1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -1.143964e-11
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 0.000000e+00
    outer loop
      vertex   1.176651e+01 -1.096651e+01 2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -1.143964e-11
      vertex   1.187542e+01 -1.085394e+01 -1.143961e-11
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 3.191366e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -1.143961e-11
      vertex   1.176651e+01 -1.096651e+01 -1.143964e-11
      vertex   1.187542e+01 -1.085394e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 3.228139e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -1.143961e-11
      vertex   1.187542e+01 -1.085394e+01 -2.374183e+00
      vertex   1.195203e+01 -1.076831e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 3.581056e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -2.374183e+00
      vertex   1.187542e+01 -1.085394e+01 -2.374183e+00
      vertex   1.195203e+01 -1.076831e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 0.000000e+00
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -1.143964e-11
      vertex   1.165394e+01 -1.107542e+01 2.374183e+00
      vertex   1.165394e+01 -1.107542e+01 -1.143965e-11
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 5.877816e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -1.143964e-11
      vertex   1.176651e+01 -1.096651e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 5.757678e-15
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -1.143964e-11
      vertex   1.165394e+01 -1.107542e+01 -1.143965e-11
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 7.329735e-15
    outer loop
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   1.195203e+01 -1.076831e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 6.807957e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -5.935131e+00
      vertex   1.195203e+01 -1.076831e+01 -4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 7.922798e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -5.935131e+00
      vertex   1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   1.187542e+01 -1.085394e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 7.562414e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -5.935131e+00
      vertex   1.187542e+01 -1.085394e+01 -4.747953e+00
      vertex   1.176651e+01 -1.096651e+01 -4.747953e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 2.582308e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -3.561030e+00
      vertex   1.187542e+01 -1.085394e+01 -2.374183e+00
      vertex   1.187542e+01 -1.085394e+01 -3.561030e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 2.256136e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -3.561030e+00
      vertex   1.187542e+01 -1.085394e+01 -2.374183e+00
      vertex   1.176651e+01 -1.096651e+01 -2.374183e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 -1.267577e-14
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -5.935131e+00
      vertex   1.195203e+01 -1.076831e+01 -6.528873e+00
      vertex   1.195203e+01 -1.076831e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 -1.259914e-14
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -5.935131e+00
      vertex   1.195203e+01 -1.076831e+01 -6.528873e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 2.223207e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -7.716772e+00
      vertex   1.195203e+01 -1.076831e+01 -8.310975e+00
      vertex   1.195203e+01 -1.076831e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 7.877671e-01 -6.159732e-01 2.355013e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -7.716772e+00
      vertex   1.195203e+01 -1.076831e+01 -8.310975e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.872176e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 2.494473e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -5.935131e+00
      vertex   1.156831e+01 -1.115203e+01 -4.747953e+00
      vertex   1.156831e+01 -1.115203e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 2.217874e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -5.935131e+00
      vertex   1.156831e+01 -1.115203e+01 -5.935131e+00
      vertex   1.165394e+01 -1.107542e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.969817e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -4.747953e+00
      vertex   1.165394e+01 -1.107542e+01 -5.935131e+00
      vertex   1.176651e+01 -1.096651e+01 -5.935131e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.040156e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -5.935131e+00
      vertex   1.165394e+01 -1.107542e+01 -5.935131e+00
      vertex   1.176651e+01 -1.096651e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.075079e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -5.935131e+00
      vertex   1.176651e+01 -1.096651e+01 -6.528873e+00
      vertex   1.187542e+01 -1.085394e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 8.528900e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -6.528873e+00
      vertex   1.176651e+01 -1.096651e+01 -6.528873e+00
      vertex   1.187542e+01 -1.085394e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 8.681850e-15
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -6.528873e+00
      vertex   1.187542e+01 -1.085394e+01 -7.122746e+00
      vertex   1.195203e+01 -1.076831e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 -3.753315e-15
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -7.122746e+00
      vertex   1.187542e+01 -1.085394e+01 -7.122746e+00
      vertex   1.195203e+01 -1.076831e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 2.294391e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -6.528873e+00
      vertex   1.165394e+01 -1.107542e+01 -5.935131e+00
      vertex   1.165394e+01 -1.107542e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.283083e-14
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -7.122746e+00
      vertex   1.176651e+01 -1.096651e+01 -6.528873e+00
      vertex   1.176651e+01 -1.096651e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 1.254894e-14
    outer loop
      vertex   1.176651e+01 -1.096651e+01 -7.122746e+00
      vertex   1.176651e+01 -1.096651e+01 -6.528873e+00
      vertex   1.165394e+01 -1.107542e+01 -6.528873e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.372309e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -7.716772e+00
      vertex   1.165394e+01 -1.107542e+01 -7.716772e+00
      vertex   1.156831e+01 -1.115203e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 6.667929e-01 -7.452430e-01 1.993855e-14
    outer loop
      vertex   1.156831e+01 -1.115203e+01 -7.122746e+00
      vertex   1.165394e+01 -1.107542e+01 -7.716772e+00
      vertex   1.165394e+01 -1.107542e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 6.953375e-01 -7.186833e-01 2.079313e-14
    outer loop
      vertex   1.165394e+01 -1.107542e+01 -7.716772e+00
      vertex   1.176651e+01 -1.096651e+01 -7.716772e+00
      vertex   1.165394e+01 -1.107542e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 7.452430e-01 -6.667929e-01 1.513500e-14
    outer loop
      vertex   1.195203e+01 -1.076831e+01 -7.716772e+00
      vertex   1.187542e+01 -1.085394e+01 -7.122746e+00
      vertex   1.187542e+01 -1.085394e+01 -7.716772e+00
    endloop
  endfacet
  facet normal 7.186833e-01 -6.953375e-01 1.490426e-14
    outer loop
      vertex   1.187542e+01 -1.085394e+01 -7.716772e+00
      vertex   1.187542e+01 -1.085394e+01 -7.122746e+00
      vertex   1.176651e+01 -1.096651e+01 -7.122746e+00
    endloop
  endfacet
  facet normal 9.769378e-02 1.136823e-01 9.887023e-01
    outer loop
      vertex   9.987858e+00 -1.070000e+01 1.195179e+01
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   9.744224e+00 -1.071951e+01 1.197811e+01
    endloop
  endfacet
  facet normal 6.085986e-02 -3.045360e-01 9.505545e-01
    outer loop
      vertex   9.744224e+00 -1.071951e+01 1.197811e+01
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   9.500000e+00 -1.070684e+01 1.199781e+01
    endloop
  endfacet
  facet normal 4.236787e-02 -5.145784e-01 8.563960e-01
    outer loop
      vertex   9.744224e+00 -1.071951e+01 1.197811e+01
      vertex   9.500000e+00 -1.070684e+01 1.199781e+01
      vertex   9.500000e+00 -1.071951e+01 1.199019e+01
    endloop
  endfacet
  facet normal 3.894308e-02 -6.155059e-01 7.871696e-01
    outer loop
      vertex   9.500000e+00 -1.071951e+01 1.199019e+01
      vertex   9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   9.744224e+00 -1.071951e+01 1.197811e+01
    endloop
  endfacet
  facet normal 3.894308e-02 -6.155059e-01 7.871696e-01
    outer loop
      vertex   9.744224e+00 -1.071951e+01 1.197811e+01
      vertex   9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   9.740482e+00 -1.076831e+01 1.194014e+01
    endloop
  endfacet
  facet normal 1.158906e-01 -6.154958e-01 7.795732e-01
    outer loop
      vertex   9.744224e+00 -1.071951e+01 1.197811e+01
      vertex   9.740482e+00 -1.076831e+01 1.194014e+01
      vertex   9.985945e+00 -1.071951e+01 1.194218e+01
    endloop
  endfacet
  facet normal 1.158906e-01 -6.154958e-01 7.795732e-01
    outer loop
      vertex   9.985945e+00 -1.071951e+01 1.194218e+01
      vertex   9.740482e+00 -1.076831e+01 1.194014e+01
      vertex   9.978498e+00 -1.076831e+01 1.190475e+01
    endloop
  endfacet
  facet normal 1.913594e-01 -6.154958e-01 7.645564e-01
    outer loop
      vertex   9.985945e+00 -1.071951e+01 1.194218e+01
      vertex   9.978498e+00 -1.076831e+01 1.190475e+01
      vertex   1.022293e+01 -1.071951e+01 1.188286e+01
    endloop
  endfacet
  facet normal 1.913594e-01 -6.154958e-01 7.645564e-01
    outer loop
      vertex   1.022293e+01 -1.071951e+01 1.188286e+01
      vertex   9.978498e+00 -1.076831e+01 1.190475e+01
      vertex   1.021186e+01 -1.076831e+01 1.184635e+01
    endloop
  endfacet
  facet normal 2.652866e-01 -6.155065e-01 7.421420e-01
    outer loop
      vertex   1.022293e+01 -1.071951e+01 1.188286e+01
      vertex   1.021186e+01 -1.076831e+01 1.184635e+01
      vertex   1.045297e+01 -1.071951e+01 1.180063e+01
    endloop
  endfacet
  facet normal 2.652866e-01 -6.155065e-01 7.421420e-01
    outer loop
      vertex   1.045297e+01 -1.071951e+01 1.180063e+01
      vertex   1.021186e+01 -1.076831e+01 1.184635e+01
      vertex   1.043837e+01 -1.076831e+01 1.176538e+01
    endloop
  endfacet
  facet normal 3.372206e-01 -6.155058e-01 7.123446e-01
    outer loop
      vertex   1.045297e+01 -1.071951e+01 1.180063e+01
      vertex   1.043837e+01 -1.076831e+01 1.176538e+01
      vertex   1.067380e+01 -1.071951e+01 1.169609e+01
    endloop
  endfacet
  facet normal 3.372206e-01 -6.155058e-01 7.123446e-01
    outer loop
      vertex   1.067380e+01 -1.071951e+01 1.169609e+01
      vertex   1.043837e+01 -1.076831e+01 1.176538e+01
      vertex   1.065582e+01 -1.076831e+01 1.166244e+01
    endloop
  endfacet
  facet normal 4.053906e-01 -6.154932e-01 6.758895e-01
    outer loop
      vertex   1.067380e+01 -1.071951e+01 1.169609e+01
      vertex   1.065582e+01 -1.076831e+01 1.166244e+01
      vertex   1.088337e+01 -1.071951e+01 1.157040e+01
    endloop
  endfacet
  facet normal 4.053906e-01 -6.154932e-01 6.758895e-01
    outer loop
      vertex   1.088337e+01 -1.071951e+01 1.157040e+01
      vertex   1.065582e+01 -1.076831e+01 1.166244e+01
      vertex   1.086217e+01 -1.076831e+01 1.153867e+01
    endloop
  endfacet
  facet normal 5.004708e-01 -6.141146e-01 6.102396e-01
    outer loop
      vertex   1.088337e+01 -1.071951e+01 1.157040e+01
      vertex   1.086217e+01 -1.076831e+01 1.153867e+01
      vertex   1.126084e+01 -1.071951e+01 1.126082e+01
    endloop
  endfacet
  facet normal 5.004708e-01 -6.141146e-01 6.102396e-01
    outer loop
      vertex   1.126084e+01 -1.071951e+01 1.126082e+01
      vertex   1.086217e+01 -1.076831e+01 1.153867e+01
      vertex   1.123386e+01 -1.076831e+01 1.123384e+01
    endloop
  endfacet
  facet normal 6.103851e-01 -6.141044e-01 5.003057e-01
    outer loop
      vertex   1.126084e+01 -1.071951e+01 1.126082e+01
      vertex   1.123386e+01 -1.076831e+01 1.123384e+01
      vertex   1.157025e+01 -1.071951e+01 1.088333e+01
    endloop
  endfacet
  facet normal 6.103851e-01 -6.141044e-01 5.003057e-01
    outer loop
      vertex   1.157025e+01 -1.071951e+01 1.088333e+01
      vertex   1.123386e+01 -1.076831e+01 1.123384e+01
      vertex   1.153853e+01 -1.076831e+01 1.086214e+01
    endloop
  endfacet
  facet normal 6.760276e-01 -6.154659e-01 4.052016e-01
    outer loop
      vertex   1.157025e+01 -1.071951e+01 1.088333e+01
      vertex   1.153853e+01 -1.076831e+01 1.086214e+01
      vertex   1.169588e+01 -1.071951e+01 1.067375e+01
    endloop
  endfacet
  facet normal 6.760276e-01 -6.154659e-01 4.052016e-01
    outer loop
      vertex   1.169588e+01 -1.071951e+01 1.067375e+01
      vertex   1.153853e+01 -1.076831e+01 1.086214e+01
      vertex   1.166223e+01 -1.076831e+01 1.065576e+01
    endloop
  endfacet
  facet normal 7.122372e-01 -6.154792e-01 3.374959e-01
    outer loop
      vertex   1.169588e+01 -1.071951e+01 1.067375e+01
      vertex   1.166223e+01 -1.076831e+01 1.065576e+01
      vertex   1.180051e+01 -1.071951e+01 1.045293e+01
    endloop
  endfacet
  facet normal 7.122372e-01 -6.154792e-01 3.374959e-01
    outer loop
      vertex   1.180051e+01 -1.071951e+01 1.045293e+01
      vertex   1.166223e+01 -1.076831e+01 1.065576e+01
      vertex   1.176526e+01 -1.076831e+01 1.043833e+01
    endloop
  endfacet
  facet normal 7.419238e-01 -6.155024e-01 2.659058e-01
    outer loop
      vertex   1.180051e+01 -1.071951e+01 1.045293e+01
      vertex   1.176526e+01 -1.076831e+01 1.043833e+01
      vertex   1.188297e+01 -1.071951e+01 1.022286e+01
    endloop
  endfacet
  facet normal 7.419238e-01 -6.155024e-01 2.659058e-01
    outer loop
      vertex   1.188297e+01 -1.071951e+01 1.022286e+01
      vertex   1.176526e+01 -1.076831e+01 1.043833e+01
      vertex   1.184645e+01 -1.076831e+01 1.021179e+01
    endloop
  endfacet
  facet normal 7.593397e-01 -6.158570e-01 2.100556e-01
    outer loop
      vertex   1.188297e+01 -1.071951e+01 1.022286e+01
      vertex   1.184645e+01 -1.076831e+01 1.021179e+01
      vertex   1.191555e+01 -1.071951e+01 1.010506e+01
    endloop
  endfacet
  facet normal 7.593397e-01 -6.158570e-01 2.100556e-01
    outer loop
      vertex   1.191555e+01 -1.071951e+01 1.010506e+01
      vertex   1.184645e+01 -1.076831e+01 1.021179e+01
      vertex   1.187854e+01 -1.076831e+01 1.009579e+01
    endloop
  endfacet
  facet normal 7.687385e-01 -6.158549e-01 1.725221e-01
    outer loop
      vertex   1.191555e+01 -1.071951e+01 1.010506e+01
      vertex   1.187854e+01 -1.076831e+01 1.009579e+01
      vertex   1.194231e+01 -1.071951e+01 9.985835e+00
    endloop
  endfacet
  facet normal 7.687385e-01 -6.158549e-01 1.725221e-01
    outer loop
      vertex   1.194231e+01 -1.071951e+01 9.985835e+00
      vertex   1.187854e+01 -1.076831e+01 1.009579e+01
      vertex   1.190489e+01 -1.076831e+01 9.978390e+00
    endloop
  endfacet
  facet normal 7.762663e-01 -6.158532e-01 1.346683e-01
    outer loop
      vertex   1.194231e+01 -1.071951e+01 9.985835e+00
      vertex   1.190489e+01 -1.076831e+01 9.978390e+00
      vertex   1.196320e+01 -1.071951e+01 9.865449e+00
    endloop
  endfacet
  facet normal 7.762663e-01 -6.158532e-01 1.346683e-01
    outer loop
      vertex   1.196320e+01 -1.071951e+01 9.865449e+00
      vertex   1.190489e+01 -1.076831e+01 9.978390e+00
      vertex   1.192545e+01 -1.076831e+01 9.859848e+00
    endloop
  endfacet
  facet normal 7.819265e-01 -6.158533e-01 9.651786e-02
    outer loop
      vertex   1.196320e+01 -1.071951e+01 9.865449e+00
      vertex   1.192545e+01 -1.076831e+01 9.859848e+00
      vertex   1.197817e+01 -1.071951e+01 9.744169e+00
    endloop
  endfacet
  facet normal 7.819265e-01 -6.158533e-01 9.651786e-02
    outer loop
      vertex   1.197817e+01 -1.071951e+01 9.744169e+00
      vertex   1.192545e+01 -1.076831e+01 9.859848e+00
      vertex   1.194019e+01 -1.076831e+01 9.740428e+00
    endloop
  endfacet
  facet normal 7.857148e-01 -6.158551e-01 5.809265e-02
    outer loop
      vertex   1.197817e+01 -1.071951e+01 9.744169e+00
      vertex   1.194019e+01 -1.076831e+01 9.740428e+00
      vertex   1.198718e+01 -1.071951e+01 9.622264e+00
    endloop
  endfacet
  facet normal 7.857148e-01 -6.158551e-01 5.809265e-02
    outer loop
      vertex   1.198718e+01 -1.071951e+01 9.622264e+00
      vertex   1.194019e+01 -1.076831e+01 9.740428e+00
      vertex   1.194907e+01 -1.076831e+01 9.620391e+00
    endloop
  endfacet
  facet normal 7.876187e-01 -6.158571e-01 1.941473e-02
    outer loop
      vertex   1.198718e+01 -1.071951e+01 9.622264e+00
      vertex   1.194907e+01 -1.076831e+01 9.620391e+00
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.876187e-01 -6.158571e-01 1.941473e-02
    outer loop
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.194907e+01 -1.076831e+01 9.620391e+00
      vertex   1.195203e+01 -1.076831e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.451173e-01 -6.666804e-01 1.836707e-02
    outer loop
      vertex   1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   1.194907e+01 -1.076831e+01 9.620391e+00
      vertex   1.187254e+01 -1.085394e+01 9.616629e+00
    endloop
  endfacet
  facet normal 7.451173e-01 -6.666804e-01 1.836707e-02
    outer loop
      vertex   1.195203e+01 -1.076831e+01 9.500000e+00
      vertex   1.187254e+01 -1.085394e+01 9.616629e+00
      vertex   1.187542e+01 -1.085394e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.247562e-01 -6.887737e-01 1.786517e-02
    outer loop
      vertex   1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   1.187254e+01 -1.085394e+01 9.616629e+00
      vertex   1.182081e+01 -1.090844e+01 9.614086e+00
    endloop
  endfacet
  facet normal 7.186331e-01 -6.952889e-01 1.182209e-02
    outer loop
      vertex   1.187542e+01 -1.085394e+01 9.500000e+00
      vertex   1.182081e+01 -1.090844e+01 9.614086e+00
      vertex   1.176651e+01 -1.096651e+01 9.500000e+00
    endloop
  endfacet
  facet normal 7.128097e-01 -7.011374e-01 1.757069e-02
    outer loop
      vertex   1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   1.182081e+01 -1.090844e+01 9.614086e+00
      vertex   1.176377e+01 -1.096651e+01 9.611282e+00
    endloop
  endfacet
  facet normal 6.952354e-01 -7.185778e-01 1.713749e-02
    outer loop
      vertex   1.176651e+01 -1.096651e+01 9.500000e+00
      vertex   1.176377e+01 -1.096651e+01 9.611282e+00
      vertex   1.165134e+01 -1.107542e+01 9.605755e+00
    endloop
  endfacet
  facet normal 6.935554e-01 -7.185760e-01 5.127874e-02
    outer loop
      vertex   1.165134e+01 -1.107542e+01 9.605755e+00
      vertex   1.176377e+01 -1.096651e+01 9.611282e+00
      vertex   1.164354e+01 -1.107542e+01 9.711199e+00
    endloop
  endfacet
  facet normal 6.650919e-01 -7.451407e-01 4.917427e-02
    outer loop
      vertex   1.165134e+01 -1.107542e+01 9.605755e+00
      vertex   1.164354e+01 -1.107542e+01 9.711199e+00
      vertex   1.155833e+01 -1.115203e+01 9.702803e+00
    endloop
  endfacet
  facet normal 6.618857e-01 -7.451391e-01 8.170052e-02
    outer loop
      vertex   1.155833e+01 -1.115203e+01 9.702803e+00
      vertex   1.164354e+01 -1.107542e+01 9.711199e+00
      vertex   1.154589e+01 -1.115203e+01 9.803536e+00
    endloop
  endfacet
  facet normal 6.114525e-01 -7.876734e-01 7.547524e-02
    outer loop
      vertex   1.155833e+01 -1.115203e+01 9.702803e+00
      vertex   1.154589e+01 -1.115203e+01 9.803536e+00
      vertex   1.149762e+01 -1.119019e+01 9.796374e+00
    endloop
  endfacet
  facet normal 6.070263e-01 -7.876733e-01 1.053082e-01
    outer loop
      vertex   1.149762e+01 -1.119019e+01 9.796374e+00
      vertex   1.154589e+01 -1.115203e+01 9.803536e+00
      vertex   1.148068e+01 -1.119019e+01 9.894006e+00
    endloop
  endfacet
  facet normal 4.425207e-01 -8.934662e-01 7.676939e-02
    outer loop
      vertex   1.149762e+01 -1.119019e+01 9.796374e+00
      vertex   1.148068e+01 -1.119019e+01 9.894006e+00
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
    endloop
  endfacet
  facet normal 4.382285e-01 -8.934671e-01 9.834827e-02
    outer loop
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
      vertex   1.148068e+01 -1.119019e+01 9.894006e+00
      vertex   1.145898e+01 -1.119019e+01 9.990698e+00
    endloop
  endfacet
  facet normal 3.603429e-01 -9.274786e-01 9.968142e-02
    outer loop
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
      vertex   1.145898e+01 -1.119019e+01 9.990698e+00
      vertex   1.143255e+01 -1.119019e+01 1.008623e+01
    endloop
  endfacet
  facet normal 5.937886e-01 -7.876763e-01 1.642593e-01
    outer loop
      vertex   1.143255e+01 -1.119019e+01 1.008623e+01
      vertex   1.145898e+01 -1.119019e+01 9.990698e+00
      vertex   1.150632e+01 -1.115203e+01 1.000256e+01
    endloop
  endfacet
  facet normal 5.937886e-01 -7.876763e-01 1.642593e-01
    outer loop
      vertex   1.143255e+01 -1.119019e+01 1.008623e+01
      vertex   1.150632e+01 -1.115203e+01 1.000256e+01
      vertex   1.147925e+01 -1.115203e+01 1.010040e+01
    endloop
  endfacet
  facet normal 6.427653e-01 -7.451424e-01 1.778077e-01
    outer loop
      vertex   1.147925e+01 -1.115203e+01 1.010040e+01
      vertex   1.150632e+01 -1.115203e+01 1.000256e+01
      vertex   1.158938e+01 -1.107542e+01 1.002336e+01
    endloop
  endfacet
  facet normal 6.427653e-01 -7.451424e-01 1.778077e-01
    outer loop
      vertex   1.147925e+01 -1.115203e+01 1.010040e+01
      vertex   1.158938e+01 -1.107542e+01 1.002336e+01
      vertex   1.156120e+01 -1.107542e+01 1.012526e+01
    endloop
  endfacet
  facet normal 6.702734e-01 -7.185778e-01 1.854173e-01
    outer loop
      vertex   1.156120e+01 -1.107542e+01 1.012526e+01
      vertex   1.158938e+01 -1.107542e+01 1.002336e+01
      vertex   1.169858e+01 -1.096651e+01 1.005071e+01
    endloop
  endfacet
  facet normal 6.702734e-01 -7.185778e-01 1.854173e-01
    outer loop
      vertex   1.156120e+01 -1.107542e+01 1.012526e+01
      vertex   1.169858e+01 -1.096651e+01 1.005071e+01
      vertex   1.166892e+01 -1.096651e+01 1.015793e+01
    endloop
  endfacet
  facet normal 6.872167e-01 -7.011374e-01 1.901043e-01
    outer loop
      vertex   1.166892e+01 -1.096651e+01 1.015793e+01
      vertex   1.169858e+01 -1.096651e+01 1.005071e+01
      vertex   1.175398e+01 -1.090844e+01 1.006459e+01
    endloop
  endfacet
  facet normal 6.872167e-01 -7.011374e-01 1.901043e-01
    outer loop
      vertex   1.166892e+01 -1.096651e+01 1.015793e+01
      vertex   1.175398e+01 -1.090844e+01 1.006459e+01
      vertex   1.172357e+01 -1.090844e+01 1.017451e+01
    endloop
  endfacet
  facet normal 6.987343e-01 -6.887737e-01 1.932904e-01
    outer loop
      vertex   1.172357e+01 -1.090844e+01 1.017451e+01
      vertex   1.175398e+01 -1.090844e+01 1.006459e+01
      vertex   1.180422e+01 -1.085394e+01 1.007718e+01
    endloop
  endfacet
  facet normal 6.987343e-01 -6.887737e-01 1.932904e-01
    outer loop
      vertex   1.172357e+01 -1.090844e+01 1.017451e+01
      vertex   1.180422e+01 -1.085394e+01 1.007718e+01
      vertex   1.177314e+01 -1.085394e+01 1.018955e+01
    endloop
  endfacet
  facet normal 7.183643e-01 -6.666804e-01 1.987206e-01
    outer loop
      vertex   1.177314e+01 -1.085394e+01 1.018955e+01
      vertex   1.180422e+01 -1.085394e+01 1.007718e+01
      vertex   1.187854e+01 -1.076831e+01 1.009579e+01
    endloop
  endfacet
  facet normal 7.183643e-01 -6.666804e-01 1.987206e-01
    outer loop
      vertex   1.177314e+01 -1.085394e+01 1.018955e+01
      vertex   1.187854e+01 -1.076831e+01 1.009579e+01
      vertex   1.184645e+01 -1.076831e+01 1.021179e+01
    endloop
  endfacet
  facet normal 3.684385e-02 -6.663402e-01 7.447370e-01
    outer loop
      vertex   9.500000e+00 -1.076831e+01 1.195203e+01
      vertex   9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   9.740482e+00 -1.076831e+01 1.194014e+01
    endloop
  endfacet
  facet normal 3.684385e-02 -6.663402e-01 7.447370e-01
    outer loop
      vertex   9.740482e+00 -1.076831e+01 1.194014e+01
      vertex   9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   9.732968e+00 -1.085394e+01 1.186389e+01
    endloop
  endfacet
  facet normal 1.096437e-01 -6.663304e-01 7.375514e-01
    outer loop
      vertex   9.740482e+00 -1.076831e+01 1.194014e+01
      vertex   9.732968e+00 -1.085394e+01 1.186389e+01
      vertex   9.978498e+00 -1.076831e+01 1.190475e+01
    endloop
  endfacet
  facet normal 1.096437e-01 -6.663304e-01 7.375514e-01
    outer loop
      vertex   9.978498e+00 -1.076831e+01 1.190475e+01
      vertex   9.732968e+00 -1.085394e+01 1.186389e+01
      vertex   9.963547e+00 -1.085394e+01 1.182962e+01
    endloop
  endfacet
  facet normal 1.810445e-01 -6.663304e-01 7.233441e-01
    outer loop
      vertex   9.978498e+00 -1.076831e+01 1.190475e+01
      vertex   9.963547e+00 -1.085394e+01 1.182962e+01
      vertex   1.021186e+01 -1.076831e+01 1.184635e+01
    endloop
  endfacet
  facet normal 1.810445e-01 -6.663304e-01 7.233441e-01
    outer loop
      vertex   1.021186e+01 -1.076831e+01 1.184635e+01
      vertex   9.963547e+00 -1.085394e+01 1.182962e+01
      vertex   1.018961e+01 -1.085394e+01 1.177303e+01
    endloop
  endfacet
  facet normal 2.509862e-01 -6.663408e-01 7.021366e-01
    outer loop
      vertex   1.021186e+01 -1.076831e+01 1.184635e+01
      vertex   1.018961e+01 -1.085394e+01 1.177303e+01
      vertex   1.043837e+01 -1.076831e+01 1.176538e+01
    endloop
  endfacet
  facet normal 2.509862e-01 -6.663408e-01 7.021366e-01
    outer loop
      vertex   1.043837e+01 -1.076831e+01 1.176538e+01
      vertex   1.018961e+01 -1.085394e+01 1.177303e+01
      vertex   1.040905e+01 -1.085394e+01 1.169460e+01
    endloop
  endfacet
  facet normal 3.190426e-01 -6.663401e-01 6.739455e-01
    outer loop
      vertex   1.043837e+01 -1.076831e+01 1.176538e+01
      vertex   1.040905e+01 -1.085394e+01 1.169460e+01
      vertex   1.065582e+01 -1.076831e+01 1.166244e+01
    endloop
  endfacet
  facet normal 3.190426e-01 -6.663401e-01 6.739455e-01
    outer loop
      vertex   1.065582e+01 -1.076831e+01 1.166244e+01
      vertex   1.040905e+01 -1.085394e+01 1.169460e+01
      vertex   1.061970e+01 -1.085394e+01 1.159487e+01
    endloop
  endfacet
  facet normal 3.835388e-01 -6.663279e-01 6.394569e-01
    outer loop
      vertex   1.065582e+01 -1.076831e+01 1.166244e+01
      vertex   1.061970e+01 -1.085394e+01 1.159487e+01
      vertex   1.086217e+01 -1.076831e+01 1.153867e+01
    endloop
  endfacet
  facet normal 3.835388e-01 -6.663279e-01 6.394569e-01
    outer loop
      vertex   1.086217e+01 -1.076831e+01 1.153867e+01
      vertex   1.061970e+01 -1.085394e+01 1.159487e+01
      vertex   1.081961e+01 -1.085394e+01 1.147497e+01
    endloop
  endfacet
  facet normal 4.736050e-01 -6.649915e-01 5.774813e-01
    outer loop
      vertex   1.086217e+01 -1.076831e+01 1.153867e+01
      vertex   1.081961e+01 -1.085394e+01 1.147497e+01
      vertex   1.123386e+01 -1.076831e+01 1.123384e+01
    endloop
  endfacet
  facet normal 4.736050e-01 -6.649915e-01 5.774813e-01
    outer loop
      vertex   1.123386e+01 -1.076831e+01 1.123384e+01
      vertex   1.081961e+01 -1.085394e+01 1.147497e+01
      vertex   1.117968e+01 -1.085394e+01 1.117967e+01
    endloop
  endfacet
  facet normal 5.776200e-01 -6.649816e-01 4.734496e-01
    outer loop
      vertex   1.123386e+01 -1.076831e+01 1.123384e+01
      vertex   1.117968e+01 -1.085394e+01 1.117967e+01
      vertex   1.153853e+01 -1.076831e+01 1.086214e+01
    endloop
  endfacet
  facet normal 5.776200e-01 -6.649816e-01 4.734496e-01
    outer loop
      vertex   1.153853e+01 -1.076831e+01 1.086214e+01
      vertex   1.117968e+01 -1.085394e+01 1.117967e+01
      vertex   1.147484e+01 -1.085394e+01 1.081957e+01
    endloop
  endfacet
  facet normal 6.395906e-01 -6.663015e-01 3.833618e-01
    outer loop
      vertex   1.153853e+01 -1.076831e+01 1.086214e+01
      vertex   1.147484e+01 -1.085394e+01 1.081957e+01
      vertex   1.166223e+01 -1.076831e+01 1.065576e+01
    endloop
  endfacet
  facet normal 6.395906e-01 -6.663015e-01 3.833618e-01
    outer loop
      vertex   1.166223e+01 -1.076831e+01 1.065576e+01
      vertex   1.147484e+01 -1.085394e+01 1.081957e+01
      vertex   1.159467e+01 -1.085394e+01 1.061965e+01
    endloop
  endfacet
  facet normal 6.738470e-01 -6.663143e-01 3.193046e-01
    outer loop
      vertex   1.166223e+01 -1.076831e+01 1.065576e+01
      vertex   1.159467e+01 -1.085394e+01 1.061965e+01
      vertex   1.176526e+01 -1.076831e+01 1.043833e+01
    endloop
  endfacet
  facet normal 6.738470e-01 -6.663143e-01 3.193046e-01
    outer loop
      vertex   1.176526e+01 -1.076831e+01 1.043833e+01
      vertex   1.159467e+01 -1.085394e+01 1.061965e+01
      vertex   1.169448e+01 -1.085394e+01 1.040901e+01
    endloop
  endfacet
  facet normal 7.019307e-01 -6.663368e-01 2.515722e-01
    outer loop
      vertex   1.176526e+01 -1.076831e+01 1.043833e+01
      vertex   1.169448e+01 -1.085394e+01 1.040901e+01
      vertex   1.184645e+01 -1.076831e+01 1.021179e+01
    endloop
  endfacet
  facet normal 7.019307e-01 -6.663368e-01 2.515722e-01
    outer loop
      vertex   1.184645e+01 -1.076831e+01 1.021179e+01
      vertex   1.169448e+01 -1.085394e+01 1.040901e+01
      vertex   1.177314e+01 -1.085394e+01 1.018955e+01
    endloop
  endfacet
  facet normal 3.583803e-02 -6.884412e-01 7.244062e-01
    outer loop
      vertex   9.732968e+00 -1.085394e+01 1.186389e+01
      vertex   9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   9.727888e+00 -1.090844e+01 1.181235e+01
    endloop
  endfacet
  facet normal 3.258764e-02 -6.949682e-01 7.183016e-01
    outer loop
      vertex   9.727888e+00 -1.090844e+01 1.181235e+01
      vertex   9.500000e+00 -1.085394e+01 1.187542e+01
      vertex   9.500000e+00 -1.096651e+01 1.176651e+01
    endloop
  endfacet
  facet normal 3.524785e-02 -7.008099e-01 7.124767e-01
    outer loop
      vertex   9.727888e+00 -1.090844e+01 1.181235e+01
      vertex   9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   9.722287e+00 -1.096651e+01 1.175551e+01
    endloop
  endfacet
  facet normal 3.437960e-02 -7.182585e-01 6.949265e-01
    outer loop
      vertex   9.722287e+00 -1.096651e+01 1.175551e+01
      vertex   9.500000e+00 -1.096651e+01 1.176651e+01
      vertex   9.500000e+00 -1.107542e+01 1.165394e+01
    endloop
  endfacet
  facet normal 3.437960e-02 -7.182585e-01 6.949265e-01
    outer loop
      vertex   9.722287e+00 -1.096651e+01 1.175551e+01
      vertex   9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   9.711247e+00 -1.107542e+01 1.164349e+01
    endloop
  endfacet
  facet normal 3.296984e-02 -7.448379e-01 6.664304e-01
    outer loop
      vertex   9.711247e+00 -1.107542e+01 1.164349e+01
      vertex   9.500000e+00 -1.107542e+01 1.165394e+01
      vertex   9.500000e+00 -1.115203e+01 1.156831e+01
    endloop
  endfacet
  facet normal 3.296984e-02 -7.448379e-01 6.664304e-01
    outer loop
      vertex   9.711247e+00 -1.107542e+01 1.164349e+01
      vertex   9.500000e+00 -1.115203e+01 1.156831e+01
      vertex   9.702849e+00 -1.115203e+01 1.155828e+01
    endloop
  endfacet
  facet normal 3.045946e-02 -7.874016e-01 6.156873e-01
    outer loop
      vertex   9.702849e+00 -1.115203e+01 1.155828e+01
      vertex   9.500000e+00 -1.115203e+01 1.156831e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
    endloop
  endfacet
  facet normal 3.045946e-02 -7.874016e-01 6.156873e-01
    outer loop
      vertex   9.702849e+00 -1.115203e+01 1.155828e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   9.698063e+00 -1.119019e+01 1.150971e+01
    endloop
  endfacet
  facet normal 2.547198e-02 -8.568875e-01 5.148737e-01
    outer loop
      vertex   9.698063e+00 -1.119019e+01 1.150971e+01
      vertex   9.500000e+00 -1.119019e+01 1.151951e+01
      vertex   9.500000e+00 -1.119781e+01 1.150684e+01
    endloop
  endfacet
  facet normal 3.216703e-02 -9.518270e-01 3.049437e-01
    outer loop
      vertex   9.698063e+00 -1.119019e+01 1.150971e+01
      vertex   9.500000e+00 -1.119781e+01 1.150684e+01
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 3.135815e-02 -9.477873e-01 3.173577e-01
    outer loop
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   9.890287e+00 -1.120000e+01 1.146144e+01
      vertex   9.698063e+00 -1.119019e+01 1.150971e+01
    endloop
  endfacet
  facet normal 6.609084e-02 -8.932976e-01 4.445799e-01
    outer loop
      vertex   9.698063e+00 -1.119019e+01 1.150971e+01
      vertex   9.890287e+00 -1.120000e+01 1.146144e+01
      vertex   9.894095e+00 -1.119019e+01 1.148057e+01
    endloop
  endfacet
  facet normal 9.064482e-02 -7.873937e-01 6.097497e-01
    outer loop
      vertex   9.698063e+00 -1.119019e+01 1.150971e+01
      vertex   9.894095e+00 -1.119019e+01 1.148057e+01
      vertex   9.903618e+00 -1.115203e+01 1.152843e+01
    endloop
  endfacet
  facet normal 1.496734e-01 -7.873937e-01 5.980042e-01
    outer loop
      vertex   9.903618e+00 -1.115203e+01 1.152843e+01
      vertex   9.894095e+00 -1.119019e+01 1.148057e+01
      vertex   1.010046e+01 -1.115203e+01 1.147917e+01
    endloop
  endfacet
  facet normal 1.620087e-01 -7.448291e-01 6.472888e-01
    outer loop
      vertex   9.903618e+00 -1.115203e+01 1.152843e+01
      vertex   1.010046e+01 -1.115203e+01 1.147917e+01
      vertex   1.012532e+01 -1.107542e+01 1.156110e+01
    endloop
  endfacet
  facet normal 2.245958e-01 -7.448384e-01 6.283092e-01
    outer loop
      vertex   1.012532e+01 -1.107542e+01 1.156110e+01
      vertex   1.010046e+01 -1.115203e+01 1.147917e+01
      vertex   1.032429e+01 -1.107542e+01 1.148998e+01
    endloop
  endfacet
  facet normal 2.341994e-01 -7.182590e-01 6.551753e-01
    outer loop
      vertex   1.012532e+01 -1.107542e+01 1.156110e+01
      vertex   1.032429e+01 -1.107542e+01 1.148998e+01
      vertex   1.036737e+01 -1.096651e+01 1.159398e+01
    endloop
  endfacet
  facet normal 2.977040e-01 -7.182584e-01 6.288698e-01
    outer loop
      vertex   1.036737e+01 -1.096651e+01 1.159398e+01
      vertex   1.032429e+01 -1.107542e+01 1.148998e+01
      vertex   1.056837e+01 -1.096651e+01 1.149883e+01
    endloop
  endfacet
  facet normal 3.052224e-01 -7.008098e-01 6.447518e-01
    outer loop
      vertex   1.036737e+01 -1.096651e+01 1.159398e+01
      vertex   1.056837e+01 -1.096651e+01 1.149883e+01
      vertex   1.059529e+01 -1.090844e+01 1.154920e+01
    endloop
  endfacet
  facet normal 3.669253e-01 -7.007980e-01 6.117581e-01
    outer loop
      vertex   1.059529e+01 -1.090844e+01 1.154920e+01
      vertex   1.056837e+01 -1.096651e+01 1.149883e+01
      vertex   1.079084e+01 -1.090844e+01 1.143191e+01
    endloop
  endfacet
  facet normal 3.730688e-01 -6.884291e-01 6.220008e-01
    outer loop
      vertex   1.059529e+01 -1.090844e+01 1.154920e+01
      vertex   1.079084e+01 -1.090844e+01 1.143191e+01
      vertex   1.081961e+01 -1.085394e+01 1.147497e+01
    endloop
  endfacet
  facet normal 4.607261e-01 -6.871225e-01 5.617776e-01
    outer loop
      vertex   1.081961e+01 -1.085394e+01 1.147497e+01
      vertex   1.079084e+01 -1.090844e+01 1.143191e+01
      vertex   1.117968e+01 -1.085394e+01 1.117967e+01
    endloop
  endfacet
  facet normal 1.091297e-01 -8.932977e-01 4.360161e-01
    outer loop
      vertex   9.894095e+00 -1.119019e+01 1.148057e+01
      vertex   9.890287e+00 -1.120000e+01 1.146144e+01
      vertex   1.008629e+01 -1.119019e+01 1.143247e+01
    endloop
  endfacet
  facet normal 9.253992e-02 -9.477376e-01 3.053354e-01
    outer loop
      vertex   1.008629e+01 -1.119019e+01 1.143247e+01
      vertex   9.890287e+00 -1.120000e+01 1.146144e+01
      vertex   1.026538e+01 -1.120000e+01 1.134775e+01
    endloop
  endfacet
  facet normal 1.512875e-01 -8.933027e-01 4.232285e-01
    outer loop
      vertex   1.008629e+01 -1.119019e+01 1.143247e+01
      vertex   1.026538e+01 -1.120000e+01 1.134775e+01
      vertex   1.027284e+01 -1.119019e+01 1.136578e+01
    endloop
  endfacet
  facet normal 1.923102e-01 -8.933024e-01 4.062359e-01
    outer loop
      vertex   1.027284e+01 -1.119019e+01 1.136578e+01
      vertex   1.026538e+01 -1.120000e+01 1.134775e+01
      vertex   1.045194e+01 -1.119019e+01 1.128100e+01
    endloop
  endfacet
  facet normal 2.637582e-01 -7.874016e-01 5.571628e-01
    outer loop
      vertex   1.027284e+01 -1.119019e+01 1.136578e+01
      vertex   1.045194e+01 -1.119019e+01 1.128100e+01
      vertex   1.047494e+01 -1.115203e+01 1.132404e+01
    endloop
  endfacet
  facet normal 3.170802e-01 -7.873916e-01 5.286535e-01
    outer loop
      vertex   1.047494e+01 -1.115203e+01 1.132404e+01
      vertex   1.045194e+01 -1.119019e+01 1.128100e+01
      vertex   1.064900e+01 -1.115203e+01 1.121964e+01
    endloop
  endfacet
  facet normal 3.432122e-01 -7.448268e-01 5.722223e-01
    outer loop
      vertex   1.047494e+01 -1.115203e+01 1.132404e+01
      vertex   1.064900e+01 -1.115203e+01 1.121964e+01
      vertex   1.069657e+01 -1.107542e+01 1.129083e+01
    endloop
  endfacet
  facet normal 4.239778e-01 -7.436299e-01 5.169694e-01
    outer loop
      vertex   1.069657e+01 -1.107542e+01 1.129083e+01
      vertex   1.064900e+01 -1.115203e+01 1.121964e+01
      vertex   1.102308e+01 -1.107542e+01 1.102306e+01
    endloop
  endfacet
  facet normal 4.420442e-01 -7.169922e-01 5.389983e-01
    outer loop
      vertex   1.069657e+01 -1.107542e+01 1.129083e+01
      vertex   1.102308e+01 -1.107542e+01 1.102306e+01
      vertex   1.110267e+01 -1.096651e+01 1.110266e+01
    endloop
  endfacet
  facet normal 5.391288e-01 -7.169829e-01 4.419000e-01
    outer loop
      vertex   1.110267e+01 -1.096651e+01 1.110266e+01
      vertex   1.102308e+01 -1.107542e+01 1.102306e+01
      vertex   1.138429e+01 -1.096651e+01 1.075907e+01
    endloop
  endfacet
  facet normal 5.526943e-01 -6.995018e-01 4.530190e-01
    outer loop
      vertex   1.110267e+01 -1.096651e+01 1.110266e+01
      vertex   1.138429e+01 -1.096651e+01 1.075907e+01
      vertex   1.143178e+01 -1.090844e+01 1.079080e+01
    endloop
  endfacet
  facet normal 6.118880e-01 -7.007726e-01 3.667572e-01
    outer loop
      vertex   1.143178e+01 -1.090844e+01 1.079080e+01
      vertex   1.138429e+01 -1.096651e+01 1.075907e+01
      vertex   1.154899e+01 -1.090844e+01 1.059524e+01
    endloop
  endfacet
  facet normal 6.221322e-01 -6.884033e-01 3.728974e-01
    outer loop
      vertex   1.143178e+01 -1.090844e+01 1.079080e+01
      vertex   1.154899e+01 -1.090844e+01 1.059524e+01
      vertex   1.159467e+01 -1.085394e+01 1.061965e+01
    endloop
  endfacet
  facet normal 6.554528e-01 -6.884159e-01 3.105884e-01
    outer loop
      vertex   1.159467e+01 -1.085394e+01 1.061965e+01
      vertex   1.154899e+01 -1.090844e+01 1.059524e+01
      vertex   1.169448e+01 -1.085394e+01 1.040901e+01
    endloop
  endfacet
  facet normal 1.504509e-01 -9.477674e-01 2.812497e-01
    outer loop
      vertex   1.026538e+01 -1.120000e+01 1.134775e+01
      vertex   1.061105e+01 -1.120000e+01 1.116284e+01
      vertex   1.045194e+01 -1.119019e+01 1.128100e+01
    endloop
  endfacet
  facet normal 2.311894e-01 -8.932964e-01 3.854517e-01
    outer loop
      vertex   1.045194e+01 -1.119019e+01 1.128100e+01
      vertex   1.061105e+01 -1.120000e+01 1.116284e+01
      vertex   1.062189e+01 -1.119019e+01 1.117906e+01
    endloop
  endfacet
  facet normal 3.170802e-01 -7.873916e-01 5.286535e-01
    outer loop
      vertex   1.045194e+01 -1.119019e+01 1.128100e+01
      vertex   1.062189e+01 -1.119019e+01 1.117906e+01
      vertex   1.064900e+01 -1.115203e+01 1.121964e+01
    endloop
  endfacet
  facet normal 3.917885e-01 -7.863113e-01 4.777199e-01
    outer loop
      vertex   1.064900e+01 -1.115203e+01 1.121964e+01
      vertex   1.062189e+01 -1.119019e+01 1.117906e+01
      vertex   1.096253e+01 -1.115203e+01 1.096251e+01
    endloop
  endfacet
  facet normal 4.239778e-01 -7.436299e-01 5.169694e-01
    outer loop
      vertex   1.064900e+01 -1.115203e+01 1.121964e+01
      vertex   1.096253e+01 -1.115203e+01 1.096251e+01
      vertex   1.102308e+01 -1.107542e+01 1.102306e+01
    endloop
  endfacet
  facet normal 5.170951e-01 -7.436211e-01 4.238400e-01
    outer loop
      vertex   1.102308e+01 -1.107542e+01 1.102306e+01
      vertex   1.096253e+01 -1.115203e+01 1.096251e+01
      vertex   1.129071e+01 -1.107542e+01 1.069654e+01
    endloop
  endfacet
  facet normal 5.391288e-01 -7.169829e-01 4.419000e-01
    outer loop
      vertex   1.102308e+01 -1.107542e+01 1.102306e+01
      vertex   1.129071e+01 -1.107542e+01 1.069654e+01
      vertex   1.138429e+01 -1.096651e+01 1.075907e+01
    endloop
  endfacet
  facet normal 5.968171e-01 -7.182221e-01 3.577239e-01
    outer loop
      vertex   1.138429e+01 -1.096651e+01 1.075907e+01
      vertex   1.129071e+01 -1.107542e+01 1.069654e+01
      vertex   1.149863e+01 -1.096651e+01 1.056832e+01
    endloop
  endfacet
  facet normal 6.118880e-01 -7.007726e-01 3.667572e-01
    outer loop
      vertex   1.138429e+01 -1.096651e+01 1.075907e+01
      vertex   1.149863e+01 -1.096651e+01 1.056832e+01
      vertex   1.154899e+01 -1.090844e+01 1.059524e+01
    endloop
  endfacet
  facet normal 6.446596e-01 -7.007850e-01 3.054740e-01
    outer loop
      vertex   1.154899e+01 -1.090844e+01 1.059524e+01
      vertex   1.149863e+01 -1.096651e+01 1.056832e+01
      vertex   1.164663e+01 -1.090844e+01 1.038919e+01
    endloop
  endfacet
  facet normal 6.554528e-01 -6.884159e-01 3.105884e-01
    outer loop
      vertex   1.154899e+01 -1.090844e+01 1.059524e+01
      vertex   1.164663e+01 -1.090844e+01 1.038919e+01
      vertex   1.169448e+01 -1.085394e+01 1.040901e+01
    endloop
  endfacet
  facet normal 6.827686e-01 -6.884378e-01 2.447046e-01
    outer loop
      vertex   1.169448e+01 -1.085394e+01 1.040901e+01
      vertex   1.164663e+01 -1.090844e+01 1.038919e+01
      vertex   1.177314e+01 -1.085394e+01 1.018955e+01
    endloop
  endfacet
  facet normal 2.858443e-01 -8.926442e-01 3.485389e-01
    outer loop
      vertex   1.062189e+01 -1.119019e+01 1.117906e+01
      vertex   1.061105e+01 -1.120000e+01 1.116284e+01
      vertex   1.092802e+01 -1.119019e+01 1.092800e+01
    endloop
  endfacet
  facet normal 2.858443e-01 -8.926442e-01 3.485389e-01
    outer loop
      vertex   1.092802e+01 -1.119019e+01 1.092800e+01
      vertex   1.061105e+01 -1.120000e+01 1.116284e+01
      vertex   1.091422e+01 -1.120000e+01 1.091421e+01
    endloop
  endfacet
  facet normal 3.486259e-01 -8.926394e-01 2.857532e-01
    outer loop
      vertex   1.092802e+01 -1.119019e+01 1.092800e+01
      vertex   1.091422e+01 -1.120000e+01 1.091421e+01
      vertex   1.117895e+01 -1.119019e+01 1.062186e+01
    endloop
  endfacet
  facet normal 3.486259e-01 -8.926394e-01 2.857532e-01
    outer loop
      vertex   1.117895e+01 -1.119019e+01 1.062186e+01
      vertex   1.091422e+01 -1.120000e+01 1.091421e+01
      vertex   1.116273e+01 -1.120000e+01 1.061102e+01
    endloop
  endfacet
  facet normal 3.855419e-01 -8.932836e-01 2.310885e-01
    outer loop
      vertex   1.117895e+01 -1.119019e+01 1.062186e+01
      vertex   1.116273e+01 -1.120000e+01 1.061102e+01
      vertex   1.128082e+01 -1.119019e+01 1.045189e+01
    endloop
  endfacet
  facet normal 2.818291e-01 -9.475441e-01 1.507732e-01
    outer loop
      vertex   1.128082e+01 -1.119019e+01 1.045189e+01
      vertex   1.116273e+01 -1.120000e+01 1.061102e+01
      vertex   1.134766e+01 -1.120000e+01 1.026535e+01
    endloop
  endfacet
  facet normal 4.061866e-01 -8.932898e-01 1.924728e-01
    outer loop
      vertex   1.128082e+01 -1.119019e+01 1.045189e+01
      vertex   1.134766e+01 -1.120000e+01 1.026535e+01
      vertex   1.136568e+01 -1.119019e+01 1.027281e+01
    endloop
  endfacet
  facet normal 4.231059e-01 -8.933008e-01 1.516413e-01
    outer loop
      vertex   1.136568e+01 -1.119019e+01 1.027281e+01
      vertex   1.134766e+01 -1.120000e+01 1.026535e+01
      vertex   1.143255e+01 -1.119019e+01 1.008623e+01
    endloop
  endfacet
  facet normal 5.802995e-01 -7.873989e-01 2.079796e-01
    outer loop
      vertex   1.136568e+01 -1.119019e+01 1.027281e+01
      vertex   1.143255e+01 -1.119019e+01 1.008623e+01
      vertex   1.147925e+01 -1.115203e+01 1.010040e+01
    endloop
  endfacet
  facet normal 3.045619e-01 -9.479944e-01 9.245869e-02
    outer loop
      vertex   1.134766e+01 -1.120000e+01 1.026535e+01
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
      vertex   1.143255e+01 -1.119019e+01 1.008623e+01
    endloop
  endfacet
  facet normal 3.712703e-01 -9.273932e-01 4.582811e-02
    outer loop
      vertex   1.149762e+01 -1.119019e+01 9.796374e+00
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
      vertex   1.150976e+01 -1.119019e+01 9.698018e+00
    endloop
  endfacet
  facet normal 3.174537e-01 -9.477575e-01 3.128708e-02
    outer loop
      vertex   1.150976e+01 -1.119019e+01 9.698018e+00
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
    endloop
  endfacet
  facet normal 3.049443e-01 -9.518289e-01 3.210523e-02
    outer loop
      vertex   1.150976e+01 -1.119019e+01 9.698018e+00
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   1.150684e+01 -1.119781e+01 9.500000e+00
    endloop
  endfacet
  facet normal 3.976664e-01 -9.170589e-01 2.940188e-02
    outer loop
      vertex   1.150976e+01 -1.119019e+01 9.698018e+00
      vertex   1.150684e+01 -1.119781e+01 9.500000e+00
      vertex   1.151707e+01 -1.119019e+01 9.599155e+00
    endloop
  endfacet
  facet normal 5.149994e-01 -8.570966e-01 1.269469e-02
    outer loop
      vertex   1.151707e+01 -1.119019e+01 9.599155e+00
      vertex   1.150684e+01 -1.119781e+01 9.500000e+00
      vertex   1.151951e+01 -1.119019e+01 9.500000e+00
    endloop
  endfacet
  facet normal 6.159022e-01 -7.876763e-01 1.518193e-02
    outer loop
      vertex   1.151707e+01 -1.119019e+01 9.599155e+00
      vertex   1.151951e+01 -1.119019e+01 9.500000e+00
      vertex   1.156831e+01 -1.115203e+01 9.500000e+00
    endloop
  endfacet
  facet normal 6.159022e-01 -7.876763e-01 1.518193e-02
    outer loop
      vertex   1.151707e+01 -1.119019e+01 9.599155e+00
      vertex   1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   1.156581e+01 -1.115203e+01 9.601551e+00
    endloop
  endfacet
  facet normal 6.667029e-01 -7.451424e-01 1.643416e-02
    outer loop
      vertex   1.156581e+01 -1.115203e+01 9.601551e+00
      vertex   1.156831e+01 -1.115203e+01 9.500000e+00
      vertex   1.165394e+01 -1.107542e+01 9.500000e+00
    endloop
  endfacet
  facet normal 6.667029e-01 -7.451424e-01 1.643416e-02
    outer loop
      vertex   1.156581e+01 -1.115203e+01 9.601551e+00
      vertex   1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   1.165134e+01 -1.107542e+01 9.605755e+00
    endloop
  endfacet
  facet normal 6.952354e-01 -7.185778e-01 1.713749e-02
    outer loop
      vertex   1.165134e+01 -1.107542e+01 9.605755e+00
      vertex   1.165394e+01 -1.107542e+01 9.500000e+00
      vertex   1.176651e+01 -1.096651e+01 9.500000e+00
    endloop
  endfacet
  facet normal 8.569744e-01 -5.149259e-01 2.112434e-02
    outer loop
      vertex   1.199019e+01 -1.071951e+01 9.500000e+00
      vertex   1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   1.198718e+01 -1.071951e+01 9.622264e+00
    endloop
  endfacet
  facet normal 9.895786e-01 -1.240202e-01 7.316553e-02
    outer loop
      vertex   1.198718e+01 -1.071951e+01 9.622264e+00
      vertex   1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   1.197817e+01 -1.071951e+01 9.744169e+00
    endloop
  endfacet
  facet normal 9.505662e-01 -3.045398e-01 6.065883e-02
    outer loop
      vertex   1.199781e+01 -1.070684e+01 9.500000e+00
      vertex   1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   1.197817e+01 -1.071951e+01 9.744169e+00
    endloop
  endfacet
  facet normal 9.887950e-01 1.130821e-01 9.745201e-02
    outer loop
      vertex   1.197817e+01 -1.071951e+01 9.744169e+00
      vertex   1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
    endloop
  endfacet
  facet normal 9.741701e-01 -1.911366e-01 1.202476e-01
    outer loop
      vertex   1.197817e+01 -1.071951e+01 9.744169e+00
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
      vertex   1.196320e+01 -1.071951e+01 9.865449e+00
    endloop
  endfacet
  facet normal 8.804288e-01 -4.489053e-01 1.527386e-01
    outer loop
      vertex   1.196320e+01 -1.071951e+01 9.865449e+00
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
      vertex   1.194231e+01 -1.071951e+01 9.985835e+00
    endloop
  endfacet
  facet normal 9.502419e-01 1.175724e-01 2.884737e-01
    outer loop
      vertex   1.180957e+01 -1.070000e+01 1.045668e+01
      vertex   1.188297e+01 -1.071951e+01 1.022286e+01
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
    endloop
  endfacet
  facet normal 9.462122e-01 -1.901827e-01 2.617500e-01
    outer loop
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
      vertex   1.188297e+01 -1.071951e+01 1.022286e+01
      vertex   1.191555e+01 -1.071951e+01 1.010506e+01
    endloop
  endfacet
  facet normal 8.718916e-01 -4.489069e-01 1.956720e-01
    outer loop
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
      vertex   1.191555e+01 -1.071951e+01 1.010506e+01
      vertex   1.194231e+01 -1.071951e+01 9.985835e+00
    endloop
  endfacet
  facet normal 8.764729e-01 1.092315e-01 4.688963e-01
    outer loop
      vertex   1.157841e+01 -1.070000e+01 1.088878e+01
      vertex   1.169588e+01 -1.071951e+01 1.067375e+01
      vertex   1.180957e+01 -1.070000e+01 1.045668e+01
    endloop
  endfacet
  facet normal 8.076677e-01 -4.485547e-01 3.827159e-01
    outer loop
      vertex   1.180957e+01 -1.070000e+01 1.045668e+01
      vertex   1.169588e+01 -1.071951e+01 1.067375e+01
      vertex   1.180051e+01 -1.071951e+01 1.045293e+01
    endloop
  endfacet
  facet normal 8.413410e-01 -4.485765e-01 3.015369e-01
    outer loop
      vertex   1.180957e+01 -1.070000e+01 1.045668e+01
      vertex   1.180051e+01 -1.071951e+01 1.045293e+01
      vertex   1.188297e+01 -1.071951e+01 1.022286e+01
    endloop
  endfacet
  facet normal 6.917276e-01 -4.472676e-01 5.669785e-01
    outer loop
      vertex   1.126778e+01 -1.070000e+01 1.126776e+01
      vertex   1.126084e+01 -1.071951e+01 1.126082e+01
      vertex   1.157841e+01 -1.070000e+01 1.088878e+01
    endloop
  endfacet
  facet normal 6.917276e-01 -4.472676e-01 5.669785e-01
    outer loop
      vertex   1.157841e+01 -1.070000e+01 1.088878e+01
      vertex   1.126084e+01 -1.071951e+01 1.126082e+01
      vertex   1.157025e+01 -1.071951e+01 1.088333e+01
    endloop
  endfacet
  facet normal 7.666018e-01 -4.485423e-01 4.594905e-01
    outer loop
      vertex   1.157841e+01 -1.070000e+01 1.088878e+01
      vertex   1.157025e+01 -1.071951e+01 1.088333e+01
      vertex   1.169588e+01 -1.071951e+01 1.067375e+01
    endloop
  endfacet
  facet normal 5.671683e-01 -4.472771e-01 6.915659e-01
    outer loop
      vertex   1.126084e+01 -1.071951e+01 1.126082e+01
      vertex   1.126778e+01 -1.070000e+01 1.126776e+01
      vertex   1.088337e+01 -1.071951e+01 1.157040e+01
    endloop
  endfacet
  facet normal 5.671683e-01 -4.472771e-01 6.915659e-01
    outer loop
      vertex   1.088337e+01 -1.071951e+01 1.157040e+01
      vertex   1.126778e+01 -1.070000e+01 1.126776e+01
      vertex   1.088882e+01 -1.070000e+01 1.157855e+01
    endloop
  endfacet
  facet normal 4.597107e-01 -4.485678e-01 7.664548e-01
    outer loop
      vertex   1.088337e+01 -1.071951e+01 1.157040e+01
      vertex   1.088882e+01 -1.070000e+01 1.157855e+01
      vertex   1.067380e+01 -1.071951e+01 1.169609e+01
    endloop
  endfacet
  facet normal 4.686508e-01 1.133123e-01 8.760860e-01
    outer loop
      vertex   1.067380e+01 -1.071951e+01 1.169609e+01
      vertex   1.088882e+01 -1.070000e+01 1.157855e+01
      vertex   1.045672e+01 -1.070000e+01 1.180969e+01
    endloop
  endfacet
  facet normal 3.824085e-01 -4.485797e-01 8.077995e-01
    outer loop
      vertex   1.067380e+01 -1.071951e+01 1.169609e+01
      vertex   1.045672e+01 -1.070000e+01 1.180969e+01
      vertex   1.045297e+01 -1.071951e+01 1.180063e+01
    endloop
  endfacet
  facet normal 3.008353e-01 -4.485803e-01 8.415900e-01
    outer loop
      vertex   1.045297e+01 -1.071951e+01 1.180063e+01
      vertex   1.045672e+01 -1.070000e+01 1.180969e+01
      vertex   1.022293e+01 -1.071951e+01 1.188286e+01
    endloop
  endfacet
  facet normal 2.881984e-01 1.127422e-01 9.509106e-01
    outer loop
      vertex   1.045672e+01 -1.070000e+01 1.180969e+01
      vertex   9.987858e+00 -1.070000e+01 1.195179e+01
      vertex   1.022293e+01 -1.071951e+01 1.188286e+01
    endloop
  endfacet
  facet normal 2.170007e-01 -4.485703e-01 8.670037e-01
    outer loop
      vertex   1.022293e+01 -1.071951e+01 1.188286e+01
      vertex   9.987858e+00 -1.070000e+01 1.195179e+01
      vertex   9.985945e+00 -1.071951e+01 1.194218e+01
    endloop
  endfacet
  facet normal 1.314195e-01 -4.485703e-01 8.840326e-01
    outer loop
      vertex   9.985945e+00 -1.071951e+01 1.194218e+01
      vertex   9.987858e+00 -1.070000e+01 1.195179e+01
      vertex   9.744224e+00 -1.071951e+01 1.197811e+01
    endloop
  endfacet
  facet normal 9.064482e-02 -7.873937e-01 6.097497e-01
    outer loop
      vertex   9.698063e+00 -1.119019e+01 1.150971e+01
      vertex   9.903618e+00 -1.115203e+01 1.152843e+01
      vertex   9.702849e+00 -1.115203e+01 1.155828e+01
    endloop
  endfacet
  facet normal 9.811532e-02 -7.448291e-01 6.600023e-01
    outer loop
      vertex   9.702849e+00 -1.115203e+01 1.155828e+01
      vertex   9.903618e+00 -1.115203e+01 1.152843e+01
      vertex   9.920328e+00 -1.107542e+01 1.161241e+01
    endloop
  endfacet
  facet normal 9.811532e-02 -7.448291e-01 6.600023e-01
    outer loop
      vertex   9.702849e+00 -1.115203e+01 1.155828e+01
      vertex   9.920328e+00 -1.107542e+01 1.161241e+01
      vertex   9.711247e+00 -1.107542e+01 1.164349e+01
    endloop
  endfacet
  facet normal 1.023105e-01 -7.182493e-01 6.882227e-01
    outer loop
      vertex   9.711247e+00 -1.107542e+01 1.164349e+01
      vertex   9.920328e+00 -1.107542e+01 1.161241e+01
      vertex   9.942294e+00 -1.096651e+01 1.172281e+01
    endloop
  endfacet
  facet normal 1.023105e-01 -7.182493e-01 6.882227e-01
    outer loop
      vertex   9.711247e+00 -1.107542e+01 1.164349e+01
      vertex   9.942294e+00 -1.096651e+01 1.172281e+01
      vertex   9.722287e+00 -1.096651e+01 1.175551e+01
    endloop
  endfacet
  facet normal 1.048943e-01 -7.008004e-01 7.056032e-01
    outer loop
      vertex   9.722287e+00 -1.096651e+01 1.175551e+01
      vertex   9.942294e+00 -1.096651e+01 1.172281e+01
      vertex   9.953440e+00 -1.090844e+01 1.177882e+01
    endloop
  endfacet
  facet normal 1.048943e-01 -7.008004e-01 7.056032e-01
    outer loop
      vertex   9.722287e+00 -1.096651e+01 1.175551e+01
      vertex   9.953440e+00 -1.090844e+01 1.177882e+01
      vertex   9.727888e+00 -1.090844e+01 1.181235e+01
    endloop
  endfacet
  facet normal 1.066506e-01 -6.884316e-01 7.174173e-01
    outer loop
      vertex   9.727888e+00 -1.090844e+01 1.181235e+01
      vertex   9.953440e+00 -1.090844e+01 1.177882e+01
      vertex   9.963547e+00 -1.085394e+01 1.182962e+01
    endloop
  endfacet
  facet normal 1.066506e-01 -6.884316e-01 7.174173e-01
    outer loop
      vertex   9.727888e+00 -1.090844e+01 1.181235e+01
      vertex   9.963547e+00 -1.085394e+01 1.182962e+01
      vertex   9.732968e+00 -1.085394e+01 1.186389e+01
    endloop
  endfacet
  facet normal 1.496734e-01 -7.873937e-01 5.980042e-01
    outer loop
      vertex   9.894095e+00 -1.119019e+01 1.148057e+01
      vertex   1.008629e+01 -1.119019e+01 1.143247e+01
      vertex   1.010046e+01 -1.115203e+01 1.147917e+01
    endloop
  endfacet
  facet normal 2.074947e-01 -7.874021e-01 5.804687e-01
    outer loop
      vertex   1.010046e+01 -1.115203e+01 1.147917e+01
      vertex   1.008629e+01 -1.119019e+01 1.143247e+01
      vertex   1.029152e+01 -1.115203e+01 1.141087e+01
    endloop
  endfacet
  facet normal 2.245958e-01 -7.448384e-01 6.283092e-01
    outer loop
      vertex   1.010046e+01 -1.115203e+01 1.147917e+01
      vertex   1.029152e+01 -1.115203e+01 1.141087e+01
      vertex   1.032429e+01 -1.107542e+01 1.148998e+01
    endloop
  endfacet
  facet normal 2.854964e-01 -7.448378e-01 6.030824e-01
    outer loop
      vertex   1.032429e+01 -1.107542e+01 1.148998e+01
      vertex   1.029152e+01 -1.115203e+01 1.141087e+01
      vertex   1.051531e+01 -1.107542e+01 1.139955e+01
    endloop
  endfacet
  facet normal 2.977040e-01 -7.182584e-01 6.288698e-01
    outer loop
      vertex   1.032429e+01 -1.107542e+01 1.148998e+01
      vertex   1.051531e+01 -1.107542e+01 1.139955e+01
      vertex   1.056837e+01 -1.096651e+01 1.149883e+01
    endloop
  endfacet
  facet normal 3.578873e-01 -7.182469e-01 5.966893e-01
    outer loop
      vertex   1.056837e+01 -1.096651e+01 1.149883e+01
      vertex   1.051531e+01 -1.107542e+01 1.139955e+01
      vertex   1.075911e+01 -1.096651e+01 1.138442e+01
    endloop
  endfacet
  facet normal 3.669253e-01 -7.007980e-01 6.117581e-01
    outer loop
      vertex   1.056837e+01 -1.096651e+01 1.149883e+01
      vertex   1.075911e+01 -1.096651e+01 1.138442e+01
      vertex   1.079084e+01 -1.090844e+01 1.143191e+01
    endloop
  endfacet
  facet normal 4.531672e-01 -6.995113e-01 5.525608e-01
    outer loop
      vertex   1.079084e+01 -1.090844e+01 1.143191e+01
      vertex   1.075911e+01 -1.096651e+01 1.138442e+01
      vertex   1.114306e+01 -1.090844e+01 1.114304e+01
    endloop
  endfacet
  facet normal 4.607261e-01 -6.871225e-01 5.617776e-01
    outer loop
      vertex   1.079084e+01 -1.090844e+01 1.143191e+01
      vertex   1.114306e+01 -1.090844e+01 1.114304e+01
      vertex   1.117968e+01 -1.085394e+01 1.117967e+01
    endloop
  endfacet
  facet normal 5.619131e-01 -6.871129e-01 4.605753e-01
    outer loop
      vertex   1.117968e+01 -1.085394e+01 1.117967e+01
      vertex   1.114306e+01 -1.090844e+01 1.114304e+01
      vertex   1.147484e+01 -1.085394e+01 1.081957e+01
    endloop
  endfacet
  facet normal 1.620087e-01 -7.448291e-01 6.472888e-01
    outer loop
      vertex   9.920328e+00 -1.107542e+01 1.161241e+01
      vertex   9.903618e+00 -1.115203e+01 1.152843e+01
      vertex   1.012532e+01 -1.107542e+01 1.156110e+01
    endloop
  endfacet
  facet normal 1.689359e-01 -7.182493e-01 6.749656e-01
    outer loop
      vertex   9.942294e+00 -1.096651e+01 1.172281e+01
      vertex   9.920328e+00 -1.107542e+01 1.161241e+01
      vertex   1.015800e+01 -1.096651e+01 1.166882e+01
    endloop
  endfacet
  facet normal 1.689359e-01 -7.182493e-01 6.749656e-01
    outer loop
      vertex   1.015800e+01 -1.096651e+01 1.166882e+01
      vertex   9.920328e+00 -1.107542e+01 1.161241e+01
      vertex   1.012532e+01 -1.107542e+01 1.156110e+01
    endloop
  endfacet
  facet normal 2.341994e-01 -7.182590e-01 6.551753e-01
    outer loop
      vertex   1.015800e+01 -1.096651e+01 1.166882e+01
      vertex   1.012532e+01 -1.107542e+01 1.156110e+01
      vertex   1.036737e+01 -1.096651e+01 1.159398e+01
    endloop
  endfacet
  facet normal 1.732022e-01 -7.008005e-01 6.920113e-01
    outer loop
      vertex   9.953440e+00 -1.090844e+01 1.177882e+01
      vertex   9.942294e+00 -1.096651e+01 1.172281e+01
      vertex   1.017458e+01 -1.090844e+01 1.172347e+01
    endloop
  endfacet
  facet normal 1.732022e-01 -7.008005e-01 6.920113e-01
    outer loop
      vertex   1.017458e+01 -1.090844e+01 1.172347e+01
      vertex   9.942294e+00 -1.096651e+01 1.172281e+01
      vertex   1.015800e+01 -1.096651e+01 1.166882e+01
    endloop
  endfacet
  facet normal 2.401141e-01 -7.008105e-01 6.717216e-01
    outer loop
      vertex   1.017458e+01 -1.090844e+01 1.172347e+01
      vertex   1.015800e+01 -1.096651e+01 1.166882e+01
      vertex   1.038922e+01 -1.090844e+01 1.164675e+01
    endloop
  endfacet
  facet normal 2.401141e-01 -7.008105e-01 6.717216e-01
    outer loop
      vertex   1.038922e+01 -1.090844e+01 1.164675e+01
      vertex   1.015800e+01 -1.096651e+01 1.166882e+01
      vertex   1.036737e+01 -1.096651e+01 1.159398e+01
    endloop
  endfacet
  facet normal 3.052224e-01 -7.008098e-01 6.447518e-01
    outer loop
      vertex   1.038922e+01 -1.090844e+01 1.164675e+01
      vertex   1.036737e+01 -1.096651e+01 1.159398e+01
      vertex   1.059529e+01 -1.090844e+01 1.154920e+01
    endloop
  endfacet
  facet normal 1.761022e-01 -6.884316e-01 7.035979e-01
    outer loop
      vertex   9.963547e+00 -1.085394e+01 1.182962e+01
      vertex   9.953440e+00 -1.090844e+01 1.177882e+01
      vertex   1.018961e+01 -1.085394e+01 1.177303e+01
    endloop
  endfacet
  facet normal 1.761022e-01 -6.884316e-01 7.035979e-01
    outer loop
      vertex   1.018961e+01 -1.085394e+01 1.177303e+01
      vertex   9.953440e+00 -1.090844e+01 1.177882e+01
      vertex   1.017458e+01 -1.090844e+01 1.172347e+01
    endloop
  endfacet
  facet normal 2.441345e-01 -6.884417e-01 6.829688e-01
    outer loop
      vertex   1.018961e+01 -1.085394e+01 1.177303e+01
      vertex   1.017458e+01 -1.090844e+01 1.172347e+01
      vertex   1.040905e+01 -1.085394e+01 1.169460e+01
    endloop
  endfacet
  facet normal 2.441345e-01 -6.884417e-01 6.829688e-01
    outer loop
      vertex   1.040905e+01 -1.085394e+01 1.169460e+01
      vertex   1.017458e+01 -1.090844e+01 1.172347e+01
      vertex   1.038922e+01 -1.090844e+01 1.164675e+01
    endloop
  endfacet
  facet normal 3.103330e-01 -6.884411e-01 6.555473e-01
    outer loop
      vertex   1.040905e+01 -1.085394e+01 1.169460e+01
      vertex   1.038922e+01 -1.090844e+01 1.164675e+01
      vertex   1.061970e+01 -1.085394e+01 1.159487e+01
    endloop
  endfacet
  facet normal 3.103330e-01 -6.884411e-01 6.555473e-01
    outer loop
      vertex   1.061970e+01 -1.085394e+01 1.159487e+01
      vertex   1.038922e+01 -1.090844e+01 1.164675e+01
      vertex   1.059529e+01 -1.090844e+01 1.154920e+01
    endloop
  endfacet
  facet normal 3.730688e-01 -6.884291e-01 6.220008e-01
    outer loop
      vertex   1.061970e+01 -1.085394e+01 1.159487e+01
      vertex   1.059529e+01 -1.090844e+01 1.154920e+01
      vertex   1.081961e+01 -1.085394e+01 1.147497e+01
    endloop
  endfacet
  facet normal 2.637582e-01 -7.874016e-01 5.571628e-01
    outer loop
      vertex   1.027284e+01 -1.119019e+01 1.136578e+01
      vertex   1.047494e+01 -1.115203e+01 1.132404e+01
      vertex   1.029152e+01 -1.115203e+01 1.141087e+01
    endloop
  endfacet
  facet normal 2.854964e-01 -7.448378e-01 6.030824e-01
    outer loop
      vertex   1.029152e+01 -1.115203e+01 1.141087e+01
      vertex   1.047494e+01 -1.115203e+01 1.132404e+01
      vertex   1.051531e+01 -1.107542e+01 1.139955e+01
    endloop
  endfacet
  facet normal 3.578873e-01 -7.182469e-01 5.966893e-01
    outer loop
      vertex   1.075911e+01 -1.096651e+01 1.138442e+01
      vertex   1.051531e+01 -1.107542e+01 1.139955e+01
      vertex   1.069657e+01 -1.107542e+01 1.129083e+01
    endloop
  endfacet
  facet normal 3.432122e-01 -7.448268e-01 5.722223e-01
    outer loop
      vertex   1.069657e+01 -1.107542e+01 1.129083e+01
      vertex   1.051531e+01 -1.107542e+01 1.139955e+01
      vertex   1.047494e+01 -1.115203e+01 1.132404e+01
    endloop
  endfacet
  facet normal 2.074947e-01 -7.874021e-01 5.804687e-01
    outer loop
      vertex   1.008629e+01 -1.119019e+01 1.143247e+01
      vertex   1.027284e+01 -1.119019e+01 1.136578e+01
      vertex   1.029152e+01 -1.115203e+01 1.141087e+01
    endloop
  endfacet
  facet normal 3.917885e-01 -7.863113e-01 4.777199e-01
    outer loop
      vertex   1.062189e+01 -1.119019e+01 1.117906e+01
      vertex   1.092802e+01 -1.119019e+01 1.092800e+01
      vertex   1.096253e+01 -1.115203e+01 1.096251e+01
    endloop
  endfacet
  facet normal 4.778369e-01 -7.863033e-01 3.916618e-01
    outer loop
      vertex   1.096253e+01 -1.115203e+01 1.096251e+01
      vertex   1.092802e+01 -1.119019e+01 1.092800e+01
      vertex   1.121952e+01 -1.115203e+01 1.064897e+01
    endloop
  endfacet
  facet normal 5.170951e-01 -7.436211e-01 4.238400e-01
    outer loop
      vertex   1.096253e+01 -1.115203e+01 1.096251e+01
      vertex   1.121952e+01 -1.115203e+01 1.064897e+01
      vertex   1.129071e+01 -1.107542e+01 1.069654e+01
    endloop
  endfacet
  facet normal 5.723464e-01 -7.448032e-01 3.430565e-01
    outer loop
      vertex   1.129071e+01 -1.107542e+01 1.069654e+01
      vertex   1.121952e+01 -1.115203e+01 1.064897e+01
      vertex   1.139937e+01 -1.107542e+01 1.051526e+01
    endloop
  endfacet
  facet normal 5.968171e-01 -7.182221e-01 3.577239e-01
    outer loop
      vertex   1.129071e+01 -1.107542e+01 1.069654e+01
      vertex   1.139937e+01 -1.107542e+01 1.051526e+01
      vertex   1.149863e+01 -1.096651e+01 1.056832e+01
    endloop
  endfacet
  facet normal 6.287810e-01 -7.182342e-01 2.979499e-01
    outer loop
      vertex   1.149863e+01 -1.096651e+01 1.056832e+01
      vertex   1.139937e+01 -1.107542e+01 1.051526e+01
      vertex   1.159387e+01 -1.096651e+01 1.036733e+01
    endloop
  endfacet
  facet normal 6.446596e-01 -7.007850e-01 3.054740e-01
    outer loop
      vertex   1.149863e+01 -1.096651e+01 1.056832e+01
      vertex   1.159387e+01 -1.096651e+01 1.036733e+01
      vertex   1.164663e+01 -1.090844e+01 1.038919e+01
    endloop
  endfacet
  facet normal 6.715249e-01 -7.008066e-01 2.406748e-01
    outer loop
      vertex   1.164663e+01 -1.090844e+01 1.038919e+01
      vertex   1.159387e+01 -1.096651e+01 1.036733e+01
      vertex   1.172357e+01 -1.090844e+01 1.017451e+01
    endloop
  endfacet
  facet normal 6.827686e-01 -6.884378e-01 2.447046e-01
    outer loop
      vertex   1.164663e+01 -1.090844e+01 1.038919e+01
      vertex   1.172357e+01 -1.090844e+01 1.017451e+01
      vertex   1.177314e+01 -1.085394e+01 1.018955e+01
    endloop
  endfacet
  facet normal 4.778369e-01 -7.863033e-01 3.916618e-01
    outer loop
      vertex   1.121952e+01 -1.115203e+01 1.064897e+01
      vertex   1.092802e+01 -1.119019e+01 1.092800e+01
      vertex   1.117895e+01 -1.119019e+01 1.062186e+01
    endloop
  endfacet
  facet normal 4.420442e-01 -7.169922e-01 5.389983e-01
    outer loop
      vertex   1.075911e+01 -1.096651e+01 1.138442e+01
      vertex   1.069657e+01 -1.107542e+01 1.129083e+01
      vertex   1.110267e+01 -1.096651e+01 1.110266e+01
    endloop
  endfacet
  facet normal 4.531672e-01 -6.995113e-01 5.525608e-01
    outer loop
      vertex   1.075911e+01 -1.096651e+01 1.138442e+01
      vertex   1.110267e+01 -1.096651e+01 1.110266e+01
      vertex   1.114306e+01 -1.090844e+01 1.114304e+01
    endloop
  endfacet
  facet normal 5.526943e-01 -6.995018e-01 4.530190e-01
    outer loop
      vertex   1.114306e+01 -1.090844e+01 1.114304e+01
      vertex   1.110267e+01 -1.096651e+01 1.110266e+01
      vertex   1.143178e+01 -1.090844e+01 1.079080e+01
    endloop
  endfacet
  facet normal 5.619131e-01 -6.871129e-01 4.605753e-01
    outer loop
      vertex   1.114306e+01 -1.090844e+01 1.114304e+01
      vertex   1.143178e+01 -1.090844e+01 1.079080e+01
      vertex   1.147484e+01 -1.085394e+01 1.081957e+01
    endloop
  endfacet
  facet normal 6.221322e-01 -6.884033e-01 3.728974e-01
    outer loop
      vertex   1.147484e+01 -1.085394e+01 1.081957e+01
      vertex   1.143178e+01 -1.090844e+01 1.079080e+01
      vertex   1.159467e+01 -1.085394e+01 1.061965e+01
    endloop
  endfacet
  facet normal 5.287706e-01 -7.873703e-01 3.169378e-01
    outer loop
      vertex   1.121952e+01 -1.115203e+01 1.064897e+01
      vertex   1.117895e+01 -1.119019e+01 1.062186e+01
      vertex   1.132386e+01 -1.115203e+01 1.047490e+01
    endloop
  endfacet
  facet normal 5.287706e-01 -7.873703e-01 3.169378e-01
    outer loop
      vertex   1.132386e+01 -1.115203e+01 1.047490e+01
      vertex   1.117895e+01 -1.119019e+01 1.062186e+01
      vertex   1.128082e+01 -1.119019e+01 1.045189e+01
    endloop
  endfacet
  facet normal 5.570882e-01 -7.873807e-01 2.639780e-01
    outer loop
      vertex   1.132386e+01 -1.115203e+01 1.047490e+01
      vertex   1.128082e+01 -1.119019e+01 1.045189e+01
      vertex   1.141077e+01 -1.115203e+01 1.029149e+01
    endloop
  endfacet
  facet normal 5.570882e-01 -7.873807e-01 2.639780e-01
    outer loop
      vertex   1.141077e+01 -1.115203e+01 1.029149e+01
      vertex   1.128082e+01 -1.119019e+01 1.045189e+01
      vertex   1.136568e+01 -1.119019e+01 1.027281e+01
    endloop
  endfacet
  facet normal 5.802995e-01 -7.873989e-01 2.079796e-01
    outer loop
      vertex   1.141077e+01 -1.115203e+01 1.029149e+01
      vertex   1.136568e+01 -1.119019e+01 1.027281e+01
      vertex   1.147925e+01 -1.115203e+01 1.010040e+01
    endloop
  endfacet
  facet normal 5.723464e-01 -7.448032e-01 3.430565e-01
    outer loop
      vertex   1.121952e+01 -1.115203e+01 1.064897e+01
      vertex   1.132386e+01 -1.115203e+01 1.047490e+01
      vertex   1.139937e+01 -1.107542e+01 1.051526e+01
    endloop
  endfacet
  facet normal 6.029989e-01 -7.448147e-01 2.857330e-01
    outer loop
      vertex   1.139937e+01 -1.107542e+01 1.051526e+01
      vertex   1.132386e+01 -1.115203e+01 1.047490e+01
      vertex   1.148987e+01 -1.107542e+01 1.032426e+01
    endloop
  endfacet
  facet normal 6.287810e-01 -7.182342e-01 2.979499e-01
    outer loop
      vertex   1.139937e+01 -1.107542e+01 1.051526e+01
      vertex   1.148987e+01 -1.107542e+01 1.032426e+01
      vertex   1.159387e+01 -1.096651e+01 1.036733e+01
    endloop
  endfacet
  facet normal 6.549836e-01 -7.182553e-01 2.347464e-01
    outer loop
      vertex   1.159387e+01 -1.096651e+01 1.036733e+01
      vertex   1.148987e+01 -1.107542e+01 1.032426e+01
      vertex   1.166892e+01 -1.096651e+01 1.015793e+01
    endloop
  endfacet
  facet normal 6.715249e-01 -7.008066e-01 2.406748e-01
    outer loop
      vertex   1.159387e+01 -1.096651e+01 1.036733e+01
      vertex   1.166892e+01 -1.096651e+01 1.015793e+01
      vertex   1.172357e+01 -1.090844e+01 1.017451e+01
    endloop
  endfacet
  facet normal 6.029989e-01 -7.448147e-01 2.857330e-01
    outer loop
      vertex   1.148987e+01 -1.107542e+01 1.032426e+01
      vertex   1.132386e+01 -1.115203e+01 1.047490e+01
      vertex   1.141077e+01 -1.115203e+01 1.029149e+01
    endloop
  endfacet
  facet normal 6.281256e-01 -7.448349e-01 2.251205e-01
    outer loop
      vertex   1.148987e+01 -1.107542e+01 1.032426e+01
      vertex   1.141077e+01 -1.115203e+01 1.029149e+01
      vertex   1.156120e+01 -1.107542e+01 1.012526e+01
    endloop
  endfacet
  facet normal 6.281256e-01 -7.448349e-01 2.251205e-01
    outer loop
      vertex   1.156120e+01 -1.107542e+01 1.012526e+01
      vertex   1.141077e+01 -1.115203e+01 1.029149e+01
      vertex   1.147925e+01 -1.115203e+01 1.010040e+01
    endloop
  endfacet
  facet normal 6.549836e-01 -7.182553e-01 2.347464e-01
    outer loop
      vertex   1.156120e+01 -1.107542e+01 1.012526e+01
      vertex   1.166892e+01 -1.096651e+01 1.015793e+01
      vertex   1.148987e+01 -1.107542e+01 1.032426e+01
    endloop
  endfacet
  facet normal 6.570945e-01 -7.451390e-01 1.139941e-01
    outer loop
      vertex   1.154589e+01 -1.115203e+01 9.803536e+00
      vertex   1.163059e+01 -1.107542e+01 9.816102e+00
      vertex   1.152854e+01 -1.115203e+01 9.903527e+00
    endloop
  endfacet
  facet normal 6.570945e-01 -7.451390e-01 1.139941e-01
    outer loop
      vertex   1.152854e+01 -1.115203e+01 9.903527e+00
      vertex   1.163059e+01 -1.107542e+01 9.816102e+00
      vertex   1.161253e+01 -1.107542e+01 9.920233e+00
    endloop
  endfacet
  facet normal 6.507218e-01 -7.451405e-01 1.460365e-01
    outer loop
      vertex   1.152854e+01 -1.115203e+01 9.903527e+00
      vertex   1.161253e+01 -1.107542e+01 9.920233e+00
      vertex   1.150632e+01 -1.115203e+01 1.000256e+01
    endloop
  endfacet
  facet normal 6.507218e-01 -7.451405e-01 1.460365e-01
    outer loop
      vertex   1.150632e+01 -1.115203e+01 1.000256e+01
      vertex   1.161253e+01 -1.107542e+01 9.920233e+00
      vertex   1.158938e+01 -1.107542e+01 1.002336e+01
    endloop
  endfacet
  facet normal 6.852155e-01 -7.185743e-01 1.188726e-01
    outer loop
      vertex   1.163059e+01 -1.107542e+01 9.816102e+00
      vertex   1.174194e+01 -1.096651e+01 9.832622e+00
      vertex   1.161253e+01 -1.107542e+01 9.920233e+00
    endloop
  endfacet
  facet normal 6.852155e-01 -7.185743e-01 1.188726e-01
    outer loop
      vertex   1.161253e+01 -1.107542e+01 9.920233e+00
      vertex   1.174194e+01 -1.096651e+01 9.832622e+00
      vertex   1.172293e+01 -1.096651e+01 9.942195e+00
    endloop
  endfacet
  facet normal 6.785703e-01 -7.185758e-01 1.522863e-01
    outer loop
      vertex   1.161253e+01 -1.107542e+01 9.920233e+00
      vertex   1.172293e+01 -1.096651e+01 9.942195e+00
      vertex   1.158938e+01 -1.107542e+01 1.002336e+01
    endloop
  endfacet
  facet normal 6.785703e-01 -7.185758e-01 1.522863e-01
    outer loop
      vertex   1.158938e+01 -1.107542e+01 1.002336e+01
      vertex   1.172293e+01 -1.096651e+01 9.942195e+00
      vertex   1.169858e+01 -1.096651e+01 1.005071e+01
    endloop
  endfacet
  facet normal 6.618857e-01 -7.451391e-01 8.170052e-02
    outer loop
      vertex   1.154589e+01 -1.115203e+01 9.803536e+00
      vertex   1.164354e+01 -1.107542e+01 9.711199e+00
      vertex   1.163059e+01 -1.107542e+01 9.816102e+00
    endloop
  endfacet
  facet normal 6.902119e-01 -7.185743e-01 8.519698e-02
    outer loop
      vertex   1.163059e+01 -1.107542e+01 9.816102e+00
      vertex   1.164354e+01 -1.107542e+01 9.711199e+00
      vertex   1.175556e+01 -1.096651e+01 9.722237e+00
    endloop
  endfacet
  facet normal 6.902119e-01 -7.185743e-01 8.519698e-02
    outer loop
      vertex   1.163059e+01 -1.107542e+01 9.816102e+00
      vertex   1.175556e+01 -1.096651e+01 9.722237e+00
      vertex   1.174194e+01 -1.096651e+01 9.832622e+00
    endloop
  endfacet
  facet normal 7.076590e-01 -7.011338e-01 8.735058e-02
    outer loop
      vertex   1.174194e+01 -1.096651e+01 9.832622e+00
      vertex   1.175556e+01 -1.096651e+01 9.722237e+00
      vertex   1.181240e+01 -1.090844e+01 9.727837e+00
    endloop
  endfacet
  facet normal 7.076590e-01 -7.011338e-01 8.735058e-02
    outer loop
      vertex   1.174194e+01 -1.096651e+01 9.832622e+00
      vertex   1.181240e+01 -1.090844e+01 9.727837e+00
      vertex   1.179843e+01 -1.090844e+01 9.841004e+00
    endloop
  endfacet
  facet normal 7.195190e-01 -6.887701e-01 8.881454e-02
    outer loop
      vertex   1.179843e+01 -1.090844e+01 9.841004e+00
      vertex   1.181240e+01 -1.090844e+01 9.727837e+00
      vertex   1.186395e+01 -1.085394e+01 9.732915e+00
    endloop
  endfacet
  facet normal 7.195190e-01 -6.887701e-01 8.881454e-02
    outer loop
      vertex   1.179843e+01 -1.090844e+01 9.841004e+00
      vertex   1.186395e+01 -1.085394e+01 9.732915e+00
      vertex   1.184967e+01 -1.085394e+01 9.848605e+00
    endloop
  endfacet
  facet normal 7.397328e-01 -6.666768e-01 9.130964e-02
    outer loop
      vertex   1.184967e+01 -1.085394e+01 9.848605e+00
      vertex   1.186395e+01 -1.085394e+01 9.732915e+00
      vertex   1.194019e+01 -1.076831e+01 9.740428e+00
    endloop
  endfacet
  facet normal 7.397328e-01 -6.666768e-01 9.130964e-02
    outer loop
      vertex   1.184967e+01 -1.085394e+01 9.848605e+00
      vertex   1.194019e+01 -1.076831e+01 9.740428e+00
      vertex   1.192545e+01 -1.076831e+01 9.859848e+00
    endloop
  endfacet
  facet normal 7.025364e-01 -7.011338e-01 1.218774e-01
    outer loop
      vertex   1.174194e+01 -1.096651e+01 9.832622e+00
      vertex   1.179843e+01 -1.090844e+01 9.841004e+00
      vertex   1.172293e+01 -1.096651e+01 9.942195e+00
    endloop
  endfacet
  facet normal 7.025364e-01 -7.011338e-01 1.218774e-01
    outer loop
      vertex   1.172293e+01 -1.096651e+01 9.942195e+00
      vertex   1.179843e+01 -1.090844e+01 9.841004e+00
      vertex   1.177895e+01 -1.090844e+01 9.953338e+00
    endloop
  endfacet
  facet normal 6.957232e-01 -7.011354e-01 1.561358e-01
    outer loop
      vertex   1.172293e+01 -1.096651e+01 9.942195e+00
      vertex   1.177895e+01 -1.090844e+01 9.953338e+00
      vertex   1.169858e+01 -1.096651e+01 1.005071e+01
    endloop
  endfacet
  facet normal 6.957232e-01 -7.011354e-01 1.561358e-01
    outer loop
      vertex   1.169858e+01 -1.096651e+01 1.005071e+01
      vertex   1.177895e+01 -1.090844e+01 9.953338e+00
      vertex   1.175398e+01 -1.090844e+01 1.006459e+01
    endloop
  endfacet
  facet normal 7.143106e-01 -6.887701e-01 1.239201e-01
    outer loop
      vertex   1.179843e+01 -1.090844e+01 9.841004e+00
      vertex   1.184967e+01 -1.085394e+01 9.848605e+00
      vertex   1.177895e+01 -1.090844e+01 9.953338e+00
    endloop
  endfacet
  facet normal 7.143106e-01 -6.887701e-01 1.239201e-01
    outer loop
      vertex   1.177895e+01 -1.090844e+01 9.953338e+00
      vertex   1.184967e+01 -1.085394e+01 9.848605e+00
      vertex   1.182974e+01 -1.085394e+01 9.963443e+00
    endloop
  endfacet
  facet normal 7.073833e-01 -6.887717e-01 1.587526e-01
    outer loop
      vertex   1.177895e+01 -1.090844e+01 9.953338e+00
      vertex   1.182974e+01 -1.085394e+01 9.963443e+00
      vertex   1.175398e+01 -1.090844e+01 1.006459e+01
    endloop
  endfacet
  facet normal 7.073833e-01 -6.887717e-01 1.587526e-01
    outer loop
      vertex   1.175398e+01 -1.090844e+01 1.006459e+01
      vertex   1.182974e+01 -1.085394e+01 9.963443e+00
      vertex   1.180422e+01 -1.085394e+01 1.007718e+01
    endloop
  endfacet
  facet normal 7.343780e-01 -6.666767e-01 1.274014e-01
    outer loop
      vertex   1.184967e+01 -1.085394e+01 9.848605e+00
      vertex   1.192545e+01 -1.076831e+01 9.859848e+00
      vertex   1.182974e+01 -1.085394e+01 9.963443e+00
    endloop
  endfacet
  facet normal 7.343780e-01 -6.666767e-01 1.274014e-01
    outer loop
      vertex   1.182974e+01 -1.085394e+01 9.963443e+00
      vertex   1.192545e+01 -1.076831e+01 9.859848e+00
      vertex   1.190489e+01 -1.076831e+01 9.978390e+00
    endloop
  endfacet
  facet normal 7.272562e-01 -6.666784e-01 1.632126e-01
    outer loop
      vertex   1.182974e+01 -1.085394e+01 9.963443e+00
      vertex   1.190489e+01 -1.076831e+01 9.978390e+00
      vertex   1.180422e+01 -1.085394e+01 1.007718e+01
    endloop
  endfacet
  facet normal 7.272562e-01 -6.666784e-01 1.632126e-01
    outer loop
      vertex   1.180422e+01 -1.085394e+01 1.007718e+01
      vertex   1.190489e+01 -1.076831e+01 9.978390e+00
      vertex   1.187854e+01 -1.076831e+01 1.009579e+01
    endloop
  endfacet
  facet normal 6.011391e-01 -7.876747e-01 1.349090e-01
    outer loop
      vertex   1.145898e+01 -1.119019e+01 9.990698e+00
      vertex   1.148068e+01 -1.119019e+01 9.894006e+00
      vertex   1.152854e+01 -1.115203e+01 9.903527e+00
    endloop
  endfacet
  facet normal 6.070263e-01 -7.876733e-01 1.053082e-01
    outer loop
      vertex   1.152854e+01 -1.115203e+01 9.903527e+00
      vertex   1.148068e+01 -1.119019e+01 9.894006e+00
      vertex   1.154589e+01 -1.115203e+01 9.803536e+00
    endloop
  endfacet
  facet normal 6.011391e-01 -7.876747e-01 1.349090e-01
    outer loop
      vertex   1.145898e+01 -1.119019e+01 9.990698e+00
      vertex   1.152854e+01 -1.115203e+01 9.903527e+00
      vertex   1.150632e+01 -1.115203e+01 1.000256e+01
    endloop
  endfacet
  facet normal 7.433165e-01 -6.666785e-01 5.495788e-02
    outer loop
      vertex   1.194019e+01 -1.076831e+01 9.740428e+00
      vertex   1.186395e+01 -1.085394e+01 9.732915e+00
      vertex   1.194907e+01 -1.076831e+01 9.620391e+00
    endloop
  endfacet
  facet normal 7.433165e-01 -6.666785e-01 5.495788e-02
    outer loop
      vertex   1.194907e+01 -1.076831e+01 9.620391e+00
      vertex   1.186395e+01 -1.085394e+01 9.732915e+00
      vertex   1.187254e+01 -1.085394e+01 9.616629e+00
    endloop
  endfacet
  facet normal 7.230047e-01 -6.887719e-01 5.345611e-02
    outer loop
      vertex   1.186395e+01 -1.085394e+01 9.732915e+00
      vertex   1.181240e+01 -1.090844e+01 9.727837e+00
      vertex   1.187254e+01 -1.085394e+01 9.616629e+00
    endloop
  endfacet
  facet normal 7.230047e-01 -6.887719e-01 5.345611e-02
    outer loop
      vertex   1.187254e+01 -1.085394e+01 9.616629e+00
      vertex   1.181240e+01 -1.090844e+01 9.727837e+00
      vertex   1.182081e+01 -1.090844e+01 9.614086e+00
    endloop
  endfacet
  facet normal 7.110871e-01 -7.011355e-01 5.257497e-02
    outer loop
      vertex   1.181240e+01 -1.090844e+01 9.727837e+00
      vertex   1.175556e+01 -1.096651e+01 9.722237e+00
      vertex   1.182081e+01 -1.090844e+01 9.614086e+00
    endloop
  endfacet
  facet normal 7.110871e-01 -7.011355e-01 5.257497e-02
    outer loop
      vertex   1.182081e+01 -1.090844e+01 9.614086e+00
      vertex   1.175556e+01 -1.096651e+01 9.722237e+00
      vertex   1.176377e+01 -1.096651e+01 9.611282e+00
    endloop
  endfacet
  facet normal 6.935554e-01 -7.185760e-01 5.127874e-02
    outer loop
      vertex   1.175556e+01 -1.096651e+01 9.722237e+00
      vertex   1.164354e+01 -1.107542e+01 9.711199e+00
      vertex   1.176377e+01 -1.096651e+01 9.611282e+00
    endloop
  endfacet
  facet normal 6.144142e-01 -7.876748e-01 4.542735e-02
    outer loop
      vertex   1.150976e+01 -1.119019e+01 9.698018e+00
      vertex   1.151707e+01 -1.119019e+01 9.599155e+00
      vertex   1.156581e+01 -1.115203e+01 9.601551e+00
    endloop
  endfacet
  facet normal 6.144142e-01 -7.876748e-01 4.542735e-02
    outer loop
      vertex   1.150976e+01 -1.119019e+01 9.698018e+00
      vertex   1.156581e+01 -1.115203e+01 9.601551e+00
      vertex   1.155833e+01 -1.115203e+01 9.702803e+00
    endloop
  endfacet
  facet normal 6.650919e-01 -7.451407e-01 4.917427e-02
    outer loop
      vertex   1.155833e+01 -1.115203e+01 9.702803e+00
      vertex   1.156581e+01 -1.115203e+01 9.601551e+00
      vertex   1.165134e+01 -1.107542e+01 9.605755e+00
    endloop
  endfacet
  facet normal 6.114525e-01 -7.876734e-01 7.547524e-02
    outer loop
      vertex   1.150976e+01 -1.119019e+01 9.698018e+00
      vertex   1.155833e+01 -1.115203e+01 9.702803e+00
      vertex   1.149762e+01 -1.119019e+01 9.796374e+00
    endloop
  endfacet
  facet normal -9.805673e-02 -3.230226e-16 -9.951808e-01
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -9.801714e-02 -2.780680e-06 -9.951847e-01
    outer loop
      vertex   -9.500000e+00 -3.690000e+00 -1.200000e+01
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
      vertex   -9.987726e+00 -3.690000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal -2.918287e-01 -5.561598e-06 -9.564706e-01
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   -9.987623e+00 -1.070000e+01 -1.195195e+01
      vertex   -1.045619e+01 -1.070000e+01 -1.180899e+01
    endloop
  endfacet
  facet normal -2.902847e-01 -1.183264e-04 -9.569403e-01
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   -1.045619e+01 -1.070000e+01 -1.180899e+01
      vertex   -1.045671e+01 -3.690000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal -4.712109e-01 -1.242687e-04 -8.820205e-01
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   -1.045619e+01 -1.070000e+01 -1.180899e+01
      vertex   -1.088849e+01 -1.070000e+01 -1.157804e+01
    endloop
  endfacet
  facet normal -4.713967e-01 -1.095428e-04 -8.819213e-01
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   -1.088849e+01 -1.070000e+01 -1.157804e+01
      vertex   -1.088893e+01 -3.690000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal -6.331815e-01 -1.097415e-04 -7.740033e-01
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   -1.088849e+01 -1.070000e+01 -1.157804e+01
      vertex   -1.126777e+01 -1.070000e+01 -1.126777e+01
    endloop
  endfacet
  facet normal -6.343933e-01 -2.159878e-07 -7.730105e-01
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   -1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   -1.126777e+01 -3.690000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal -7.730105e-01 -2.075670e-07 -6.343933e-01
    outer loop
      vertex   -1.126777e+01 -3.690000e+00 -1.126777e+01
      vertex   -1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   -1.157867e+01 -3.690000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal -7.733944e-01 -4.253863e-05 -6.339251e-01
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   -1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   -1.157840e+01 -1.070000e+01 -1.088879e+01
    endloop
  endfacet
  facet normal -8.817475e-01 -4.357923e-05 -4.717217e-01
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   -1.157840e+01 -1.070000e+01 -1.088879e+01
      vertex   -1.180957e+01 -1.070000e+01 -1.045669e+01
    endloop
  endfacet
  facet normal -8.819213e-01 -1.781517e-05 -4.713967e-01
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   -1.180957e+01 -1.070000e+01 -1.045669e+01
      vertex   -1.180970e+01 -3.690000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal -9.568779e-01 -1.867045e-05 -2.904903e-01
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   -1.180957e+01 -1.070000e+01 -1.045669e+01
      vertex   -1.195193e+01 -1.070000e+01 -9.987751e+00
    endloop
  endfacet
  facet normal -9.569403e-01 -3.648353e-06 -2.902847e-01
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   -1.195193e+01 -1.070000e+01 -9.987751e+00
      vertex   -1.195196e+01 -3.690000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal -9.951784e-01 -4.540031e-06 -9.808177e-02
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   -1.195193e+01 -1.070000e+01 -9.987751e+00
      vertex   -1.200000e+01 -1.070000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal -9.951847e-01 1.242154e-16 -9.801714e-02
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   -1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   -1.200000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 1.184565e-31 -9.349247e-17
    outer loop
      vertex   -1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   -1.200000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 1.520420e-15 4.674623e-16
    outer loop
      vertex   -1.200000e+01 -3.690000e+00 -9.500000e+00
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   -1.200000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -9.951808e-01 1.190070e-15 9.805673e-02
    outer loop
      vertex   -1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
      vertex   -1.200000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -9.951847e-01 -2.780681e-06 9.801714e-02
    outer loop
      vertex   -1.200000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
      vertex   -1.195196e+01 -3.690000e+00 9.987726e+00
    endloop
  endfacet
  facet normal -9.564706e-01 -5.561599e-06 2.918287e-01
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   -1.195195e+01 -1.070000e+01 9.987623e+00
      vertex   -1.180899e+01 -1.070000e+01 1.045619e+01
    endloop
  endfacet
  facet normal -9.569403e-01 -1.183264e-04 2.902847e-01
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   -1.180899e+01 -1.070000e+01 1.045619e+01
      vertex   -1.180970e+01 -3.690000e+00 1.045671e+01
    endloop
  endfacet
  facet normal -8.820205e-01 -1.242687e-04 4.712109e-01
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   -1.180899e+01 -1.070000e+01 1.045619e+01
      vertex   -1.157804e+01 -1.070000e+01 1.088849e+01
    endloop
  endfacet
  facet normal -8.819213e-01 -1.095428e-04 4.713967e-01
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   -1.157804e+01 -1.070000e+01 1.088849e+01
      vertex   -1.157867e+01 -3.690000e+00 1.088893e+01
    endloop
  endfacet
  facet normal -7.740033e-01 -1.097415e-04 6.331815e-01
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   -1.157804e+01 -1.070000e+01 1.088849e+01
      vertex   -1.126777e+01 -1.070000e+01 1.126777e+01
    endloop
  endfacet
  facet normal -7.730105e-01 -2.159890e-07 6.343933e-01
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   -1.126777e+01 -1.070000e+01 1.126777e+01
      vertex   -1.126777e+01 -3.690000e+00 1.126777e+01
    endloop
  endfacet
  facet normal -6.343933e-01 -2.075655e-07 7.730105e-01
    outer loop
      vertex   -1.126777e+01 -3.690000e+00 1.126777e+01
      vertex   -1.126777e+01 -1.070000e+01 1.126777e+01
      vertex   -1.088893e+01 -3.690000e+00 1.157867e+01
    endloop
  endfacet
  facet normal -6.339251e-01 -4.253864e-05 7.733944e-01
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   -1.126777e+01 -1.070000e+01 1.126777e+01
      vertex   -1.088879e+01 -1.070000e+01 1.157840e+01
    endloop
  endfacet
  facet normal -4.717217e-01 -4.357923e-05 8.817475e-01
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   -1.088879e+01 -1.070000e+01 1.157840e+01
      vertex   -1.045669e+01 -1.070000e+01 1.180957e+01
    endloop
  endfacet
  facet normal -4.713967e-01 -1.781517e-05 8.819213e-01
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   -1.045669e+01 -1.070000e+01 1.180957e+01
      vertex   -1.045671e+01 -3.690000e+00 1.180970e+01
    endloop
  endfacet
  facet normal -2.904903e-01 -1.867045e-05 9.568779e-01
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   -1.045669e+01 -1.070000e+01 1.180957e+01
      vertex   -9.987751e+00 -1.070000e+01 1.195193e+01
    endloop
  endfacet
  facet normal -2.902847e-01 -3.648358e-06 9.569403e-01
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   -9.987751e+00 -1.070000e+01 1.195193e+01
      vertex   -9.987726e+00 -3.690000e+00 1.195196e+01
    endloop
  endfacet
  facet normal -9.808177e-02 -4.540038e-06 9.951784e-01
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   -9.987751e+00 -1.070000e+01 1.195193e+01
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal -9.801714e-02 -1.216907e-15 9.951847e-01
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 3.982756e-30 1.064995e-14 1.000000e+00
    outer loop
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal 1.184238e-14 0.000000e+00 1.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   -8.750000e+00 -7.933974e+00 1.200000e+01
    endloop
  endfacet
  facet normal 1.184238e-14 1.470440e-28 1.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   -8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -2.092799e-15 1.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.690000e+00 1.200000e+01
      vertex   -8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -2.092799e-15 1.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.690000e+00 1.200000e+01
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   9.500000e+00 -3.690000e+00 1.200000e+01
    endloop
  endfacet
  facet normal -1.184238e-14 -3.000897e-30 1.000000e+00
    outer loop
      vertex   9.500000e+00 -3.690000e+00 1.200000e+01
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal -1.184238e-14 0.000000e+00 1.000000e+00
    outer loop
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   8.750000e+00 -9.866026e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.064995e-14 1.000000e+00
    outer loop
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.064995e-14 1.000000e+00
    outer loop
      vertex   1.154595e-05 -1.070000e+01 1.200000e+01
      vertex   8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   1.146154e+01 -1.120000e+01 9.890199e+00
      vertex   1.134766e+01 -1.120000e+01 1.026535e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   -1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   -1.150000e+01 -1.120000e+01 9.500000e+00
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -9.500000e+00 -1.120000e+01 -1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -9.890099e+00 -1.120000e+01 -1.146156e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.890099e+00 -1.120000e+01 -1.146156e+01
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.026495e+01 -1.120000e+01 -1.134719e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.026495e+01 -1.120000e+01 -1.134719e+01
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.061079e+01 -1.120000e+01 -1.116243e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.061079e+01 -1.120000e+01 -1.116243e+01
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.091421e+01 -1.120000e+01 -1.091421e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.091421e+01 -1.120000e+01 -1.091421e+01
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.116272e+01 -1.120000e+01 -1.061103e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.116272e+01 -1.120000e+01 -1.061103e+01
      vertex   -1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   -1.146154e+01 -1.120000e+01 -9.890201e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.116272e+01 -1.120000e+01 -1.061103e+01
      vertex   -1.146154e+01 -1.120000e+01 -9.890201e+00
      vertex   -1.134765e+01 -1.120000e+01 -1.026535e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.890201e+00 -1.120000e+01 1.146154e+01
      vertex   -1.061103e+01 -1.120000e+01 1.116272e+01
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 6.892750e-15 -1.000000e+00 -2.270539e-14
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   -1.061103e+01 -1.120000e+01 1.116272e+01
      vertex   -1.091421e+01 -1.120000e+01 1.091421e+01
    endloop
  endfacet
  facet normal -1.113540e-14 -1.000000e+00 2.081833e-14
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   -1.091421e+01 -1.120000e+01 1.091421e+01
      vertex   -1.116243e+01 -1.120000e+01 1.061079e+01
    endloop
  endfacet
  facet normal -3.537725e-14 -1.000000e+00 8.533827e-14
    outer loop
      vertex   -9.890201e+00 -1.120000e+01 1.146154e+01
      vertex   -1.026535e+01 -1.120000e+01 1.134765e+01
      vertex   -1.061103e+01 -1.120000e+01 1.116272e+01
    endloop
  endfacet
  facet normal 7.692950e-15 -1.000000e+00 -1.438245e-14
    outer loop
      vertex   -1.116243e+01 -1.120000e+01 1.061079e+01
      vertex   -1.134719e+01 -1.120000e+01 1.026495e+01
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal -1.037713e-14 -1.000000e+00 1.264387e-14
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   -1.134719e+01 -1.120000e+01 1.026495e+01
      vertex   -1.146156e+01 -1.120000e+01 9.890099e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   -1.146156e+01 -1.120000e+01 9.890099e+00
      vertex   -1.150000e+01 -1.120000e+01 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.154595e-05 -1.120000e+01 1.150000e+01
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   1.150000e+01 -1.120000e+01 9.500000e+00
    endloop
  endfacet
  facet normal -5.050139e-15 -1.000000e+00 5.050139e-15
    outer loop
      vertex   9.500000e+00 -1.120000e+01 -1.150000e+01
      vertex   9.890201e+00 -1.120000e+01 -1.146154e+01
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 5.940080e-15 -1.000000e+00 -3.969312e-15
    outer loop
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   9.890201e+00 -1.120000e+01 -1.146154e+01
      vertex   1.026535e+01 -1.120000e+01 -1.134765e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   1.026535e+01 -1.120000e+01 -1.134765e+01
      vertex   1.061103e+01 -1.120000e+01 -1.116272e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.061103e+01 -1.120000e+01 -1.116272e+01
      vertex   1.091421e+01 -1.120000e+01 -1.091421e+01
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 2.899347e-14 -1.000000e+00 -1.200952e-14
    outer loop
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   1.091421e+01 -1.120000e+01 -1.091421e+01
      vertex   1.116243e+01 -1.120000e+01 -1.061079e+01
    endloop
  endfacet
  facet normal -3.071218e-14 -1.000000e+00 6.135118e-15
    outer loop
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
      vertex   1.116243e+01 -1.120000e+01 -1.061079e+01
      vertex   1.134719e+01 -1.120000e+01 -1.026495e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.134719e+01 -1.120000e+01 -1.026495e+01
      vertex   1.146156e+01 -1.120000e+01 -9.890099e+00
      vertex   1.150000e+01 -1.120000e+01 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   1.134766e+01 -1.120000e+01 1.026535e+01
      vertex   1.116273e+01 -1.120000e+01 1.061102e+01
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   1.116273e+01 -1.120000e+01 1.061102e+01
      vertex   1.091422e+01 -1.120000e+01 1.091421e+01
    endloop
  endfacet
  facet normal -5.979336e-15 -1.000000e+00 -1.443528e-14
    outer loop
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
      vertex   1.091422e+01 -1.120000e+01 1.091421e+01
      vertex   1.061105e+01 -1.120000e+01 1.116284e+01
    endloop
  endfacet
  facet normal 6.717135e-15 -1.000000e+00 2.216319e-14
    outer loop
      vertex   1.026538e+01 -1.120000e+01 1.134775e+01
      vertex   9.890287e+00 -1.120000e+01 1.146144e+01
      vertex   1.061105e+01 -1.120000e+01 1.116284e+01
    endloop
  endfacet
  facet normal 7.719414e-16 -1.000000e+00 7.812372e-15
    outer loop
      vertex   1.061105e+01 -1.120000e+01 1.116284e+01
      vertex   9.890287e+00 -1.120000e+01 1.146144e+01
      vertex   9.500000e+00 -1.120000e+01 1.150000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   8.750000e+00 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 1.000000e+00 -0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -9.707107e+00 1.220711e+01
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   8.750000e+00 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -9.707107e+00 1.220711e+01
      vertex   8.750000e+00 -8.092893e+00 1.220711e+01
      vertex   8.750000e+00 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 1.000000e+00 -0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   8.750000e+00 -8.092893e+00 1.220711e+01
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   8.750000e+00 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 1.000000e+00 -0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -9.258820e+00 1.246593e+01
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   8.750000e+00 -9.000001e+00 1.250000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   8.750000e+00 -8.800000e+00 1.250000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   8.750000e+00 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 8.881752e-15 1.000000e+00
    outer loop
      vertex   8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   -8.750000e+00 -9.000001e+00 1.250000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 8.881752e-15 1.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   -8.750000e+00 -8.800000e+00 1.250000e+01
    endloop
  endfacet
  facet normal 4.025508e-16 1.305262e-01 9.914449e-01
    outer loop
      vertex   8.750000e+00 -8.541181e+00 1.246593e+01
      vertex   4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   8.750000e+00 -8.800000e+00 1.250000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.305262e-01 9.914449e-01
    outer loop
      vertex   8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   1.110223e-14 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.305262e-01 9.914449e-01
    outer loop
      vertex   8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   1.110223e-14 -8.541181e+00 1.246593e+01
      vertex   -8.750000e+00 -8.800000e+00 1.250000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.305262e-01 9.914449e-01
    outer loop
      vertex   -8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   1.110223e-14 -8.541181e+00 1.246593e+01
      vertex   -4.375000e+00 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal -4.025042e-16 1.305262e-01 9.914449e-01
    outer loop
      vertex   -8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   -4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   -8.750000e+00 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal -3.751177e-16 3.826834e-01 9.238795e-01
    outer loop
      vertex   -8.750000e+00 -8.541181e+00 1.246593e+01
      vertex   -4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   -8.750000e+00 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal -0.000000e+00 3.826834e-01 9.238795e-01
    outer loop
      vertex   -8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   -4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   -4.375000e+00 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal -0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   -8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   -4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   -8.750000e+00 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal -0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   -8.750000e+00 -8.092893e+00 1.220711e+01
      vertex   -4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   -4.375000e+00 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal -0.000000e+00 7.933533e-01 6.087614e-01
    outer loop
      vertex   -8.750000e+00 -8.092893e+00 1.220711e+01
      vertex   -4.375000e+00 -8.092893e+00 1.220711e+01
      vertex   -8.750000e+00 -7.933974e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 7.933533e-01 6.087614e-01
    outer loop
      vertex   -8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   -4.375000e+00 -8.092893e+00 1.220711e+01
      vertex   1.110223e-14 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal -0.000000e+00 7.933533e-01 6.087614e-01
    outer loop
      vertex   -8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   1.110223e-14 -8.092893e+00 1.220711e+01
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 7.933533e-01 6.087614e-01
    outer loop
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   1.110223e-14 -8.092893e+00 1.220711e+01
      vertex   4.375000e+00 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 7.933533e-01 6.087614e-01
    outer loop
      vertex   8.750000e+00 -7.933974e+00 1.200000e+01
      vertex   4.375000e+00 -8.092893e+00 1.220711e+01
      vertex   8.750000e+00 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   8.750000e+00 -8.092893e+00 1.220711e+01
      vertex   4.375000e+00 -8.092893e+00 1.220711e+01
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   4.375000e+00 -8.092893e+00 1.220711e+01
      vertex   4.375000e+00 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 3.826834e-01 9.238795e-01
    outer loop
      vertex   8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   8.750000e+00 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal 3.751177e-16 3.826834e-01 9.238795e-01
    outer loop
      vertex   8.750000e+00 -8.541181e+00 1.246593e+01
      vertex   4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   4.375000e+00 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 3.826834e-01 9.238795e-01
    outer loop
      vertex   -4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   -4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   1.110223e-14 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal -0.000000e+00 3.826834e-01 9.238795e-01
    outer loop
      vertex   1.110223e-14 -8.541181e+00 1.246593e+01
      vertex   4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   1.110223e-14 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal -0.000000e+00 3.826834e-01 9.238795e-01
    outer loop
      vertex   1.110223e-14 -8.300000e+00 1.236603e+01
      vertex   4.375000e+00 -8.541181e+00 1.246593e+01
      vertex   4.375000e+00 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal -0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   1.110223e-14 -8.300000e+00 1.236603e+01
      vertex   4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   1.110223e-14 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal -0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   1.110223e-14 -8.092893e+00 1.220711e+01
      vertex   4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   4.375000e+00 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   -4.375000e+00 -8.092893e+00 1.220711e+01
      vertex   -4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   1.110223e-14 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 3.826834e-01 9.238795e-01
    outer loop
      vertex   1.110223e-14 -8.300000e+00 1.236603e+01
      vertex   -4.375000e+00 -8.300000e+00 1.236603e+01
      vertex   1.110223e-14 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal -0.000000e+00 6.087614e-01 7.933533e-01
    outer loop
      vertex   -4.375000e+00 -8.092893e+00 1.220711e+01
      vertex   1.110223e-14 -8.300000e+00 1.236603e+01
      vertex   1.110223e-14 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.933533e-01 6.087614e-01
    outer loop
      vertex   8.750000e+00 -9.707107e+00 1.220711e+01
      vertex   4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   8.750000e+00 -9.866026e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.933533e-01 6.087614e-01
    outer loop
      vertex   8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   1.110223e-14 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.933533e-01 6.087614e-01
    outer loop
      vertex   8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   1.110223e-14 -9.707107e+00 1.220711e+01
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.933533e-01 6.087614e-01
    outer loop
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   1.110223e-14 -9.707107e+00 1.220711e+01
      vertex   -4.375000e+00 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -7.933533e-01 6.087614e-01
    outer loop
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   -4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   -8.750000e+00 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   -8.750000e+00 -9.707107e+00 1.220711e+01
      vertex   -4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   -4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   -4.375000e+00 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   -4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   -8.750000e+00 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   -8.750000e+00 -9.258820e+00 1.246593e+01
      vertex   -4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   -4.375000e+00 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.305262e-01 9.914449e-01
    outer loop
      vertex   -8.750000e+00 -9.258820e+00 1.246593e+01
      vertex   -4.375000e+00 -9.258820e+00 1.246593e+01
      vertex   -8.750000e+00 -9.000001e+00 1.250000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.305262e-01 9.914449e-01
    outer loop
      vertex   -8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   -4.375000e+00 -9.258820e+00 1.246593e+01
      vertex   1.110223e-14 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.305262e-01 9.914449e-01
    outer loop
      vertex   -8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   1.110223e-14 -9.258820e+00 1.246593e+01
      vertex   8.750000e+00 -9.000001e+00 1.250000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.305262e-01 9.914449e-01
    outer loop
      vertex   8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   1.110223e-14 -9.258820e+00 1.246593e+01
      vertex   4.375000e+00 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -1.305262e-01 9.914449e-01
    outer loop
      vertex   8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   4.375000e+00 -9.258820e+00 1.246593e+01
      vertex   8.750000e+00 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   8.750000e+00 -9.258820e+00 1.246593e+01
      vertex   4.375000e+00 -9.258820e+00 1.246593e+01
      vertex   8.750000e+00 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   4.375000e+00 -9.258820e+00 1.246593e+01
      vertex   4.375000e+00 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   8.750000e+00 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   8.750000e+00 -9.707107e+00 1.220711e+01
      vertex   4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   4.375000e+00 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   -4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   -4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   1.110223e-14 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   1.110223e-14 -9.707107e+00 1.220711e+01
      vertex   4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   1.110223e-14 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   1.110223e-14 -9.500001e+00 1.236603e+01
      vertex   4.375000e+00 -9.707107e+00 1.220711e+01
      vertex   4.375000e+00 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   1.110223e-14 -9.500001e+00 1.236603e+01
      vertex   4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   1.110223e-14 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   1.110223e-14 -9.258820e+00 1.246593e+01
      vertex   4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   4.375000e+00 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   -4.375000e+00 -9.258820e+00 1.246593e+01
      vertex   -4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   1.110223e-14 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -6.087614e-01 7.933533e-01
    outer loop
      vertex   1.110223e-14 -9.500001e+00 1.236603e+01
      vertex   -4.375000e+00 -9.500001e+00 1.236603e+01
      vertex   1.110223e-14 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal 0.000000e+00 -3.826834e-01 9.238795e-01
    outer loop
      vertex   -4.375000e+00 -9.258820e+00 1.246593e+01
      vertex   1.110223e-14 -9.500001e+00 1.236603e+01
      vertex   1.110223e-14 -9.258820e+00 1.246593e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.000001e+00 1.250000e+01
      vertex   -8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   -8.750000e+00 -8.800000e+00 1.250000e+01
      vertex   -8.750000e+00 -8.541181e+00 1.246593e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   -8.750000e+00 -8.541181e+00 1.246593e+01
      vertex   -8.750000e+00 -8.300000e+00 1.236603e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   -8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   -8.750000e+00 -9.707107e+00 1.220711e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.707107e+00 1.220711e+01
      vertex   -8.750000e+00 -8.300000e+00 1.236603e+01
      vertex   -8.750000e+00 -8.092893e+00 1.220711e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 -0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.707107e+00 1.220711e+01
      vertex   -8.750000e+00 -8.092893e+00 1.220711e+01
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.866026e+00 1.200000e+01
      vertex   -8.750000e+00 -8.092893e+00 1.220711e+01
      vertex   -8.750000e+00 -7.933974e+00 1.200000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   -8.750000e+00 -9.500001e+00 1.236603e+01
      vertex   -8.750000e+00 -9.258820e+00 1.246593e+01
      vertex   -8.750000e+00 -9.000001e+00 1.250000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 -2.104688e-16 -1.110224e-15
    outer loop
      vertex   -3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   -3.800000e+00 -3.690000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 -2.104688e-16 -1.110224e-15
    outer loop
      vertex   -3.800000e+00 -3.690000e+00 -1.160000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   -3.800000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 -0.000000e+00 -0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.690000e+00 -1.160000e+01
      vertex   3.800000e+00 -3.690000e+00 -1.200000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   3.800000e+00 -3.690000e+00 -1.200000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -3.116416e-16 0.000000e+00 1.000000e+00
    outer loop
      vertex   3.800000e+00 -3.690000e+00 -1.160000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   9.500000e+00 -3.690000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -3.116416e-16 0.000000e+00 1.000000e+00
    outer loop
      vertex   9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   9.500000e+00 -9.200000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -4.674623e-16 -2.612289e-16 1.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -6.544473e-16 -9.926700e-16 1.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -1.246566e-15 0.000000e+00 1.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -1.246566e-15 0.000000e+00 1.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.160000e+01
      vertex   -3.800000e+00 -3.690000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.967294e+00 -9.200000e+00 -1.154735e+01
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   -9.500000e+00 -9.200000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.967294e+00 -9.200000e+00 -1.154735e+01
      vertex   -1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   -1.080933e+01 -9.200000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.080933e+01 -9.200000e+00 -1.114185e+01
      vertex   -1.114185e+01 -9.200000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.114185e+01 -9.200000e+00 -1.080933e+01
      vertex   -1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   -1.154735e+01 -9.200000e+00 -9.967294e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.160000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   -1.160000e+01 -9.200000e+00 9.500000e+00
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   -1.160000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.154735e+01 -9.200000e+00 9.967294e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   -1.154735e+01 -9.200000e+00 9.967294e+00
      vertex   -1.139203e+01 -9.200000e+00 1.041116e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.139203e+01 -9.200000e+00 1.041116e+01
      vertex   -1.114185e+01 -9.200000e+00 1.080933e+01
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   -1.114185e+01 -9.200000e+00 1.080933e+01
      vertex   -1.080933e+01 -9.200000e+00 1.114185e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   -1.080933e+01 -9.200000e+00 1.114185e+01
      vertex   -1.041116e+01 -9.200000e+00 1.139203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.041116e+01 -9.200000e+00 1.139203e+01
      vertex   -9.967294e+00 -9.200000e+00 1.154735e+01
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.967294e+00 -9.200000e+00 1.154735e+01
      vertex   1.041116e+01 -9.200000e+00 1.139203e+01
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   1.041116e+01 -9.200000e+00 1.139203e+01
      vertex   1.080933e+01 -9.200000e+00 1.114185e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   1.080933e+01 -9.200000e+00 1.114185e+01
      vertex   1.114185e+01 -9.200000e+00 1.080933e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.114185e+01 -9.200000e+00 1.080933e+01
      vertex   1.139203e+01 -9.200000e+00 1.041116e+01
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   1.139203e+01 -9.200000e+00 1.041116e+01
      vertex   1.154735e+01 -9.200000e+00 9.967294e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   1.154735e+01 -9.200000e+00 9.967294e+00
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.154735e+01 -9.200000e+00 -9.967294e+00
      vertex   1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   1.114185e+01 -9.200000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.114185e+01 -9.200000e+00 -1.080933e+01
      vertex   1.080933e+01 -9.200000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.080933e+01 -9.200000e+00 -1.114185e+01
      vertex   1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   9.967294e+00 -9.200000e+00 -1.154735e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   9.967294e+00 -9.200000e+00 -1.154735e+01
      vertex   9.500000e+00 -9.200000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   -9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.690000e+00 -1.160000e+01
      vertex   9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   3.800000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   3.800000e+00 -3.690000e+00 -1.200000e+01
      vertex   9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   9.500000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.690000e+00 -1.200000e+01
      vertex   9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   9.987726e+00 -3.690000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   9.967294e+00 -3.690000e+00 -1.154735e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   1.045671e+01 -3.690000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   1.041116e+01 -3.690000e+00 -1.139203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   1.088893e+01 -3.690000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   1.080933e+01 -3.690000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   1.126777e+01 -3.690000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.126777e+01 -3.690000e+00 -1.126777e+01
      vertex   1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   1.114185e+01 -3.690000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.126777e+01 -3.690000e+00 -1.126777e+01
      vertex   1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   1.157867e+01 -3.690000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   1.139203e+01 -3.690000e+00 -1.041116e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   1.180970e+01 -3.690000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   1.154735e+01 -3.690000e+00 -9.967294e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   1.195196e+01 -3.690000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.200000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   1.200000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.200000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.200000e+01 -3.690000e+00 9.500000e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.160000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.200000e+01 -3.690000e+00 9.500000e+00
      vertex   1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   1.195196e+01 -3.690000e+00 9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   1.154735e+01 -3.690000e+00 9.967294e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   1.180970e+01 -3.690000e+00 1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   1.139203e+01 -3.690000e+00 1.041116e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   1.157867e+01 -3.690000e+00 1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   1.114185e+01 -3.690000e+00 1.080933e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   1.126777e+01 -3.690000e+00 1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.126777e+01 -3.690000e+00 1.126777e+01
      vertex   1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   1.080933e+01 -3.690000e+00 1.114185e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.126777e+01 -3.690000e+00 1.126777e+01
      vertex   1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   1.088893e+01 -3.690000e+00 1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   1.041116e+01 -3.690000e+00 1.139203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   1.045671e+01 -3.690000e+00 1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   9.967294e+00 -3.690000e+00 1.154735e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   9.987726e+00 -3.690000e+00 1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   9.500000e+00 -3.690000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   9.500000e+00 -3.690000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.690000e+00 1.200000e+01
      vertex   9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   -9.500000e+00 -3.690000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   9.500000e+00 -3.690000e+00 1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   -9.500000e+00 -3.690000e+00 1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.690000e+00 1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   -9.987726e+00 -3.690000e+00 1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   -9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   -9.967294e+00 -3.690000e+00 1.154735e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   -9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   -1.045671e+01 -3.690000e+00 1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   -9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   -1.041116e+01 -3.690000e+00 1.139203e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   -1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   -1.088893e+01 -3.690000e+00 1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   -1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   -1.080933e+01 -3.690000e+00 1.114185e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   -1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   -1.126777e+01 -3.690000e+00 1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.690000e+00 1.126777e+01
      vertex   -1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   -1.114185e+01 -3.690000e+00 1.080933e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.690000e+00 1.126777e+01
      vertex   -1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   -1.157867e+01 -3.690000e+00 1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   -1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   -1.139203e+01 -3.690000e+00 1.041116e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   -1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   -1.180970e+01 -3.690000e+00 1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   -1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   -1.154735e+01 -3.690000e+00 9.967294e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   -1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   -1.195196e+01 -3.690000e+00 9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   -1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.200000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.200000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -3.690000e+00 -9.500000e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.160000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.200000e+01 -3.690000e+00 -9.500000e+00
      vertex   -1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   -1.195196e+01 -3.690000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   -1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   -1.154735e+01 -3.690000e+00 -9.967294e+00
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   -1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   -1.180970e+01 -3.690000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   -1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   -1.139203e+01 -3.690000e+00 -1.041116e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   -1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   -1.157867e+01 -3.690000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   -1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   -1.114185e+01 -3.690000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   -1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   -1.126777e+01 -3.690000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.690000e+00 -1.126777e+01
      vertex   -1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   -1.080933e+01 -3.690000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.126777e+01 -3.690000e+00 -1.126777e+01
      vertex   -1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   -1.088893e+01 -3.690000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   -1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   -1.041116e+01 -3.690000e+00 -1.139203e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   -1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   -1.045671e+01 -3.690000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   -1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   -9.967294e+00 -3.690000e+00 -1.154735e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   -9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   -9.987726e+00 -3.690000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   -9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 0.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.690000e+00 -1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   -3.800000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 0.000000e+00 1.000000e+00 -0.000000e+00
    outer loop
      vertex   -3.800000e+00 -3.690000e+00 -1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   -3.800000e+00 -3.690000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal 1.119645e-01 -0.000000e+00 9.937122e-01
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   -9.967294e+00 -9.200000e+00 -1.154735e+01
    endloop
  endfacet
  facet normal 1.119645e-01 -0.000000e+00 9.937122e-01
    outer loop
      vertex   -9.967294e+00 -9.200000e+00 -1.154735e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.160000e+01
      vertex   -9.967294e+00 -3.690000e+00 -1.154735e+01
    endloop
  endfacet
  facet normal 3.302791e-01 -0.000000e+00 9.438833e-01
    outer loop
      vertex   -9.967294e+00 -9.200000e+00 -1.154735e+01
      vertex   -9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   -1.041116e+01 -9.200000e+00 -1.139203e+01
    endloop
  endfacet
  facet normal 3.302791e-01 -0.000000e+00 9.438833e-01
    outer loop
      vertex   -1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   -9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   -1.041116e+01 -3.690000e+00 -1.139203e+01
    endloop
  endfacet
  facet normal 5.320321e-01 -0.000000e+00 8.467242e-01
    outer loop
      vertex   -1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   -1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   -1.080933e+01 -9.200000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal 5.320321e-01 -0.000000e+00 8.467242e-01
    outer loop
      vertex   -1.080933e+01 -9.200000e+00 -1.114185e+01
      vertex   -1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   -1.080933e+01 -3.690000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal 7.071068e-01 -0.000000e+00 7.071068e-01
    outer loop
      vertex   -1.080933e+01 -9.200000e+00 -1.114185e+01
      vertex   -1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   -1.114185e+01 -9.200000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal 7.071068e-01 -4.559252e-16 7.071068e-01
    outer loop
      vertex   -1.114185e+01 -9.200000e+00 -1.080933e+01
      vertex   -1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   -1.114185e+01 -3.690000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal 8.467242e-01 -3.430413e-16 5.320321e-01
    outer loop
      vertex   -1.114185e+01 -9.200000e+00 -1.080933e+01
      vertex   -1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   -1.139203e+01 -9.200000e+00 -1.041116e+01
    endloop
  endfacet
  facet normal 8.467242e-01 -0.000000e+00 5.320321e-01
    outer loop
      vertex   -1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   -1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   -1.139203e+01 -3.690000e+00 -1.041116e+01
    endloop
  endfacet
  facet normal 9.438833e-01 -0.000000e+00 3.302791e-01
    outer loop
      vertex   -1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   -1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   -1.154735e+01 -9.200000e+00 -9.967294e+00
    endloop
  endfacet
  facet normal 9.438833e-01 -1.064779e-16 3.302791e-01
    outer loop
      vertex   -1.154735e+01 -9.200000e+00 -9.967294e+00
      vertex   -1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   -1.154735e+01 -3.690000e+00 -9.967294e+00
    endloop
  endfacet
  facet normal 9.937122e-01 -3.609598e-17 1.119645e-01
    outer loop
      vertex   -1.154735e+01 -9.200000e+00 -9.967294e+00
      vertex   -1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 9.937122e-01 -0.000000e+00 1.119645e-01
    outer loop
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   -1.160000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 5.609548e-16
    outer loop
      vertex   -1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 0.000000e+00 5.609548e-16
    outer loop
      vertex   -1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.160000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 9.937122e-01 0.000000e+00 -1.119645e-01
    outer loop
      vertex   -1.160000e+01 -9.200000e+00 9.500000e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.154735e+01 -9.200000e+00 9.967294e+00
    endloop
  endfacet
  facet normal 9.937122e-01 0.000000e+00 -1.119645e-01
    outer loop
      vertex   -1.154735e+01 -9.200000e+00 9.967294e+00
      vertex   -1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   -1.154735e+01 -3.690000e+00 9.967294e+00
    endloop
  endfacet
  facet normal 9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   -1.154735e+01 -9.200000e+00 9.967294e+00
      vertex   -1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   -1.139203e+01 -9.200000e+00 1.041116e+01
    endloop
  endfacet
  facet normal 9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   -1.139203e+01 -9.200000e+00 1.041116e+01
      vertex   -1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   -1.139203e+01 -3.690000e+00 1.041116e+01
    endloop
  endfacet
  facet normal 8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   -1.139203e+01 -9.200000e+00 1.041116e+01
      vertex   -1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   -1.114185e+01 -9.200000e+00 1.080933e+01
    endloop
  endfacet
  facet normal 8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   -1.114185e+01 -9.200000e+00 1.080933e+01
      vertex   -1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   -1.114185e+01 -3.690000e+00 1.080933e+01
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   -1.114185e+01 -9.200000e+00 1.080933e+01
      vertex   -1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   -1.080933e+01 -9.200000e+00 1.114185e+01
    endloop
  endfacet
  facet normal 7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   -1.080933e+01 -9.200000e+00 1.114185e+01
      vertex   -1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   -1.080933e+01 -3.690000e+00 1.114185e+01
    endloop
  endfacet
  facet normal 5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   -1.080933e+01 -9.200000e+00 1.114185e+01
      vertex   -1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   -1.041116e+01 -9.200000e+00 1.139203e+01
    endloop
  endfacet
  facet normal 5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   -1.041116e+01 -9.200000e+00 1.139203e+01
      vertex   -1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   -1.041116e+01 -3.690000e+00 1.139203e+01
    endloop
  endfacet
  facet normal 3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   -1.041116e+01 -9.200000e+00 1.139203e+01
      vertex   -1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   -9.967294e+00 -9.200000e+00 1.154735e+01
    endloop
  endfacet
  facet normal 3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   -9.967294e+00 -9.200000e+00 1.154735e+01
      vertex   -1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   -9.967294e+00 -3.690000e+00 1.154735e+01
    endloop
  endfacet
  facet normal 1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   -9.967294e+00 -9.200000e+00 1.154735e+01
      vertex   -9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   -9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   -9.500000e+00 -3.690000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 5.609548e-16 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 5.609548e-16 0.000000e+00 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
    endloop
  endfacet
  facet normal 9.349247e-17 5.473896e-08 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
    endloop
  endfacet
  facet normal -3.529223e-08 -4.105422e-08 -1.000000e+00
    outer loop
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -2.178379e-16 -2.534033e-16 -1.000000e+00
    outer loop
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   9.500000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal -3.116416e-16 0.000000e+00 -1.000000e+00
    outer loop
      vertex   9.500000e+00 -3.690000e+00 -1.200000e+01
      vertex   3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   3.800000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 4.705630e-08 1.550149e-22 -1.000000e+00
    outer loop
      vertex   -9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.200000e+01
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 4.705630e-08 -9.903884e-24 -1.000000e+00
    outer loop
      vertex   -3.800000e+00 -5.800000e+00 -1.200000e+01
      vertex   -9.500000e+00 -3.690000e+00 -1.200000e+01
      vertex   -3.800000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 9.951808e-01 -7.084057e-17 -9.805673e-02
    outer loop
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
      vertex   1.200000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 9.951847e-01 -2.780680e-06 -9.801714e-02
    outer loop
      vertex   1.200000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
      vertex   1.195196e+01 -3.690000e+00 -9.987726e+00
    endloop
  endfacet
  facet normal 9.564706e-01 -5.561598e-06 -2.918287e-01
    outer loop
      vertex   1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   1.195195e+01 -1.070000e+01 -9.987623e+00
      vertex   1.180899e+01 -1.070000e+01 -1.045619e+01
    endloop
  endfacet
  facet normal 9.569403e-01 -1.183264e-04 -2.902847e-01
    outer loop
      vertex   1.195196e+01 -3.690000e+00 -9.987726e+00
      vertex   1.180899e+01 -1.070000e+01 -1.045619e+01
      vertex   1.180970e+01 -3.690000e+00 -1.045671e+01
    endloop
  endfacet
  facet normal 8.820205e-01 -1.242687e-04 -4.712109e-01
    outer loop
      vertex   1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   1.180899e+01 -1.070000e+01 -1.045619e+01
      vertex   1.157804e+01 -1.070000e+01 -1.088849e+01
    endloop
  endfacet
  facet normal 8.819213e-01 -1.095428e-04 -4.713967e-01
    outer loop
      vertex   1.180970e+01 -3.690000e+00 -1.045671e+01
      vertex   1.157804e+01 -1.070000e+01 -1.088849e+01
      vertex   1.157867e+01 -3.690000e+00 -1.088893e+01
    endloop
  endfacet
  facet normal 7.740033e-01 -1.097415e-04 -6.331815e-01
    outer loop
      vertex   1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   1.157804e+01 -1.070000e+01 -1.088849e+01
      vertex   1.126777e+01 -1.070000e+01 -1.126777e+01
    endloop
  endfacet
  facet normal 7.730105e-01 -2.159878e-07 -6.343933e-01
    outer loop
      vertex   1.157867e+01 -3.690000e+00 -1.088893e+01
      vertex   1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   1.126777e+01 -3.690000e+00 -1.126777e+01
    endloop
  endfacet
  facet normal 6.343933e-01 -2.075670e-07 -7.730105e-01
    outer loop
      vertex   1.126777e+01 -3.690000e+00 -1.126777e+01
      vertex   1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   1.088893e+01 -3.690000e+00 -1.157867e+01
    endloop
  endfacet
  facet normal 6.339251e-01 -4.253863e-05 -7.733944e-01
    outer loop
      vertex   1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   1.126777e+01 -1.070000e+01 -1.126777e+01
      vertex   1.088879e+01 -1.070000e+01 -1.157840e+01
    endloop
  endfacet
  facet normal 4.717217e-01 -4.357923e-05 -8.817475e-01
    outer loop
      vertex   1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   1.088879e+01 -1.070000e+01 -1.157840e+01
      vertex   1.045669e+01 -1.070000e+01 -1.180957e+01
    endloop
  endfacet
  facet normal 4.713967e-01 -1.781517e-05 -8.819213e-01
    outer loop
      vertex   1.088893e+01 -3.690000e+00 -1.157867e+01
      vertex   1.045669e+01 -1.070000e+01 -1.180957e+01
      vertex   1.045671e+01 -3.690000e+00 -1.180970e+01
    endloop
  endfacet
  facet normal 2.904903e-01 -1.867045e-05 -9.568779e-01
    outer loop
      vertex   1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   1.045669e+01 -1.070000e+01 -1.180957e+01
      vertex   9.987751e+00 -1.070000e+01 -1.195193e+01
    endloop
  endfacet
  facet normal 2.902847e-01 -3.648353e-06 -9.569403e-01
    outer loop
      vertex   1.045671e+01 -3.690000e+00 -1.180970e+01
      vertex   9.987751e+00 -1.070000e+01 -1.195193e+01
      vertex   9.987726e+00 -3.690000e+00 -1.195196e+01
    endloop
  endfacet
  facet normal 9.808177e-02 -4.540031e-06 -9.951784e-01
    outer loop
      vertex   9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   9.987751e+00 -1.070000e+01 -1.195193e+01
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
    endloop
  endfacet
  facet normal 9.801714e-02 -1.524920e-16 -9.951847e-01
    outer loop
      vertex   9.987726e+00 -3.690000e+00 -1.195196e+01
      vertex   9.500000e+00 -1.070000e+01 -1.200000e+01
      vertex   9.500000e+00 -3.690000e+00 -1.200000e+01
    endloop
  endfacet
  facet normal 1.000000e+00 9.476518e-32 9.349247e-17
    outer loop
      vertex   1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   1.200000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal 1.000000e+00 2.534033e-16 0.000000e+00
    outer loop
      vertex   1.200000e+01 -3.690000e+00 9.500000e+00
      vertex   1.200000e+01 -1.070000e+01 -9.500000e+00
      vertex   1.200000e+01 -3.690000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal 9.801714e-02 2.483786e-17 9.951847e-01
    outer loop
      vertex   9.500000e+00 -3.690000e+00 1.200000e+01
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   9.987726e+00 -3.690000e+00 1.195196e+01
    endloop
  endfacet
  facet normal 9.833125e-02 -2.206665e-05 9.951537e-01
    outer loop
      vertex   9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   9.500000e+00 -1.070000e+01 1.200000e+01
      vertex   9.987858e+00 -1.070000e+01 1.195179e+01
    endloop
  endfacet
  facet normal 2.902847e-01 -1.751925e-05 9.569403e-01
    outer loop
      vertex   9.987726e+00 -3.690000e+00 1.195196e+01
      vertex   9.987858e+00 -1.070000e+01 1.195179e+01
      vertex   1.045671e+01 -3.690000e+00 1.180970e+01
    endloop
  endfacet
  facet normal 2.900477e-01 -2.100033e-07 9.570122e-01
    outer loop
      vertex   1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   9.987858e+00 -1.070000e+01 1.195179e+01
      vertex   1.045672e+01 -1.070000e+01 1.180969e+01
    endloop
  endfacet
  facet normal 4.713967e-01 1.725753e-07 8.819213e-01
    outer loop
      vertex   1.045671e+01 -3.690000e+00 1.180970e+01
      vertex   1.045672e+01 -1.070000e+01 1.180969e+01
      vertex   1.088893e+01 -3.690000e+00 1.157867e+01
    endloop
  endfacet
  facet normal 4.716887e-01 -2.297698e-05 8.817651e-01
    outer loop
      vertex   1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   1.045672e+01 -1.070000e+01 1.180969e+01
      vertex   1.088882e+01 -1.070000e+01 1.157855e+01
    endloop
  endfacet
  facet normal 6.341359e-01 -2.353935e-05 7.732216e-01
    outer loop
      vertex   1.088893e+01 -3.690000e+00 1.157867e+01
      vertex   1.088882e+01 -1.070000e+01 1.157855e+01
      vertex   1.126778e+01 -1.070000e+01 1.126776e+01
    endloop
  endfacet
  facet normal 7.733983e-01 -4.266957e-05 6.339204e-01
    outer loop
      vertex   1.157841e+01 -1.070000e+01 1.088878e+01
      vertex   1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   1.126778e+01 -1.070000e+01 1.126776e+01
    endloop
  endfacet
  facet normal 7.730105e-01 9.082114e-08 6.343933e-01
    outer loop
      vertex   1.126778e+01 -1.070000e+01 1.126776e+01
      vertex   1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   1.126777e+01 -3.690000e+00 1.126777e+01
    endloop
  endfacet
  facet normal 6.343933e-01 -2.629018e-07 7.730105e-01
    outer loop
      vertex   1.126778e+01 -1.070000e+01 1.126776e+01
      vertex   1.126777e+01 -3.690000e+00 1.126777e+01
      vertex   1.088893e+01 -3.690000e+00 1.157867e+01
    endloop
  endfacet
  facet normal 8.817490e-01 -4.344537e-05 4.717190e-01
    outer loop
      vertex   1.157841e+01 -1.070000e+01 1.088878e+01
      vertex   1.180957e+01 -1.070000e+01 1.045668e+01
      vertex   1.157867e+01 -3.690000e+00 1.088893e+01
    endloop
  endfacet
  facet normal 8.819213e-01 -1.790187e-05 4.713967e-01
    outer loop
      vertex   1.157867e+01 -3.690000e+00 1.088893e+01
      vertex   1.180957e+01 -1.070000e+01 1.045668e+01
      vertex   1.180970e+01 -3.690000e+00 1.045671e+01
    endloop
  endfacet
  facet normal 9.568785e-01 -1.858082e-05 2.904885e-01
    outer loop
      vertex   1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   1.180957e+01 -1.070000e+01 1.045668e+01
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
    endloop
  endfacet
  facet normal 9.569403e-01 -3.692422e-06 2.902847e-01
    outer loop
      vertex   1.180970e+01 -3.690000e+00 1.045671e+01
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
      vertex   1.195196e+01 -3.690000e+00 9.987726e+00
    endloop
  endfacet
  facet normal 9.951784e-01 -4.496045e-06 9.808114e-02
    outer loop
      vertex   1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   1.195193e+01 -1.070000e+01 9.987748e+00
      vertex   1.200000e+01 -1.070000e+01 9.500000e+00
    endloop
  endfacet
  facet normal 9.951847e-01 9.997822e-17 9.801714e-02
    outer loop
      vertex   1.195196e+01 -3.690000e+00 9.987726e+00
      vertex   1.200000e+01 -1.070000e+01 9.500000e+00
      vertex   1.200000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -9.937122e-01 0.000000e+00 1.119645e-01
    outer loop
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.154735e+01 -9.200000e+00 -9.967294e+00
    endloop
  endfacet
  facet normal -9.937122e-01 0.000000e+00 1.119645e-01
    outer loop
      vertex   1.154735e+01 -9.200000e+00 -9.967294e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.154735e+01 -3.690000e+00 -9.967294e+00
    endloop
  endfacet
  facet normal -9.438833e-01 0.000000e+00 3.302791e-01
    outer loop
      vertex   1.154735e+01 -9.200000e+00 -9.967294e+00
      vertex   1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   1.139203e+01 -9.200000e+00 -1.041116e+01
    endloop
  endfacet
  facet normal -9.438833e-01 9.134059e-17 3.302791e-01
    outer loop
      vertex   1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   1.154735e+01 -3.690000e+00 -9.967294e+00
      vertex   1.139203e+01 -3.690000e+00 -1.041116e+01
    endloop
  endfacet
  facet normal -8.467242e-01 -7.006775e-17 5.320321e-01
    outer loop
      vertex   1.139203e+01 -9.200000e+00 -1.041116e+01
      vertex   1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   1.114185e+01 -9.200000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal -8.467242e-01 0.000000e+00 5.320321e-01
    outer loop
      vertex   1.114185e+01 -9.200000e+00 -1.080933e+01
      vertex   1.139203e+01 -3.690000e+00 -1.041116e+01
      vertex   1.114185e+01 -3.690000e+00 -1.080933e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   1.114185e+01 -9.200000e+00 -1.080933e+01
      vertex   1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   1.080933e+01 -9.200000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 7.071068e-01
    outer loop
      vertex   1.080933e+01 -9.200000e+00 -1.114185e+01
      vertex   1.114185e+01 -3.690000e+00 -1.080933e+01
      vertex   1.080933e+01 -3.690000e+00 -1.114185e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 8.467242e-01
    outer loop
      vertex   1.080933e+01 -9.200000e+00 -1.114185e+01
      vertex   1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   1.041116e+01 -9.200000e+00 -1.139203e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 8.467242e-01
    outer loop
      vertex   1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   1.080933e+01 -3.690000e+00 -1.114185e+01
      vertex   1.041116e+01 -3.690000e+00 -1.139203e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 9.438833e-01
    outer loop
      vertex   1.041116e+01 -9.200000e+00 -1.139203e+01
      vertex   1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   9.967294e+00 -9.200000e+00 -1.154735e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 9.438833e-01
    outer loop
      vertex   9.967294e+00 -9.200000e+00 -1.154735e+01
      vertex   1.041116e+01 -3.690000e+00 -1.139203e+01
      vertex   9.967294e+00 -3.690000e+00 -1.154735e+01
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 9.937122e-01
    outer loop
      vertex   9.967294e+00 -9.200000e+00 -1.154735e+01
      vertex   9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   9.500000e+00 -9.200000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 9.937122e-01
    outer loop
      vertex   9.500000e+00 -9.200000e+00 -1.160000e+01
      vertex   9.967294e+00 -3.690000e+00 -1.154735e+01
      vertex   9.500000e+00 -3.690000e+00 -1.160000e+01
    endloop
  endfacet
  facet normal -1.000000e+00 -0.000000e+00 -6.544473e-16
    outer loop
      vertex   1.160000e+01 -3.690000e+00 9.500000e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -1.000000e+00 0.000000e+00 -6.544473e-16
    outer loop
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
      vertex   1.160000e+01 -3.690000e+00 -9.500000e+00
      vertex   1.160000e+01 -9.200000e+00 -9.500000e+00
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   9.500000e+00 -9.200000e+00 1.160000e+01
      vertex   9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   9.967294e+00 -9.200000e+00 1.154735e+01
    endloop
  endfacet
  facet normal -1.119645e-01 0.000000e+00 -9.937122e-01
    outer loop
      vertex   9.967294e+00 -9.200000e+00 1.154735e+01
      vertex   9.500000e+00 -3.690000e+00 1.160000e+01
      vertex   9.967294e+00 -3.690000e+00 1.154735e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   9.967294e+00 -9.200000e+00 1.154735e+01
      vertex   9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   1.041116e+01 -9.200000e+00 1.139203e+01
    endloop
  endfacet
  facet normal -3.302791e-01 0.000000e+00 -9.438833e-01
    outer loop
      vertex   1.041116e+01 -9.200000e+00 1.139203e+01
      vertex   9.967294e+00 -3.690000e+00 1.154735e+01
      vertex   1.041116e+01 -3.690000e+00 1.139203e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   1.041116e+01 -9.200000e+00 1.139203e+01
      vertex   1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   1.080933e+01 -9.200000e+00 1.114185e+01
    endloop
  endfacet
  facet normal -5.320321e-01 0.000000e+00 -8.467242e-01
    outer loop
      vertex   1.080933e+01 -9.200000e+00 1.114185e+01
      vertex   1.041116e+01 -3.690000e+00 1.139203e+01
      vertex   1.080933e+01 -3.690000e+00 1.114185e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   1.080933e+01 -9.200000e+00 1.114185e+01
      vertex   1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   1.114185e+01 -9.200000e+00 1.080933e+01
    endloop
  endfacet
  facet normal -7.071068e-01 0.000000e+00 -7.071068e-01
    outer loop
      vertex   1.114185e+01 -9.200000e+00 1.080933e+01
      vertex   1.080933e+01 -3.690000e+00 1.114185e+01
      vertex   1.114185e+01 -3.690000e+00 1.080933e+01
    endloop
  endfacet
  facet normal -8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   1.114185e+01 -9.200000e+00 1.080933e+01
      vertex   1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   1.139203e+01 -9.200000e+00 1.041116e+01
    endloop
  endfacet
  facet normal -8.467242e-01 0.000000e+00 -5.320321e-01
    outer loop
      vertex   1.139203e+01 -9.200000e+00 1.041116e+01
      vertex   1.114185e+01 -3.690000e+00 1.080933e+01
      vertex   1.139203e+01 -3.690000e+00 1.041116e+01
    endloop
  endfacet
  facet normal -9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   1.139203e+01 -9.200000e+00 1.041116e+01
      vertex   1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   1.154735e+01 -9.200000e+00 9.967294e+00
    endloop
  endfacet
  facet normal -9.438833e-01 0.000000e+00 -3.302791e-01
    outer loop
      vertex   1.154735e+01 -9.200000e+00 9.967294e+00
      vertex   1.139203e+01 -3.690000e+00 1.041116e+01
      vertex   1.154735e+01 -3.690000e+00 9.967294e+00
    endloop
  endfacet
  facet normal -9.937122e-01 0.000000e+00 -1.119645e-01
    outer loop
      vertex   1.154735e+01 -9.200000e+00 9.967294e+00
      vertex   1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
    endloop
  endfacet
  facet normal -9.937122e-01 0.000000e+00 -1.119645e-01
    outer loop
      vertex   1.160000e+01 -9.200000e+00 9.500000e+00
      vertex   1.154735e+01 -3.690000e+00 9.967294e+00
      vertex   1.160000e+01 -3.690000e+00 9.500000e+00
    endloop
  endfacet
endsolid

```

### Assembly

Pretty straight forward. Solder the header sockets and pins to the pcb and to the INMP441.

>❗Check the direction of the header sockets and pins. Especially on the INMP441, the side with mic icon should face the same direction as the screen.

Put it in the case, screw it together and attach the HAT to the AtomS3.

![MicHatCase v15](https://github.com/user-attachments/assets/4bc6dd32-d535-4368-bd40-c113e375623f)

## Software

- **ESPHome / Home Assistant**
- **Music Assistant** (optional)
- A **media player entity** (e.g. media_player.office)

### ESPHome

Install Firmware: [Web Installer](https://www.ittips.ch/ha-assist-mic-satellite/) | [yaml](code/esphome/va-mic-sat-atoms3.yaml)

This has been frankensteined together from various sources. I will try to give [credit](#credits) where [credit](#credits) is due.

### Home Assistant

The device should get auto discovered.

We need to tick **Allow the device to perform Home Assistant actions**. Since the firmware will call the `media_player.play_media` service, we need to allow this.
![Configure ESPHome Device](docs/assets/HAConfigure.png)

While you here, click on **device** and change paste your media player entity id where the announcement should be played.

### Sounds

There are **two** sound files required. One for when the device is listening, this is the silent wav file, the second is for the alarm ringtone.

Currently the firmware is configured that the media player streams the files directly from github, in other words it (media_player) requires an internet connection. If you want to change this, adopt the device in ESPHome and change the following lines:

```yaml
substitutions:
  # ....
  timer_sound_file: media-source://media_source/local/my-alarm.mp3
  silence_sound_file: media-source://media_source/local/my-silence.mp3
```

So these need to be copied there. Can be done with the vscode addon or via samba share. see [Home Assistant Docs](https://www.home-assistant.io/integrations/media_source/)

## How it works

### Simplified Process

```mermaid
sequenceDiagram
    participant MIC Satellite
    participant Assist Pipeline
    participant media_player
    MIC Satellite->MIC Satellite: Wake Word detection
    MIC Satellite->>media_player: service call media_player.play_media (empty announcement)
    MIC Satellite->MIC Satellite: Listening  
    MIC Satellite->>Assist Pipeline: Send intent
    Assist Pipeline->>MIC Satellite: response mp3_url
    MIC Satellite->>media_player: service call media_player.play_media (announcement / mp3_url)
```

### Wiring / Schematics

[KiCAD Schematic](<pcb/Mic HAT for M5Stack Atom/Mic HAT for M5Stack Atom.kicad_sch>) | [KiCAD Canvas Online View](https://kicanvas.org/?github=https%3A%2F%2Fgithub.com%2FMrWyss%2Fha-assist-mic-satellite%2Ftree%2Fmain%2Fpcb%2FMic%2520HAT%2520for%2520M5Stack%2520Atom)

<img src="docs/assets/wiring.png" alt="wiring" style="width: 500px;" />

AtomS3 Pin|INMP441 Pin
:----------:|:-----------:
3V3| VDD
GND | GND + L/R
G5 (GPIO5) | WS
G6 (GPIO6) | SCK
G7 (GPIO7) | SD

## 🚧 Gallery Work in Progress 🚧

3D Illustration            |  Config Options
:-------------------------:|:-------------------------:
![Render](docs/assets/case_render.png) | ![ESPhome Configurations](docs/assets/HAConfig.png)

Muted            |  Intent in Action
:-------------------------:|:-------------------------:
![Muted](docs/assets/muted_smaller.jpg) | ![Intent in Action](docs/assets/intent_video.gif)

Back View            |  Front View
:-------------------------:|:-------------------------:
![alt text](docs/assets/INMP441_HAT_For_M5Stack_AtomS3_Back_RT.png) | ![alt text](docs/assets/INMP441_HAT_For_M5Stack_AtomS3_RT.png)

## Credits

- [HA Voice Kit](https://github.com/esphome/voice-kit)
- [ESPHome Voice Assistant Github Repo](https://github.com/esphome/firmware/tree/main/voice-assistant/)
- [SmarthomeCircle](https://smarthomecircle.com/How-I-created-my-voice-assistant-with-on-device-wake-word-using-home-assistant)
- [Community](https://community.home-assistant.io/t/esphome-voice-assistant-speech-output-to-home-assistant-media-player/588337/18)

## Contributing

Please do
