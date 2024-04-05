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
```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:Santha ramanath M
RegisterNumber:212223220097*/

module Ex02(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule

```
**RTL realization**

![Screenshot 2024-03-25 081948](https://github.com/Santharamanath/BOOLEAN_FUNCTION_MINIMIZATION/assets/149035289/b77b500f-0718-454a-baf4-d3b6f560b870)

**Truth table**

![316250520-e6c8b78e-c29b-46ee-aee9-29ee38d94cd0](https://github.com/Santharamanath/BOOLEAN_FUNCTION_MINIMIZATION/assets/149035289/deaba710-03a9-4d25-b7a0-56f2c8fc2ade)


**Timing Diagram**

![316250652-ac8ff171-7e0f-4034-9f73-63466a9d2ffe](https://github.com/Santharamanath/BOOLEAN_FUNCTION_MINIMIZATION/assets/149035289/e4dd2e20-ccce-4a06-b41e-3e533f261217)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

