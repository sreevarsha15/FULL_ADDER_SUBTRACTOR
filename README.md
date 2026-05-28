# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
```
FULL ADDER 
<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/28f8576c-6aad-453e-96f9-dcd58ed320e2" />
FULL SUBTRACTOR
<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/84e69d98-dab1-4707-8acc-0e2dc3285952" />
```
**Procedure**

1. Open Intel Quartus Prime and create a new project.
2. Create a new Verilog HDL file and write the Verilog code for Full Adder and Full Subtractor.
3. Save the file and compile the design using Start Compilation.
4. Create input waveforms for A, B, Cin/Bin and run the simulation.
5. Verify the outputs with the truth table and confirm the correct operation of the circuits.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: SREE VARSHA D RegisterNumber: 212225040422
*/
```
module exp_3a(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule

FULL SUBTRACTOR:
module exp_3b(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule
```

**RTL Schematic**
FULL ADDER
<img width="1461" height="818" alt="image" src="https://github.com/user-attachments/assets/f57ba0e1-860f-4fee-87c0-294bce73158e" />
FULL SUBTRACTOR 
<img width="1460" height="816" alt="image" src="https://github.com/user-attachments/assets/85afa598-df7d-4f59-8abe-60ff5523f2fa" />

**Output Timing Waveform**
FULL ADDER
<img width="1463" height="825" alt="image" src="https://github.com/user-attachments/assets/6ad642c9-f3b7-4aa7-82c0-319b34d5ad0a" />
FULL SUBTRACTOR 
<img width="1460" height="816" alt="image" src="https://github.com/user-attachments/assets/f7b8e997-07bb-427b-8301-93ca7dbac44e" />

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



