 HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
![Screenshot 2024-12-09 182732](https://github.com/user-attachments/assets/24c87353-5680-4922-af74-089e81391d91)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:ASHIKA TR RegisterNumber:24900481
```
module ha(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum= (a^b);
assign borrow= ( a&b);
endmodule
```

```
module hs(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference= (a^b);
assign borrow= ( ~a&b);
endmodule
```




**RTL Schematic**

Half Adder
![Screenshot 2024-11-11 232329](https://github.com/user-attachments/assets/4e552ca5-bac1-427e-8ae8-6ce91c29f0c3)

Half Subractor
![Screenshot 2024-11-11 232840](https://github.com/user-attachments/assets/f1e1e936-70ca-43ad-af02-b95a24431023)

**Output/TIMING Waveform**

Half Adder
![Screenshot 2024-11-11 232444](https://github.com/user-attachments/assets/8ab20a8a-05ea-41d3-9acd-33066897507e)

Half Subractor
![Screenshot 2024-11-11 232947](https://github.com/user-attachments/assets/6da89532-4c48-4df9-8ec1-9e50cc1f7dcf)



**Result:**
Thus the truth table of  half adder and half subtractor in QuartusII using Verilog programming is verified.

