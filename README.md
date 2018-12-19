Stacker  is  a  common  game  in  arcades  and  theme  parks.   Players  attempt  tostack  rows  of  blocks  on  top  of  each  other  in  hopes  of  winning  big  prizes.   Ifthe player fails to stack the blocks, the game is lost and they have to restart.  This concept was deemed ideal to create on the MSP430G2553.  Utilizing serial communication,  the MSP430 controlled a matrix of LEDs with shift registers.

The goal of Stacker is to align rows of moving blocks on top of each other.  Bypressing a start/stop button, the user can ’stack’ one row of blocks and if it isstacked directly on top of the previous row, the next row begins.  In this project,stacking seven consecutive rows of LEDs on top of each other results in a win.As the user moves up the rows, the rows afterwards begin to move faster andfaster.  This increases the game’s difficulty.  If the user misses the stack, theylose the game and it resets to the first row.

# Connecting the board
If using a breadboard, the project uses all the I/O pins of the MSP430G2553 (G2).  Pins 1.1 to 1.7 are used for the shift registers' inputs.  Each pin correlates to a row (i.e. Pin 1.1 is connected to the first shift register/first row).  Pins 2.1 to 2.7 are used for the shift registers' latches.  Pin 1.0 is a common clock that all registers share while pin 2.0 is the button's input.

# Powering the board
In order to supply the G2 with enough power, 2 AAA batteries are used.  These output 1.5V each and are placed in serial.  This results in 3V total.

# Initializing the game
When powering up the game, the shift registers are loaded with random values.  This is because they recieve random noise and interferrence from the G2.  In order to start the game, the start/stop button must be pressed twice to reset the board and clear the registers.

# Adjusting the game settings
In order to increase the game's difficulty, each level increases the stack shifting speed.  This is done in the software by decreasing the CCR0 value every level.
