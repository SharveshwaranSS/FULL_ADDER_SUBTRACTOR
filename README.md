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
FULL SUBTRACTER :
![Screenshot 2024-11-19 173914](https://github.com/user-attachments/assets/6921c3f2-127e-4085-b391-5620ff0ec090)
FULL ADDER :
![Screenshot 2024-11-19 173950](https://github.com/user-attachments/assets/52d03107-8a6c-4840-ab24-9d6b3db2c2da)


**Procedure**

Write the detailed procedure here

**Program:**
FULL SUBTRACTER :
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
FULL ADDER :
module exp5 (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:24900901
*/

**RTL Schematic**
FULL ADDER :
![image](https://github.com/user-attachments/assets/aeebfe19-661d-4179-95a7-d54eb4c136aa)
FULL SUBTRACTER :
![image](https://github.com/user-attachments/assets/b0472105-644f-428a-bd23-ddaaa38fc21a)



**Output Timing Waveform**
FULL ADDER :
![Screenshot 2024-11-19 112014](https://github.com/user-attachments/assets/15189960-7df7-4007-964c-84e7439ee1b5)
FULL SUBTRACTER :
![Screenshot 2024-11-19 173740](https://github.com/user-attachments/assets/63b353ea-2ea9-4e00-948a-83ae43d7105f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



