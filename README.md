 AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


 Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule



FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule


Developed by: M.ABINAYA

RegisterNumber: 22008642 

LOGIC GATES

![Screenshot (14)](https://user-images.githubusercontent.com/121557017/211147329-e455ae2d-3b20-41fc-af83-fab6a5a90bcb.png)


OUTPUT
RTL REALIZATION

HALF SUBTRACTOR


![Screenshot (18)](https://user-images.githubusercontent.com/121557017/211147336-e584ec70-9473-4a57-9ff3-b0653994fdec.png)



FULL SUBTRACTOR

![Screenshot (19)](https://user-images.githubusercontent.com/121557017/211147361-6dd98522-f508-4552-8473-8712d1dd4676.png)


TIMEING DIAGRAM

HALF SUBTRACTOR

![Screenshot (20)](https://user-images.githubusercontent.com/121557017/211147374-0036cdef-85ea-41e0-a217-3229b1338400.png)



FULL SUBTRACTOR

![Screenshot (21)](https://user-images.githubusercontent.com/121557017/211147914-a9427f5d-1841-44f5-a751-44453da5d1c5.png)



 Truthtable


HALF SUBTRACTOR

![Screenshot (15)](https://user-images.githubusercontent.com/121557017/211147941-86fd6cc0-aa0c-4ddc-98da-685096df195b.png)

FULL SUBTRACTOR

![Screenshot (16)](https://user-images.githubusercontent.com/121557017/211147946-523069f3-fb17-4191-995f-4229c5c730ee.png)


Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
