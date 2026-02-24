(i) OBJECTIVE: 
To design, implement, and simulate a Digital Lock System using Verilog HDL.

(ii) INTRODUCTION:
A digital lock system offers an electronic solution for access control, replacing traditional mechanical locks. This design is implemented using a finite state machine (FSM) model that processes a predefined key sequence serially. Only the correct sequence triggers the 'unlock' signal. This approach offers reliability, reprogrammability, and ease of integration into larger systems like smart homes or secured labs.

(iii) SOFTWARE:
- Tool Used: Synopsys
- Components Used:
  * Verdi: For waveform analysis and debugging
  * Design Compiler: For synthesis and gate-level analysis (if needed)
  * ICC: Floor Planning, Power Planning, Placement Planning, Clock-Tree Synthesis and Routing.

(iv) DESCRIPTION: 
The Digital Lock System is built around a finite state machine that detects a 4-bit key sequence: 1011. The lock starts in a reset state and transitions between states on every clock cycle based on the key input. If the exact sequence is entered, it activates the unlocked output.
Functional Details:
* States: S0 to S4, representing progression in key detection.
* Reset: Brings the FSM to initial state (S0).
* Key Input: 1-bit serial input representing each bit of the key.
* Unlocked Output: Goes high for one cycle when the key 1011 is correctly entered.

(v) DESIGN: 
The system is designed as a Moore FSM, where the output (unlocked) is determined by the state. The correct input sequence (1011) transitions the FSM through S0 → S1 → S2 → S3 → S4, with S4 being the unlock state.

