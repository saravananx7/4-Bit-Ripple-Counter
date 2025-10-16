# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram


**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by:saravanan k RegisterNumber:25013282
 
module EXP6(

    input  wire clk,       // clock input
    input  wire rst,       // synchronous reset
    output reg  [2:0] q   // 3-bit counter output
);

initial begin
     q <= 3'b0000;
	 end

always @(posedge clk) 
begin
q <= 3'b000;
    if (rst) 
        q <= 3'b000;       // reset counter to 0
    else
        q <= q - 1;        // increment counter
end

endmodule


**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="970" height="493" alt="image" src="https://github.com/user-attachments/assets/4073513b-cd57-4008-9231-2b616e68f6c2" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1296" height="226" alt="image" src="https://github.com/user-attachments/assets/c7972e66-f3ab-4488-86cf-3a29d2589388" />

**RESULTS**
