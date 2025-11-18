# HALF_ADDER_SUBTRACTOR

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
half adder
<img width="254" height="198" alt="tru" src="https://github.com/user-attachments/assets/42b63b81-e62a-475f-8554-af7ef0574fc3" />
half Subtractor
<img width="590" height="345" alt="Halftruthtable" src="https://github.com/user-attachments/assets/adf0ddd4-c3c7-4fe7-875d-94868b8b4834" />


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

half adder

module sumcarry(a,b,s,c);

input a,b;

output s,c;

xor g1(s,a,b);

and g2(c,a,b);

endmodule

half subtractor

module diffb(a,b,B,D);

input a,b;

output B,D;

assign D=(a^b);

assign B=(~a&b);

endmodule




**RTL Schematic**
half adder
<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/85e8a454-6b81-451f-8822-0d2d2e908112" />

half subtractor
<img width="1920" height="1080" alt="Screenshot (96)" src="https://github.com/user-attachments/assets/4f970ad9-0842-4d32-bf79-299857ca94c6" />



**Output/TIMING Waveform**
<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/16ca5a32-af4f-4484-a0db-7a59c8cc43d0" />

half subtractor
<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/9c9e7baf-b1cf-454c-aba7-c75a9f096e5f" />

**Result:** 
Thus the given logic combinational circuits are implemented using and their operations are verified using Verilog programming.
