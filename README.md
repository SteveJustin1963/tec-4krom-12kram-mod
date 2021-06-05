The tec1's rom is 4k split into 2 x 2k roms via high address line switch, one 2k rom is active at a time. The ram is 2k blocks that can be added via stacking or a addon pcb, maxin out at 1+6 ram chip=14k. 

This project is to use the full 4k rom and keep the ram addressed in 2k increments, doing this reduces one 2k block thus max ram is now 1+5 =12k. The high rom line is restored to the address bus, and a AND gate is placed on the ram select line.


https://easyeda.com/editor#id=ca7f0e34e8fe4a03bffd24e4f2ac7bdb

![](https://github.com/SteveJustin1963/tec-4krom-12kram-mod/blob/master/pics/4%2B12mod.png)

![](https://github.com/SteveJustin1963/tec-4krom-12kram-mod/blob/master/pics/pic%20mod.png)
