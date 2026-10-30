# chimera-toolchanger
A tool changing system for Klipper based printers.

## The Intro
I wanted a toolchanger that changes the filament path without changing the entire toolhead. There's a lot of options that are either in active development or even some stage of published but all have some kind of tradeoff. This specific project is an attempt to take the things i like and mash them together hence the "chimera" name. 

Many systems are attempting to open the extrusion mechanism through toolhead motion, a servo, or even leveraging the extruder gears. These aren't bad ideas but I wanted to approach a system that's more simple.  I took some time to look at the Flashforge Creator 5, the Blackbox CE, and even the "teased" armored turtle changer as they all swap gearsets with the hotend. This adds a cost per tool but allows a simpler changing mechanism if done correctly. between these and the awesome folks working on the A4T-C project I ended up assembling this project as a combination of the elements I liked. Specifically this project uses a carriage mounted motor with a 17 tooth bondtech gear that meshes with a set of hgx v2 gears attached to the hotend. Additionally it uses a maxwell coupling (derived from user ycsy in the A4T-C project channel and cxchanger) to achieve repeatable coupling. These mechanisms avoid two of the other common elements i see on hotend changers, opening extruders, and pins and bushings. 


This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
