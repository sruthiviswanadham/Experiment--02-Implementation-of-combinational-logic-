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

A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.


## Procedure
1.*Create a New Project:
Open Quartus and create a new project by selecting "File" > "New Project Wizard." Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2.*Create a New Design File: Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3.*Write the Combinational Logic Code: Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4.*Compile the Project: To compile the project, click on "Processing" > "Start Compilation" in the menu. Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5.*Analyze and Fix Errors: If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window. Review and fix any issues in your code if necessary. View the RTL diagram.

6.*Verification: Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF". Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All. Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform


## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: V.Sai Sruthi
RegisterNumber: 23012602 
```
module boolean_exp(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire A1,A2,A3,B1,B2,B3;
assign A1=(~a)&(~b)&(~c)&(~d);
assign A2=(a&c&(~d));
assign A3=((~b)&c&(~d));
assign f1=A1|A2|A3;
assign B1=(x&(~y)&z);
assign B2=(~x&(~y)&z);
assign B3=(~w&x&y);
assign f2=B1|B2|B3;
endmodule
```


## truth table 

![image](https://github.com/sruthiviswanadham/Experiment--02-Implementation-of-combinational-logic-/assets/151760421/420fb46d-c8fd-4e83-a69c-436b795c0a54)

## RTL diagram

![image](https://github.com/sruthiviswanadham/Experiment--02-Implementation-of-combinational-logic-/assets/151760421/4d7b7d72-baa9-4e6a-b1c6-2c309197c4da)

## Timing Diagram

![image](https://github.com/sruthiviswanadham/Experiment--02-Implementation-of-combinational-logic-/assets/151760421/f4a8b435-33e3-4a51-ad54-9ec4965c0837)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
