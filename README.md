# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

EXP-10

DATE- 3-12-2024

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */

1.Type the Verilog program in Quartus Prime to implement the 4-bit Serial-In Serial Out (SISO) Shift Register.

2.Compile and run the program to ensure the design is error-free.

3.Generate the RTL schematic to visualize the cascading D flip-flop connections and save it for documentation.

4.Create nodes for the serial input (SI), clock (CLK), and serial output (SO) to observe the shifting process during simulation.

5.Simulate the design for different input serial data patterns and observe the timing
diagrams.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.*/

module siso (clk, sin, q);

input clk;

input sin;

output [3:0] q;

reg [3:0] q;

always @(posedge clk)

begin

q[0] <= sin;

q[1] <= q[0];

q[2] <= q[1];

q[3] <= q[2];

end

endmodule

Developed by:JEEVIKA R

RegisterNumber: 24900508



**RTL LOGIC FOR SISO Shift Register**

![image](https://github.com/user-attachments/assets/5ea36390-16ac-41b3-8aae-f0afbaf7323a)

**TIMING DIGRAMS FOR SISO Shift Register**

![image](https://github.com/user-attachments/assets/622a1b94-15c7-44fd-a271-997913e62d83)

**BASIC DATA MOVEMENT THROUGH A SHIFT REGISTER**

![image](https://github.com/user-attachments/assets/25007fd4-ff85-4dc3-99b7-6c2b5c7f4b32)


**RESULTS**

Thus, the Serial-In Serial-Out (SISO) Shift Register is implemented using Verilog, and its functionality is validated with the truth table and timing diagrams
