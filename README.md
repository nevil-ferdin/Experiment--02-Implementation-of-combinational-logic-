# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
+ F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
+ F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
### Hardware – PCs, Cyclone II , USB flasher
### Software – Quartus prime


## Theory
* A combinational logic circuit implement logical functions where its outputs depend only on its current combination of input values. On the other hand sequential circuits, unlike combinational logic, have state or memory.
* Some logic operations may require more than one logic gate. Different combinations of gates are designed for different operations. The behaviour of the combined logic gates can be determined by constructing a truth table of the combined gates.

## Logic Diagram

![Combinational-Logic-Circuits-1](https://user-images.githubusercontent.com/115524975/233445547-da8f5b1f-2dbb-49ac-a548-3e877a65d354.png)

## Procedure
1. Create a project with required entities.
2. Create a module along with respective file name.
3. Run the respective programs for the given boolean equations.
4. Run the module and get the respective RTL outputs.
5. Create university program(VWF) for getting timing diagram.
6. Give the respective inputs for timing diagram and obtain the results
## Program:


```verilog
Program For F1

module combilogic(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire G1,G2,G3,G4,G5;
assign G1=((~A)&(~B)&(~C)&(~D));
assign G2=((A)&(~C)&(~D));
assign G3=((~B)&(C)&(~D));
assign G4=((~A)&(B)&(C)&(D));
assign G5=((B)&(~C)&(D));
assign F1=G1|G2|G3|G4|G5;
endmodule

```
```verilog
Program For F2

module combilogic(W,X,Y,Z,F);
input W,X,Y,Z;
output F;
wire G6,G7,G8,G9,G10;
assign G6=((X)&(~Y)&(Z));
assign G7=((~X)&(~Y)&(Z));
assign G8=((~W)&(X)&(Y));
assign G9=((W)&(~X)&(Y)); 
assign G10=((W)&(X)&(Y));
assign F=G6|G7|G8|G9|G10;
endmodule
```
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by : P.Nevil Joe Ferdin
RegisterNumber : 212222050041
```
## RTL realization

## Output:
### Output for F1
### RTL
![f1rtl](https://user-images.githubusercontent.com/115524975/233157599-8d141b96-5272-412e-9a23-fab91073abd4.png)

### Timing Diagram
![f1td](https://user-images.githubusercontent.com/115524975/233157616-2af36321-5caf-4354-8c44-6b29ea2d677a.png)

### Output for F2
### RTL
![f2rtl](https://user-images.githubusercontent.com/115524975/233157641-f5367b9b-0bf7-4323-beec-af5fe8b289b6.png)

### Timing Diagram
![f2td](https://user-images.githubusercontent.com/115524975/233157653-2c124554-d30e-408c-8b1b-a92dfdf77b7c.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
