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
Developed by: SUBASH CHANDRA BOSE R
RegisterNumber: 22009106 
*/
```
half adder verilog code:
module half_adder(a, b, s, c);
input a, b;
output s, c;
xor(s, a, b);
and(c, a, b);
endmodule

full adder verilog code:

module full_adder(x, y, z, s, c, x1, x2, x3, x4);
input x, y, z;
output s, c, x1, x2, x3, x4;
xor(x1, x, y);
xor(s, x1, z);
and(x3, x, y);
and(x4, x1, z);
or(c, x3, x4);
endmodule
```

Logic symbol & Truthtable
RTL realization

### Output:
### RTL
half adder
![image](https://user-images.githubusercontent.com/123537051/215269742-c6d2fbbe-fee9-4cf7-93ad-8464fe390c07.png)
full adder 
![image](https://user-images.githubusercontent.com/123537051/215269782-c9c3d427-87c7-4c1f-a9c2-e9be5fc17b38.png)

### TIMING DIAGRAM
half adder
![image](https://user-images.githubusercontent.com/123537051/215269819-8defa03a-fafd-40a7-99ed-22103937ba70.png)
full adder
![image](https://user-images.githubusercontent.com/123537051/215269830-cfef432e-254f-43a4-a02a-f478fd78a5be.png)


### TRUTH TABLE 
![image](https://user-images.githubusercontent.com/123537051/215269870-9de0fa0f-b934-4c70-ab3e-97acedb13f9a.png)
![image](https://user-images.githubusercontent.com/123537051/215269881-b7426ceb-e2ae-4849-9c9a-3884ffd41c4b.png)

### Result:
