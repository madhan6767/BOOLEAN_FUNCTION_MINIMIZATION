# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:Madhan M RegisterNumber:* 212225040213
```
module exp2de(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash;
wire f11,f12,f13,f21,f22,f23;
not (adash,a);
not (bdash,b);
not (cdash,c);
not (ddash,d);
not (ydash,y);

and (f11,bdash,ddash);
and (f12,adash,b,d);
and (f13,a,b,cdash);
or (f1,f11,f12,f13);

and (f21,ydash,z);
and (f22,x,y);
and (f23,w,y);
or (f2,f21,f22,f23);
endmodule
```

**RTL realization**

<img width="787" height="712" alt="image" src="https://github.com/user-attachments/assets/1f216247-f4c6-463d-aa4f-5cfde1110dc6" />


**RTL**

<img width="1917" height="336" alt="image" src="https://github.com/user-attachments/assets/9fe8dfff-da5c-4b01-adad-591f9338316e" />

<img width="1915" height="350" alt="image" src="https://github.com/user-attachments/assets/0ee16e98-3de4-4aa5-bbf3-c607071582d9" />

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

