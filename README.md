# chimera-toolchanger
A tool changing system for Klipper based printers.

## The Intro
I wanted a toolchanger that changes the filament path without changing the entire toolhead. There's a lot of great projects that are either in active development or some stage of published but I wanted something slightly different. This specific project is an attempt to take the things i like and mash them together hence the "chimera" name. 

Many systems are attempting to open the extrusion mechanism through toolhead motion, a servo, or even leveraging the extruder gears. These aren't bad ideas but I wanted to approach a system that's more simple.  I took some time to look at the Flashforge Creator 5, the (Blackbox)[https://blackbox3d.xyz], and even the "teased" armored turtle changer as they all swap gearsets along with the hotend. This adds an additional cost per tool but allows a simpler changing mechanism if done correctly. between these and the awesome folks working on the A4T-C project I ended up assembling this project as a combination of the elements I liked. Specifically this project uses a carriage mounted motor with a 17 tooth bondtech gear that meshes with a set of hgx v2 gears attached to the hotend. Additionally it uses a maxwell coupling (derived from user ycsy in the A4T-C project channel and cxchanger) to achieve repeatable coupling. These mechanisms avoid two of the common elements i see on hotend changers, opening extruders, and pins and bushings. This is not a condemnation of those mechanisms (I'll likely build one of those projects in the future) but rather an experimentation to see where this path leads.

## Toolhead
The toolhead carries the part fans and extruder motor in addition to a tool detection sensor. The motor requires a 5mm shaft for a bond tech-style 17 tooth motor gear that was part of the big gear sets before the smaller nematodes 14 motors with an integrated gear became common. The part cooling fans were designed to be modular and prioritized footprint over capability to try and keep the size of tools minimal. For this reason 3010 blower fans are used. The LDO fans meant for the jabberwocky project provide high static pressure and perform well here. Future fan designs may be adapted but there are other priorities at the time of writing. The Maxwell coupling side on the toolhead uses 6 2x10mm pins and an additional 6 6x3mm round magnets.

The toolhead is designed around the xol carriage though adapting to a standard stealth burner carriage shouldn't be difficult. Testing has been conducted with the standard xol cartographer probe mount though any options that work with xol should work.

## Tools
A tool is composed of a set of hgx v2 gears in a fixed arrangement (no tensioning) with a Bambu X1 style hotend. While a set of gears and a hotend are needed for each tool these can be regularly found for $15 or less each so the cost can be minimized as long as engineering hotends aren't used. A goal here was to be able to mix and match X1 style hotends with a few nice ones and a few cheap ones if desired. A 2510 hotend fan is also used per tool to cool the heatbreak. The maxwell portion of the tool uses 3 4x6mm rounded pins (6mm total length with an approximately 2mm fillet on one end) to interface with the pins on the toolhead carriage. A set of 6 3x6mm magnets attracts it to the toolhead.

The front of each tool has a cover that contains the screws used for docking a tool and a hollow space to manage wires.

## Docks
As I'm prototyping on a 2.4 the current dock is designed to use z motion to lift the tool up and lower it into the cradle then move in y to disengage. I'm also using a 1515 bar across the top of the printer as I has one available to be used for another tool changing system. 

## BOM
`incomplete`
4x6 rounded pins - 3 per tool
2x10mm pins - 6
3x6mm round magnets (n52 preferred) - 6 for toolhead and 6 more per tool
HGX V2 gears - 1 per tool
X1 style hotend - 1 per tool

## Assembly
TODO

The cad will be provided to reference for assembly. I recommend placing the magnets in alternating polarity to provide the strongest connection and alignment forces.





This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
