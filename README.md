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

FULL ADDER 

<img width="938" height="645" alt="image" src="https://github.com/user-attachments/assets/07dc6439-d405-4637-96df-6944802ec1de" />

FULL SUBTRACTOR

<img width="780" height="680" alt="image" src="https://github.com/user-attachments/assets/705ff4a1-628e-4d8c-8a91-63ab7fc15263" />



**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:SAHANA S 
RegisterNumber:25015837
```
```
FULL ADDER

module experiment4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule


FULL SUSTRACTOR


module experiment4a (df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(-w1&bin);
assign df-w1^bin;
assign bo-w2/w3;
endmodule
```
**RTL Schematic**


#FULL ADDER

<img width="573" height="298" alt="image" src="https://github.com/user-attachments/assets/184e5686-0b57-4ac4-8f7d-cd75923d2467" />


#FULL SUBTRACTOR

<img width="376" height="181" alt="image" src="https://github.com/user-attachments/assets/a352791b-442b-499a-b1e2-e45b55467203" />



**Output Timing Waveform**

#FULL ADDER 


<img width="1022" height="418" alt="image" src="https://github.com/user-attachments/assets/6622fc0f-5e22-4eeb-b5ca-fa46ad551089" />

FULL SUBTRACTOR

<img width="1031" height="486" alt="image" src="https://github.com/user-attachments/assets/0af1d8c9-97b3-4f21-859c-627a499d0612" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



