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
![Screenshot 2024-04-19 095518](https://github.com/Karthickraja23006120/HALF_ADDER_SUBTRACTOR/assets/139335315/55b088fa-b884-453d-b92c-72d7c46c7532)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**


/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Karthick Raja K
RegisterNumber:212223240066
```
module HalfAddSub(a,b,sum,carry,D,Bo);
input a,b;
output sum,carry,D,Bo;
wire abar;
xor G1(sum,a,b);
and G2(carry,a,b);
not (abar,a);
xor G3(D,a,b);
and G4(Bo,abar,b);
endmodule
```
![Screenshot 2024-04-19 095601](https://github.com/Karthickraja23006120/HALF_ADDER_SUBTRACTOR/assets/139335315/d549e963-258f-4526-aef3-213bf3ca349b)

**RTL Schematic**
![Screenshot 2024-04-19 095627](https://github.com/Karthickraja23006120/HALF_ADDER_SUBTRACTOR/assets/139335315/4be5a7e5-b09b-49be-b02b-9fdacbb730b1)

**Output/TIMING Waveform**
![Screenshot 2024-04-19 095657](https://github.com/Karthickraja23006120/HALF_ADDER_SUBTRACTOR/assets/139335315/ce4f521e-20d8-4aa4-9866-0fbdc2f1a98a)

**Result:**
Thus,a half adder and half subtractor circuit has been designed and its truth table has been verified in Quartus using Verilog programming.
