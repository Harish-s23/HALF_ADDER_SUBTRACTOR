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

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

module half_add(a,b,bin,cy,df);
 input a,b,bin;
 output cy,df;
 xor(sm,a,b);
 and(bo,~a,b);
 wire w1,w2,w3;
 assign w1=a^b;
 assign w2=(~a&b);
 assign w3=(~w1&bin);
 assign df =w1^bin;
 assign bo=w2|w3;
 endmodule
module half_sub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference= (a ^ b);
assign borrow= ( ~a & b);
endmodule

Developed by:Haresh R
RegisterNumber:24901004

**RTL Schematic**
![Screenshot 2024-12-13 232842](https://github.com/user-attachments/assets/e9cb97a2-3943-4bfd-b734-20db5a6d4eba)
![Screenshot 2024-12-13 232825](https://github.com/user-attachments/assets/fb270949-3382-4214-be5e-e76e2bceec7f)


**Output/TIMING Waveform**
![Screenshot 2024-12-13 233019](https://github.com/user-attachments/assets/f7845775-d040-49c5-a935-f4016b87b4e3)
![Screenshot 2024-12-13 233003](https://github.com/user-attachments/assets/53616878-7786-4438-9dbd-c30fa94c7f9a)


**Result:**
hence the programm for half adder and half subtractor nd verification of its
 truth table in quartus using verilog programming is verified
