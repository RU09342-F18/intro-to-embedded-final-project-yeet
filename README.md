Stacker  is  a  common  game  in  arcades  and  theme  parks.   Players  attempt  tostack  rows  of  blocks  on  top  of  each  other  in  hopes  of  winning  big  prizes.   Ifthe player fails to stack the blocks, the game is lost and they have to restart.  This concept was deemed ideal to create on the MSP430G2553.  Utilizing serial communication,  the MSP430 controlled a matrix of LEDs with shift registers.

The goal of Stacker is to align rows of moving blocks on top of each other.  Bypressing a start/stop button, the user can ’stack’ one row of blocks and if it isstacked directly on top of the previous row, the next row begins.  In this project,stacking seven consecutive rows of LEDs on top of each other results in a win.As the user moves up the rows, the rows afterwards begin to move faster andfaster.  This increases the game’s difficulty.  If the user misses the stack, theylose the game and it resets to the first row.

