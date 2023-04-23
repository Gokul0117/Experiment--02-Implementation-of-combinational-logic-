# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 

## Logic Diagram
## Procedure
## Program:

```Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Gokul J
RegisterNumber: 212222230038

module fourexp(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

USING NOR OPERATION

module fourexp(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
assign F = ~S;
endmodule
```


## RTL realization

## Output:

## RTL

NAND combination : 
![Screenshot 2023-04-23 204013](https://user-images.githubusercontent.com/121165938/233848007-2bd15509-2586-4909-920d-64ca5eeaca2f.png)

NOR combination :
![Screenshot 2023-04-23 204630](https://user-images.githubusercontent.com/121165938/233848246-2124b870-c03a-46ba-8aed-52872a301776.png)



## Timing Diagram

NAND combination:

![Screenshot 2023-04-23 204645](https://user-images.githubusercontent.com/121165938/233848270-46a94be8-11e4-40a5-9fd2-99e54a1084ca.png)

NOR combination :

![Screenshot 2023-04-23 204729](https://user-images.githubusercontent.com/121165938/233848322-2e2747c4-92eb-4513-a1e7-a88318bc6510.png)



## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
