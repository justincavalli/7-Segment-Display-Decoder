# 7-Segment Display Decoder

## Introduction
 Our group was tasked with coding a 7 segment Display Decoder with an orientation of upside up with an active low signal. Essentially, an active low signal means a function is accomplished when the input is in a low state. Now, one of the benefits of an active low signal is that it helps eliminate problems with voltage supplies. Meaning, it is easier to pull-down a signal to ground than pull-up a signal, which is between a resistor and the power 

## Plan
Following the directions of the lab slides, the plan was to fill out the truth table in accordance with the pictured seven segment display, and use the outputs to write the verilog code for the correct implementation. Each team member was tasked with filling in the output for multiple hex digits by ‘activating’ the corresponding segments as shown in the picture. Each output was to be verified by all the other members of the team, so that we could add this into the cloned initial code from github. Testing followed to verify the display functioned exactly as intended.

## Implementation
I was responsible for filling out a portion of the spreadsheet, shown in figure 1, that held information about what bits needed to be turned on to display a certain number. After completing the spreadsheet each member of the team verified that the information was correct. Next I set up the wires to connect the 7-segment display to the chip on the breadboard. From there I cloned the initial code from the github repository, and edited it to display 0 to F on the 7-segment display using the information in the spreadsheet. Since the 7-segment display is active low the ~ needed to be removed because we were assigned active low upside up.

## Results
The project had 2 goals that needed to be meet:</br>
1. Displaying our team letter “F” on the 7-segment display 
1. Counting from 0 to F on the 7-segment display

The first objective listed above was completed on the first attempt. The output was the letter “F” displaying in this order on display: F, FF, FFF, FFFF, repeat. 

The second objective failed on the first attempt as some numbers were not mapped to the correct output. For example, 7’b0001000 would need to be 7’b0010000. This error was corrected by referring to our  physical sheet where we wrote down the correct mappings. Each case statement condition was checked in the Verilog code, and the necessary changes were made. On the second attempt, the FPGA executed as expected.

## Conclusion
Overall, 
While we had a couple of missteps. Namely, an error entering in the correct bits as well as a couple wires in the wrong place; however, all the tests passed successfully after the correction.  
