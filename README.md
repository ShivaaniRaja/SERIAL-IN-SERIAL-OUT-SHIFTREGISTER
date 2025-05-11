# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

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

1.Initialize the shift register to a known state (e.g., all zeros). 2.Input a bit serially into the shift register. 3.Shift the contents of the register one position to the right (or left). 4.Output the shifted bit from the last stage of the register. 5.Repeat steps 2-4 for each bit you want to input and shift.

**PROGRAM**

```
1. SERIAL IN SERIAL OUT SHIFT REGISTER
module SISOSR(clock, clear, A, E);
input clock, clear, A;
output reg E;
reg B, C, D;
always @(posedge clock or negedge clear)
begin
if (!clear) begin B=0; C=0; D=0; E=0; end
else begin
E = D;
D = C;
C = B;
B = A;
end
end
endmodule
```

Developed by:R.SHIVAANI
RegisterNumber:212224220097



**RTL LOGIC FOR SISO Shift Register**

![image](https://github.com/user-attachments/assets/3d9e5f3f-99f5-4f88-8aeb-39f1762465b2)



**TIMING DIGRAMS FOR SISO Shift Register**

![image](https://github.com/user-attachments/assets/84c29fd3-f81d-4bad-9bcc-b9924baccda3)


**RESULTS**

SISO Shift Register using verilog and validating their functionality using their functional tables has successful execution of the program.
