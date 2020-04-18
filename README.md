# Marlin 3D Printer Firmware for Creality CR-10S V1
<img align="right" src="../../raw/1.1.x/buildroot/share/pixmaps/logo/marlin-250.png" />

This is a fork of the Marlin Firmware configured to work optimally with the Creality CR10s printer.

Marlin is the world's most popular open source firmware for Replicating Rapid Prototyper (RepRap) machines, commonly referred to as "3D printers." Marlin Firmware is highly efficient, running even on modest 16MHz embedded AVR processors. 


## bugfix-1.1.x-bltouch-bed-leveling

The bugfix-1.1.x-bltouch-bed-leveling branch is based on [`bugfix-1.1.x`](https://github.com/MarlinFirmware/Marlin/tree/bugfix-1.1.x).

Modified files:
* CONFIGURATIONS.H
* CONFIGURATION_ADV.H
* PINS_RAMPS.H

Download earlier versions of Marlin on the [Releases page](https://github.com/MarlinFirmware/Marlin/releases). (The latest tagged release of Marlin is version 1.1.9.)
 This configuration has been tested used with the following setup
 *  Creality CR10-S (V1)
 *  Stock hotend & extruder
 *  Petzfang Bullseye duct
 *  BLtouch 3.1
 *  Arduino 1.8.10


## Features

* All settings that are not stock have an UPDATED comment and many are documented.
* Added UBL bed leveling. Unified Bed Leveling gives the opportunity to fine tune and test the bed level mesh, and store multiple settings for different beds
* Added tri-point bed correction. This still uses the bed level mesh, but tilts it based on 3 measurement points for each print
* space saving features. Some features like Arc support have been disabled to save some space for other features such as Unified Bed Leveling
* Settings to avoid timeouts when working with OctoPrint. In particular, timing for bed heater and nozzle are more forgiving.
* Default heater settings are set for PLA-HT material. (heater temp 235, bed 60). This is a personal taste, change to your preference

## Start G-code

In order to enable mesh leveling, use following G code as part of your Start G-code block:

```
G28     ; Home all axes to prevent scratching of surface
G29     ; Enable mesh bed leveling
M420 S1 ; Turn on the Eeprom Bed Mesh
G29 L1  ; Load the mesh stored in slot 1 
G29 J   ; Probe the specified 3 points and tilt the mesh according
```

## Sources

The settings are gathered from many sources but notably:
 *  Configuration sample in .\example_configurations\Creality\CR-10S
 *  http://www.cr10.fr/le-guide-malin-de-marlin/
  * [English translation of guide above](http://translate.google.com/translate?js=n&sl=auto&tl=en&u=http://www.cr10.fr/le-guide-malin-de-marlin/)
 *  https://www.printedsolid.com/blogs/news/installing-marlin-1-1-9-on-your-cr-10s-with-mesh-bed-leveling-thermal-protection-better-menu-layout-and-finally-power-resume
 *  https://www.thingiverse.com/thing:2828555
 *  https://github.com/houseofbugs/TH3D-Unified-U1.R2
 *  trial & error

## Marlin Documentation

- Visit [Marlin at github](https://github.com/MarlinFirmware/Marlin) for the original repository
- Visit [marlinfw.org](http://marlinfw.org/) for complete documentation on [configuration](http://marlinfw.org/docs/configuration/configuration.html), [installation](http://marlinfw.org/docs/basics/install.html), [features](http://marlinfw.org/meta/features/), and the many [G-codes](http://marlinfw.org/meta/gcode/) that Marlin supports. We will continue to expand the site to include in-depth articles, tutorials, and how-to videos on all of Marlin's features.
- See the [Releases](https://github.com/MarlinFirmware/Marlin/releases) page for Release Notes on all current and previous versions of Marlin.
- Check out the [RepRap.org Marlin Page](http://reprap.org/wiki/Marlin) for an overview of Marlin and its role in the RepRap project.

## Getting started

### Calibrating your 3D printer

 * http://reprap.org/wiki/Calibration
 * http://youtu.be/wAL9d7FgInk
 * http://calculator.josefprusa.cz
 * http://reprap.org/wiki/Triffid_Hunter%27s_Calibration_Guide
 * http://www.thingiverse.com/thing:5573
 * https://sites.google.com/site/repraplogphase/calibration-of-your-reprap
 * http://www.thingiverse.com/thing:298812

### Updating firmware for CR10-s 
 * http://www.cr10.fr/le-guide-malin-de-marlin/
 * https://www.printedsolid.com/blogs/news/installing-marlin-1-1-9-on-your-cr-10s-with-mesh-bed-leveling-thermal-protection-better-menu-layout-and-finally-power-resume
 * https://www.youtube.com/watch?v=f_-FIHq4WxE
 * https://www.thingiverse.com/thing:2828555

### BlTouch v3 specific settings
 * https://youtu.be/sOFxalLOZOI
 * https://github.com/InsanityAutomation/Marlin/commit/15ce74badfd3a1b6e6ffabf882234ffa77682715

### Updating firmware, calibrating for BLTouch and Unified Bed Leveling
 * https://www.youtube.com/watch?v=y_1Kg45APko
 * https://www.youtube.com/watch?v=ONpKxkil16Q&t=832s
 * https://www.youtube.com/watch?v=U98V1nMwLKk
 
### Calibration tooling
 * https://marlin3dprintertool.se/
 * http://www.pronterface.com/
 * https://plugins.octoprint.org/plugins/bedlevelvisualizer/

## Other Branches
### bugfix-1.1.x-manual-mesh-bed-leveling

This branch implements manual mesh leveling functionality and was the basis for this branch. You can find the [branch here](https://github.com/thijse/Marlin-Creality-CR10/tree/1.1.x-manual-mesh-bed-leveling).

## License

Marlin is published under the [GPL license](https://github.com/COPYING.md) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.
