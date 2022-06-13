# Jim's Purgatory - Computer Science 599.82 Term Project

An original game created for the Commodore Vic-20 written in 6502 Assembly. Entire project runs in 3.5KB of memory utilizing screen memory to store map data.

Created by:
- Jacob Huber
- Karen Kuribayashi
- Debprasad Mandal
- Eddy Qiang

Compiled using DASM

## Gameplay
<img src="https://user-images.githubusercontent.com/16791782/173258290-ed1bd8e2-3443-4f9d-9d3f-ead000fbd3cb.png" width="600"/>

### Rules:

Try to earn as much score as possible by moving around and eatting flies while 
not falling down into the lava. You have three lives.

### Controls:

'A' and 'D' keys are used to move the frog left and right respectively.

'SPACE' is used to jump and navigate the menus. Jumping diagonally is done by jumping while moving.

**(Debug):** 'RETURN' is used to restart the game.

## Marking

The items that are listed here may be difficult to find but are important components for marking.

### Run-Length Encoding

RLE was implemented in two separate files.

The first file, **characterSet.s**, is used to store animated sprites with RLE of the $00 and $FF bytes as they were repeated the most often.

The second file, **animation.s**, is used to decode the data. This was done in the *load_frame* function which would check if the byte it is loading is encoded or not, then appropriately store it in character memory.

### Procedural Content Generation

Our game implements all of its levels through PCG, which is done in the file **pcg.s**.
