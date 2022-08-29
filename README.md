# Twomes boiler BASE  hardware

This repository contains the open hardware design files for the Twomes boiler BASE device, which can be used as a BASE module for the [M5Stack CoreInk device](https://shop.m5stack.com/collections/m5-controllers/products/m5stack-esp32-core-ink-development-kit1-54-elnk-display). This device can:
* monitor OpenTherm signals between boiler and thermostat, similar to the [Twomes OpenTherm monitor](https://github.com/energietransitie/twomes-opentherm-monitor-hardware);
* monitor with two pipe clips supply and return temperatures of hot water supplied from the boiler to the radiators and returning from the radiators, similar to the [Twomes Temperature Monitor Hardware](https://github.com/energietransitie/twomes-temp-monitor-hardware). 

<img src="./images/pcb.jpg" width="600"  />

## Table of contents
* [General info](#general-info)
* [Prerequisites](#prerequisites)
* [Producing](#producing)
* [Developing](#developing) 
* [Features](#features)
* [Status](#status)
* [License](#license)
* [Credits](#credits)

## General info
This repository contains the open hardware designs files for the Twomes something shield / base. It also includes a `docs` folder with recent printouts of the [schematics](./docs/twomes-hardware-repository-sch.pdf) and [PCB layout](./docs/twomes-hardware-repository-pcb.pdf). 

For the associated firmware that you can run on this device, please see [Twomes boiler BASE firmware](https://github.com/energietransitie/twomes-boiler-base-firmware).

## Producing


### Printed Circuit Board
To fabricate the printed circuit board you can use various PCB services. 

The folder [pcb/jlcpcb](./pcb/jlcpcb) includes all exported files needed to have the PCBs manufactured by [JLCPCB](https://www.jlcpcb.com). Upload the [zipped gerber files](./pcb/jlcpcb/gerber/gerber-TwomesSomething.zip) to the [JLCPCB quote page](https://cart.jlcpcb.com/quote), select the amount of PCBs and a colour for the silkscreen. All other options can be left on default.  If SMT assembly is desired, also select this option before ordering. This will take you to a page where the BOM and POS file can be uploaded. Use the files [BOM-TwomesSomething.csv](./pcb/jlcpcb/assembly/BOM-TwomesSomething.csv) and [CPL-TwomesSomething.csv](./pcb/jlcpcb/assembly/CPL-TwomesSomething.csv).


In the current version of this design, no SMT assembly is used. Hence, we do not provide BOM*.csv and CPL-*.csv files in the folder [pcb/jlcpcb/assembly](./pcb/jlcpcb/assembly)

### Enclosure
To fabricate the enclosure you can use your own 3D printer or use a 3D printing service. 

<img src="./images/enclosure.jpg" height="600" />

The folder [enclosure/fabrication](./enclosure/fabrication) contains exported STL files for the [case](./enclosure/fabrication/twomes-hardware-repository-template-case.stl) and [lid](./enclosure/twomes-hardware-repository-template-lid.step) of the Twomes Something device enclosure. The STL files can be imported into any slicer and turned into G-Code for a 3D printer.

## Developing
### Printed Circuit Board
To change the hardware design of the PCB, you need:
* [KiCad](https://www.kicad.org/download/) installed to change te PCB design. 

The KiCad source files of the PCB can be found in the folder [pcb](./pcb).

To convert the PCBs into a format suitable for fabrication, consult the webpage of your PCB manufacturer of choice. For example, see the [JLCPCB guide on how to export Gerbers](https://support.jlcpcb.com/article/149-how-to-generate-gerber-and-drill-files-in-kicad) and the  [JLCPCB guide how to export the BOM and POS files](https://support.jlcpcb.com/article/84-how-to-generate-the-bom-and-centroid-file-from-kicad). You may also use a KiCad plug-in for this purpose such as [kicad-jlcpcb-tools](https://github.com/Bouni/kicad-jlcpcb-tools).

### Enclosure
To change the hardware design of the enclosure, you need either:
* [Autodesk Fusion 360](https://www.kicad.org/download/) installed (Autodesk provides 30 day free trials and [free one-year educational access](https://www.autodesk.com/education/edu-software/overview?sorting=featured&filters=individual) to its products and services for eligible students, teachers and research staff); 
* or [FreeCAD](https://www.freecadweb.org/), an open source alternative.

The source files of the enclosure can be found in the folder [enclosure](./enclosure). We include both .f3d source files and .step source files we obtained after conversion.
## Features
The Twomes Something Shield features the follwoing main hardware components:
* awesome feature 1;
* awesome feature 2;
* awesome feature 3.

To-do:
* wow improvement to be done 1;
* wow improvement to be done 2.

## Status
Project is:  _in progress_, _finished_, _no longer continued_ and why?

## License
The hardware designs in this repository are available under the [CERN-OHL-P v2 license](./LICENSE), Copyright 2022 [Research group Energy Transition, Windesheim University of Applied Sciences](https://windesheim.nl/energietransitie)

## Credits
This software is a collaborative effort of:
* Huub Buter · [@Github_handle_1](https://github.com/<github_handle_1>)
* Mirjam van Wee · [@Github_handle_2](https://github.com/<github_handle_2>)
* Kees Fokker · [@Github_handle_3](https://github.com/<github_handle_3>)
 
Product owners:
* Marco Winkelman · [@MarcoW71](https://github.com/MarcoW71)
* Henri ter Hofte · [@henriterhofte](https://github.com/henriterhofte) · Twitter [@HeNRGi](https://twitter.com/HeNRGi)

We use and gratefully acknowlegde the efforts of the makers of the following designs:

* [Twomes OpenTherm monitor](https://github.com/energietransitie/twomes-opentherm-monitor-hardware), by Research group Energy Transition at Windesheim University of Applied Sciences, licenced under [Apache 2.0](https://raw.githubusercontent.com/energietransitie/twomes-opentherm-monitor-hardware/main/LICENSE)
* [Twomes Temperature Monitor Hardware](https://github.com/energietransitie/twomes-temp-monitor-hardware), by Research group Energy Transition at Windesheim University of Applied Sciences, licenced under [Apache 2.0](https://raw.githubusercontent.com/energietransitie/twomes-temp-monitor-hardware/main/LICENSE)

