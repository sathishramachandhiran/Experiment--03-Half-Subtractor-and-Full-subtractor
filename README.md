# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
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
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SATHISH R
RegisterNumber: 22009045
```
```
### PROGRAM FOR HALF SUBTRACTOR:
module expthree(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
```
```
### PROGRAM FOR FULL SUBTRACTOR:
module expfour(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference=(a^b^c);
assign borrow=(~a&(b^c)|(b&c));
endmodule
```

## Output:
### HALF SUBTRACTOR
## Truthtable
![half table](https://user-images.githubusercontent.com/120574768/211187090-e47d8ef2-3315-499d-88c7-196ef70db7c7.png)

##  RTL realization
![half sub](https://user-images.githubusercontent.com/120574768/211187098-73bdafa0-c24f-4c52-b046-2f50b397fc18.png)


## Timing diagram 
![half timing](https://user-images.githubusercontent.com/120574768/211187104-3fef04db-407a-421e-b30b-4f5a8e5f2f81.png)

## FULL SUBTRACTOR

## Truthtable
![full table](https://user-images.githubusercontent.com/120574768/211187112-e44f70ef-80e9-4699-8802-0a35807b6cf5.png)

##  RTL realization

![full sub](https://user-images.githubusercontent.com/120574768/211187125-f20c4c82-d02b-4cb2-ad3c-dd61c24ee494.png)

## Timing diagram 
![full timing](https://user-images.githubusercontent.com/120574768/211187138-4e896935-7fa2-4cd5-8709-ccb2bca32f89.jpg)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
