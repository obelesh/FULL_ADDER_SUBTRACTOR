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

![Screenshot 2024-12-22 213140](https://github.com/user-attachments/assets/ed4ca22e-34f1-4374-a3a6-db659052c7ce)

![Screenshot 2024-12-22 213153](https://github.com/user-attachments/assets/dba5193b-a8bb-410b-8e0e-47e69493b15a)

![Screenshot 2024-12-22 213204](https://github.com/user-attachments/assets/1e04ed76-3492-4a66-b785-33387230cc74)

![Screenshot 2024-12-22 213221](https://github.com/user-attachments/assets/38d0c5f9-7094-40ae-b7ec-fea62e05168e)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.Developed by: RegisterNumber:
*/ OBELESH R (24901123)

```
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

```

```
module exp4b(df,bo,a,b,bin);
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

```

**RTL Schematic**

**Full adder**

![Screenshot 2024-12-22 214914](https://github.com/user-attachments/assets/35ee6767-f36a-4e43-89bf-812f33dfe9f2)

**full substractor**

![Screenshot 2024-12-22 214927](https://github.com/user-attachments/assets/3064384a-df78-403c-bb27-a36f46756f9e)


**Output Timing Waveform**

**Full Adder**

![Screenshot 2024-12-22 214945](https://github.com/user-attachments/assets/576dcdaa-85c4-4a51-b0a4-5882b4d9e7ab)

**Full substractor**

![Screenshot 2024-12-22 215002](https://github.com/user-attachments/assets/755c5441-726a-49cb-a1f9-ed444d590759)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



