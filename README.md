# Digital-Logic-Design-Whack-a-Mole-Game-based-on-Digital-Systems


This project implements a Whac-A-Mole game on an FPGA board using Verilog and the ISE design suite. The game features a timer, scoring system, and randomized mole appearances that players must hit with buttons.

Overview:
- Utilizes an FPGA board with LEDs, 7-segment displays, and buttons
- Game duration: 60 seconds
- Initial score: 16 points
- 4 random mole locations represented by LEDs
- Hitting a mole: +1 point
- Missing a mole: -1 point

Implementation
The project is divided into several modules:

- Time_: Implements a countdown timer
- Random: Generates random mole locations
- hamster_1, hamster_4: Handles mole appearances and scoring
- Bin2BCD16: Converts binary to BCD for display
- Press, Calculate: Detects button presses and updates the score
The top-level module integrates these components and interfaces with the FPGA board's inputs and outputs.

Challenges:
- Initially aimed to use a VGA display but faced issues with image rendering
- Debugging random mole appearances and LED flickering
- Incomplete implementation of storing the previous game's score

Usage:
- Program the FPGA board with the provided Verilog files
- Set the game reset switch (SW15) to 1, then 0 to start the game
- Press the buttons (BTN0-BTN3) to hit the moles represented by the LEDs
- The 7-segment displays show the remaining time and current score

Notes:
This project was developed as part of a course requirement and provides insights into FPGA design, Verilog coding, and hardware-software integration. While some features were not fully implemented, the core gameplay functionality was achieved.

