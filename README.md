# bambu-waste-conveyor
Plans, model files, etc., for a conveyor that can remove poop, er, waste from multiple Bambu P-class or X-class printers sitting next to each other.

## Background:

The maker space I work at has rows of Bambu P-class and X-class printers on shelves up against walls. Nobody wants to have to pull these out to remove the poops the printers produce. What you're seeing here is my attempt at a conveyor belt that will sit behind any (reasonable) number of printers, automatically activate when enough poop piles up, carrying it to one end where presumably a large receptacle will catch them, then turn back off.

## Description:

The conveyor itself consists of a loop of roller chain that should be a bit longer than twice the length of the conveyor. The chain links are constructed out of 3D-printed rollers, inner links, and outer links. There is no "Master" link; because everything is pressure-fitted, any link can be opened when needed.

The outer links have aquare pegs (get it?) protruing outward that each hold a platform, which is laser cut from 3mm basswood. The chain-with-platform rides in a track. Under the track are the driven sprocket, idler sprocket, and tensioner sprocket. The driven sprocket connects directly to the spindle of the stepper motor. The other two use 608-form factor bearings. The entire assembly is configured such that the space needed behind the printers is no more than the platform width (100mm as I built it) plus 8mm for the track wall. The height is optimized for these particular printers, but it can be modified for other printer brands.

<a href="https://github.com/edhorch/bambu-waste-conveyor">Bambu Waste Conveyor</a> © 2025 by <a href="https://github.com/edhorch">Edward B. Horch</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a><img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/sa.svg" style="max-width: 1em;max-height:1em;margin-left: .2em;">
