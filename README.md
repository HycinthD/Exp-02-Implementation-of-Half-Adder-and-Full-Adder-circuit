# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Hycinth D
RegisterNumber:23006688  
*/
##Code

module Hycinth(x,y,s,c);
input x,y;
output s,c;
xor(s,x,y);
and(c,x,y);
endmodule

module full_adder(x, y, z, s, c, x1, x2, x3);
input x,  y,z;
output s ,c, x1, x2, x3;
xor(x1, x, y);
xor(s, x1, z);
and(x2, x, y);
and(x3, x1, z);
or(c, x2, x3);
endmodule

##Truth Table

![image](https://github.com/HycinthD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870810/7d0d8513-8fa8-4612-a1ee-895a84b250ce)
![image](https://github.com/HycinthD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870810/7ac27403-4991-46d5-b82f-548ec0a84d91)

## RTL Diagram

![image](https://github.com/HycinthD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870810/0ff3d257-8c75-4e5b-988a-d75416b015e6)

Result:
Therefore,half adder and full adder is verified

Result:
Therefore,half adder and full adder is verified
![image](https://github.com/HycinthD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870810/cf766324-1140-4ba3-bb84-6c80584d83f5)

## Timing Diagram

![image](https://github.com/HycinthD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870810/8dfb85fa-5a1c-407e-90ba-86d91a50a9c5)
![image](https://github.com/HycinthD/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870810/8c401faa-f31b-4a7d-bbcc-a553636511bf)

