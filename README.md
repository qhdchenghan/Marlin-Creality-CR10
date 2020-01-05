# Marlin 3D Printer Firmware for Creality CR-10S V1
<img align="right" src="../../raw/1.1.x/buildroot/share/pixmaps/logo/marlin-250.png" />

This is a fork of the Marlin Firmware configured to work optimally with the Creality CR10s printer, with branches

Marlin is the world's most popular open source firmware for Replicating Rapid Prototyper (RepRap) machines, commonly referred to as "3D printers." Marlin Firmware is highly efficient, running even on modest 16MHz embedded AVR processors. 

## Documentation

- Visit [Marlin at github](https://github.com/MarlinFirmware/Marlin) for the original repository
- Visit [marlinfw.org](http://marlinfw.org/) for complete documentation on [configuration](http://marlinfw.org/docs/configuration/configuration.html), [installation](http://marlinfw.org/docs/basics/install.html), [features](http://marlinfw.org/meta/features/), and the many [G-codes](http://marlinfw.org/meta/gcode/) that Marlin supports. We will continue to expand the site to include in-depth articles, tutorials, and how-to videos on all of Marlin's features.
- See the [Releases](https://github.com/MarlinFirmware/Marlin/releases) page for Release Notes on all current and previous versions of Marlin.
- Check out the [RepRap.org Marlin Page](http://reprap.org/wiki/Marlin) for an overview of Marlin and its role in the RepRap project.

## bugfix-1.1.x-manual-mesh-bed-leveling

The bugfix-1.1.x-manual-mesh-bed-leveling branch is based on [`bugfix-1.1.x`](https://github.com/MarlinFirmware/Marlin/tree/bugfix-1.1.x).

 This configuration has been tested used with the following setup
 
 *  Creality CR10-S (V1)
 *  Stock hotend & extruded
 *  Petzfang Bullseye duct
 *  Arduino 1.8.10+

The settings are gathered from many sources but notably:
 *  Configuration sample in .\example_configurations\Creality\CR-10S
 *  http://www.cr10.fr/le-guide-malin-de-marlin/   [English translation](http://translate.google.com/translate?js=n&sl=auto&tl=en&u=http://www.cr10.fr/le-guide-malin-de-marlin/)
 *  https://www.printedsolid.com/blogs/news/installing-marlin-1-1-9-on-your-cr-10s-with-mesh-bed-leveling-thermal-protection-better-menu-layout-and-finally-power-resume
 *  https://www.thingiverse.com/thing:2828555
 *  https://github.com/houseofbugs/TH3D-Unified-U1.R2
 *  trial & error

## bugfix-1.1.x-bltouch-bed-leveling

This branch implements BLTouch functionality and a set of other tweaking. You can find the [branch here](https://github.com/thijse/Marlin-Creality-CR10/tree/1.1.x-bltouch-bed-leveling).

## License

Marlin is published under the [GPL license](https://github.com/COPYING.md) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
