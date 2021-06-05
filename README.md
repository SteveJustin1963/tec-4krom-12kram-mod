This project is to convert back to full 4k rom and keep ram in 2k increments, but we loose one of the 2k rams thus 1+5 =12k max.
The tec1's rom is 4k split into 2 x 2k roms via high address line switch, one 2k rom is active at a time. The ram is 2k blocks that can be added via stacking or a addon pcb, maxin out at 1+6 ram chip=14k (14,336k). see magazine TE-12-28.  
This is sufficent to boot a monitor or a skinny forth system but 4k rom is a better option, 8k would be ideal.

While RAM and ROM are both 2k blocks, addressing is decoded from A0,A1,A2, 000-111, into 8 ports from a 74138. The ROM is select 0, the 0800h-3800h RAM from 1-7 (6).
When we address ROM as 4k, 0000h-07FFh, it will overlap with 1 slect line of RAM.
A solution proposed by Craig Hart "...in that case there is another approach. 
* Leave the '138 wired as is. 
* take an AND gate and hook Y0 and Y1 from the 138 to it. 
* The output of this gate is your ROM /CS. 
* Y2 becomes your RAM /CS 
* and your RAM starts at 0x1000. 
* If you need a second 2K+ chips, wire it's /CS to Y3,4,5,... to output of the '138."




https://easyeda.com/editor#id=ca7f0e34e8fe4a03bffd24e4f2ac7bdb

![](https://github.com/SteveJustin1963/tec-4krom-12kram-mod/blob/master/pics/4%2B12mod.png)

![](https://github.com/SteveJustin1963/tec-4krom-12kram-mod/blob/master/pics/pic%20mod.png)

https://github.com/SteveJustin1963/tec-BOOKS/blob/master/TE/Mag/talking_electronics_12.pdf
