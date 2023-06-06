# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Using NOR GATES
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

 

## Logic Diagram
![Screenshot 2023-04-23 205318](https://user-images.githubusercontent.com/121165938/233848623-c2ad4223-5864-46b9-88b5-0a7ee7778233.png)

## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:

```Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Gokul J
RegisterNumber: 212222230038
```
### F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
```
module f1(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule
```
### F2=xy’z+x’y’z+w’xy+wx’y+wxy
```
module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
```

## Output:

## RTL
### F1
![Screenshot 2023-06-06 130341](https://github.com/Gokul0117/Experiment--02-Implementation-of-combinational-logic-/assets/121165938/66bb4d66-1f09-448e-9fcb-e2bfefaed9b3)

### F2
![Screenshot 2023-06-06 130516](https://github.com/Gokul0117/Experiment--02-Implementation-of-combinational-logic-/assets/121165938/1cb32153-5714-4610-9b0b-25f5462949ad)


## Timing Diagram
### F1
![Screenshot 2023-06-06 130619](https://github.com/Gokul0117/Experiment--02-Implementation-of-combinational-logic-/assets/121165938/7412485d-1556-4931-b632-44c8d5b81a88)

### F2
![Screenshot 2023-06-06 130813](https://github.com/Gokul0117/Experiment--02-Implementation-of-combinational-logic-/assets/121165938/b9896c23-2035-43be-a8a7-e193de46975b)



## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
