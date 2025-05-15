# Bambu Waste Conveyor
Plans, model files, etc., for a conveyor that can remove waste from multiple Bambu P-class or X-class printers sitting next to each other.

## Background:
Bambu P1 and X1 series printers often have to purge filament from their hotends, resulting in small amounts of waste filament[^1] that is expelled out the back of each printer and must then be disposed of. The maker space where I work has rows of these printers on shelves. It is difficult and dangerous to move the printers to remove the wastes, and worse, allowing the waste receptacles to overflow to the point where the wastes stay near the hotend can result in a clog that may require significant disassembly and can take hours to fix.

What you're seeing here is my attempt at a conveyor belt that will sit behind any (reasonable) number of printers, automatically activate when enough waste piles up, transporting it to one end where presumably a large receptacle will catch them, then turn back off.

> [!NOTE]
> At the time of writing, the drive mechanism is not fully automated. Instead, the conveyor is actuated manually using a power screwdriver with a standard 6.35mm (1/4-inch) hex drive.

[^1]: To keep this family-friendly, I have avoided using the more common term for this waste. 💩

## Description:
The conveyor itself consists of a loop of roller chain that should be a bit longer than twice the length of the conveyor. The chain links are constructed out of 3D-printed rollers, inner links, and outer links. There is no "Master" link; because everything is pressure-fitted, any link can be opened when needed.

The outer links have aquare pegs (get it?) protruing outward that each hold a platform, which is laser cut from 3mm basswood. The chain-with-platform rides in a track. Under the track are the driven sprocket, idler sprocket, and tensioner sprocket. The driven sprocket connects directly to the spindle of the stepper motor. The other two use 608-form factor bearings. The entire assembly is configured such that the space needed behind the printers is no more than the platform width (100mm as I built it) plus 8mm for the track wall. The height is optimized for these particular printers, but it can be modified for other printer brands.

## Tools and environment
This project was created on an Apple Mac Mini using using the 2024.04.01 developer snapshot of [OpenSCAD](https://openscad.org/).[^1] The resultant `.stl` files are included in this repository, but can also be built noninteractively using any reasonably recent versions of [CMake](https://cmake.org/) and [GNU Make](https://www.gnu.org/software/make/). The `.stl` files have been successfully imported into version 2.0.3 of [Bambu Studio](https://bambulab.com/en-us/download/studio) and have been successfully printed using PLA and PETG[^2], on Bambu [X1-C](https://us.store.bambulab.com/products/x1-carbon) and [P1-S](https://us.store.bambulab.com/products/p1s)  printers.

[^1]: The last "official" release of OpenSCAD is 2021.01. Recent developer snapshots contain many new features yet are quite stable. 
  The code in this project has not been tested using the 2021.01 version and I would not expect it to work.
[^2]: I use mopstly Bambu-branded filament because it plays nicely with my AMS units, but other brands have worked just as well.

## AI Disclosure
I have spent most of my adult life writing Makefiles for a wide variety of `make` tools going back to the original [Feldman `make` on AT&T Unix System III](https://onlinelibrary.wiley.com/doi/epdf/10.1002/spe.4380090402) (paywalled, sorry). However, I didn't want to restrict the ability to build the model files to just Unix/Linux-like systems, so I decided to use CMake to take advantage of its built-in multi-OS capabilities. I am not very good at CMake, so I asked Google's AI to write me a simple `CMakeLists.txt` file as a starting point. This fact is noted in the commentary in that file.

## Licenses
<a href="https://github.com/edhorch/bambu-waste-conveyor">Bambu Waste Conveyor</a> is copyright © 2025 by <a href="https://github.com/edhorch">Edward B. Horch</a>.

All source code, including, but not limited to, the `.scad` files in this repository, is is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

All project documentation, inclusing this document, is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a><img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/sa.svg" style="max-width: 1em;max-height:1em;margin-left: .2em;">

These licenses do not prohibit this content from being used for AI training. Notwithstanding my own use of AI as disclosed above, however, I respectfully ask that my work not be used for this purpose.
