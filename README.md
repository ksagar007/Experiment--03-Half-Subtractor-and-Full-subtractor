# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
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
1.Connect the supply (+5V) to the circuit
2.Switch ON the main switch
3.If the output is 1, then the led glows.



## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: K Sagar Krishna
RegisterNumber:  212222110037
*/
### Half Adder
```
module HalfSubtractor(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference = (A ^ B);
assign Borrow = (~A & B);
endmodule 

```
### Full Adder
```
module FullSubtractor(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (~A &(B ^ C) | (B & C));
assign Borrow = ( A^B^C);
endmodule

```
## Output:



## Half Subractor
## Truthtable:
![output](https://user-images.githubusercontent.com/121117266/233019093-6afe4766-bf66-46c2-98eb-738ef543058a.png)
## Logic Diagram:
![output](https://user-images.githubusercontent.com/121117266/233019226-7d044551-908d-42dc-a8c9-d51fa2c38c54.png)
## RTL realization:
![output](https://user-images.githubusercontent.com/121117266/233019413-f4133c5f-a771-4516-8c64-e04f4a3af296.png)
## Timing diagram
![output](https://user-images.githubusercontent.com/121117266/233019578-1e94a96c-79b1-4e24-b9ae-ff98a88f52fd.png)

## Full Subractor
## Truthtable:
![output](https://user-images.githubusercontent.com/121117266/233019115-34b8e1cf-216b-49eb-9231-46ab34090dd8.png)
## Logic Diagram:
![output](https://user-images.githubusercontent.com/121117266/233019310-d7f768a5-0615-4e79-bf5f-b6348f736a08.png)
## RTL realization:
![output](https://user-images.githubusercontent.com/121117266/233019477-6bf66d6d-3c50-475f-88e6-288a73199ef3.png)
## Timing diagram
![output](https://user-images.githubusercontent.com/121117266/233019633-6ab6b0e2-3a93-4626-ba45-e99635c9a43b.png)





## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
