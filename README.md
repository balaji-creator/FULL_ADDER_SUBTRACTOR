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
FULL ADDER:


<img width="429" height="395" alt="TT2" src="https://github.com/user-attachments/assets/aeb1a9a4-e156-4891-bfe6-f257c8065601" />


FULL SUBTRACTOR:


<img width="438" height="393" alt="TT1" src="https://github.com/user-attachments/assets/04b852e5-87a6-43e2-b878-77683740da4a" />
**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: BALAJI B
RegisterNumber:212225040040
*/
```
FULL ADDER PROGRAM:
```
module Fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=((a^b)^cin);
assign carry=((a&b)|(cin&(a^b)));
endmodule
```
FULL SUTRACTOR PROGRAM:
```
module FullSub(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference=((a^b)^bin);
assign borrow=((~a&b|(bin&(~(a^b)))));
endmodule
```
**RTL Schematic**
FULL ADDER:
<img width="1802" height="877" alt="Screenshot 2025-10-08 114341" src="https://github.com/user-attachments/assets/e674fe8b-d85e-41d0-8464-23259f5fa82d" />
FULL SUBTRACTOR:
<img width="1773" height="855" alt="Screenshot 2025-10-09 141327" src="https://github.com/user-attachments/assets/236addfc-4415-4efd-aed6-425e4ce16d07" />


**Output Timing Waveform**
FULL ADDER:
<img width="1912" height="553" alt="Screenshot 2025-10-09 140231" src="https://github.com/user-attachments/assets/6260b649-53ca-4c44-9b3e-c3aedf03ba40" />
FULL SUBTRACTOR:
<img width="1903" height="498" alt="Screenshot 2025-10-09 141255" src="https://github.com/user-attachments/assets/4a942971-bb3b-4883-9595-0136f1fe964c" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




