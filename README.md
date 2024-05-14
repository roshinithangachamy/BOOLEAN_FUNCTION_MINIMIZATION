## EX-2 <p align="center"><b> BOOLEAN_FUNCTION_MINIMIZATION </b>    

**DATE:**

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

**Developed by: T.ROSHINI**

**RegisterNumber:212223230175**

```
module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
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

**Output:**

**RTL**

![boolean](https://github.com/naavaneetha/BOOLEAN_FUNCTION_MINIMIZATION/assets/147118341/0273c170-c7d3-4cc7-89bf-2d438baf778f)

**Timing Diagram**

![2 waveform](https://github.com/naavaneetha/BOOLEAN_FUNCTION_MINIMIZATION/assets/147118341/8ea1aa75-984f-486c-849e-e0e1bfb13351)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

