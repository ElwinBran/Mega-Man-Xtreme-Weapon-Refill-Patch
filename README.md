# Mega Man Xtreme Weapon Refill Patch
This patch for Mega Man Xtreme on the Gameboy Color makes weapon energy refill upon death in the whole game. 
A detailed description can be found [on the RomHacking page of this hack](http://www.romhacking.net/hacks/4827/), as well as an alternative download link.
In this README you will find further information on how this patch was made and reference material.

## Tools
- [The BGB emulator](http://bgb.bircd.org/#downloads), for disassembly, hex editing, memory viewing, testing and even breakpoints.
- [LunarIPS](https://www.romhacking.net/utilities/240/), to create a patch file.

## Process
After the weapon values were found and the Gameboy architecture understood, there was little difficulty in creating the patch.
The method equal to that of the NES patches created for Mega Man.

Instead of using a loop to iterate over the weapon energy offsets, two opcodes were repeated as much as there are weapons. This saved the difficulty of further research into how loops worked and memory space was not an issue either; free space was plenty available. 

## References
In order to write the code a lot of knowledge was required. Here I list the sources specifically used for this project.
A big thanks for the people behind these to make Z80 gameboy programming more accessible.
- [A visual opcode map for the gameboy Z80.](http://pastraiser.com/cpu/gameboy/gameboy_opcodes.html)
- [Detailed descriptions for the opcodes, which were confusing to me without it.](https://raw.githubusercontent.com/gb-archive/salvage/master/txt-files/gb-instructions.txt)
- [The full gameboy memory map explanation.](http://gameboy.mongenel.com/dmg/asmmemmap.html)
