# Experiment-03 Implementation of Half Subtractor and Full subtractor

## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

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
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SOWMYA V
RegisterNumber: 212222110045

HALF SUBTRACTOR:
module halfsubtraction (a,b,diff,borrow);
input a,b;
output diff,borrow;
assign diff = (a^b);
assign borrow = ~a&b;
endmodule

FULL SUBTRACTOR:
module fullsubtractor(a,b,bin,diff,borrow);
input a,b,bin;
output diff,borrow;
assign diff= a^b^bin;
assign borrow = (~a&b)|(~(a^b)&bin);
endmodule

```
## Output:
![image](https://github.com/SowmyaVisvanathan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119475775/b86b0277-3edc-4602-a833-c0901e081111)

![image](https://github.com/SowmyaVisvanathan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119475775/f544fe5e-ffa8-45f9-8a91-83910029e28c)

## Truthtable
![image](https://github.com/SowmyaVisvanathan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119475775/9bb9002d-18bf-40a8-8a96-69bec35e4aa4)

![image](https://github.com/SowmyaVisvanathan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119475775/a8382574-34b2-44ca-90e6-a4f88001ca39)


##  RTL realization
![image](https://github.com/SowmyaVisvanathan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119475775/e914821a-7eb7-4db6-8ff0-a56ea0d98a51)

![image](https://github.com/SowmyaVisvanathan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119475775/143429fa-6cab-4e54-90c0-c0fb6771f33e)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
