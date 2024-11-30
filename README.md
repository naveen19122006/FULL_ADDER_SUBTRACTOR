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

**Procedure**

Write the detailed procedure here

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:NAVEEN KUMAR E

Register Number:24006129


FULL ADDER 

~~~
module fulladder(a,b,cin,sum,carry);
input a;
input b;
input cin;
output sum;
output carry;
assign sum=(a^b^cin);
assign carry=(a&b)|(b&cin)|(cin&a);
endmodule

~~~

FULL SUBRACTOR

~~~
module fullsubractor(a,b,cin,diff,borrow);
input a;
input b;
input cin;
output diff;
output borrow;
wire abar;
assign abar=~a;
assign diff=a^b^cin;
assign borrow=(abar&b)|(b&cin)|(cin&abar);
endmodule
~~~

**RTL Schematic**

FULL ADDER 

![Screenshot 2024-11-30 220639](https://github.com/user-attachments/assets/627017f8-b72c-41dc-9789-523987166bf7)


FULL SUBRACTOR

![Screenshot 2024-11-30 220939](https://github.com/user-attachments/assets/836c9ac4-8d3c-4189-97fb-652c4250f54a)


**Output Timing Waveform**

FULL ADDER

![Screenshot 2024-11-30 214353](https://github.com/user-attachments/assets/56d38bb8-1452-4f48-9dc1-82e919e58742)
FULL SUBRACTOR

![Screenshot 2024-11-30 221510](https://github.com/user-attachments/assets/22ccb733-912d-4e3b-a613-b1cf73d205e5)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



