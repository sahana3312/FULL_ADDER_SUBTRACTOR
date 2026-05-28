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

module ADD3(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule

FULL SUSTRACTOR

module SUB3(df, bo, a, b, bin);

    output df;
    output bo;

    input a;
    input b;
    input bin;

    wire w1, w2, w3;

    assign w1 = a ^ b;
    assign df = w1 ^ bin;

    assign w2 = (~a) & b;
    assign w3 = (~w1) & bin;

    assign bo = w2 | w3;

endmodule
```
**RTL Schematic**


#FULL ADDER

<img width="752" height="350" alt="image" src="https://github.com/user-attachments/assets/a6bf97dc-ebf5-4afa-9d2a-a3674b12c344" />

#FULL SUBTRACTOR

<img width="792" height="352" alt="image" src="https://github.com/user-attachments/assets/e62ca824-643a-49e4-aa8c-83782cd775d8" />


**Output Timing Waveform**

#FULL ADDER 

<img width="1037" height="548" alt="image" src="https://github.com/user-attachments/assets/a0935fae-d194-472c-9552-6eeb123f4011" />

FULL SUBTRACTOR

<img width="1032" height="543" alt="image" src="https://github.com/user-attachments/assets/2173c69b-665b-455f-ba0a-5b4ae4a375f1" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



