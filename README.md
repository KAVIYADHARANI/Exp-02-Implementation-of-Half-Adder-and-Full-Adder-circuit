# NAME: KAVIYA D
# REGISTER NUMBER: 212223040089
# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
# Theory
Adders are digital circuits that carry out addition of numbers.

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
![image](https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/0e80d074-d929-4cc9-a758-6ccf6e1b2d77)

# PROGRAM
```
module half_add(a,b,sum,carry);	                                   
input a,b;
output sum,carry; 
xor(sum,a,b);
and(carry,a,b);
endmodule
```
# RTL REALIZATION

![image](https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/50ad7bbe-b402-47bf-885d-31b441cae313)

# TRUTH TABLE

![image](https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/374a4978-335f-47a8-9bb4-d072f2a2ffe6)

# TIMING DIAGRAM

![image](https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/4d145ab0-8158-4e18-b4a1-c2c735fdf17d)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
![image](https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/05f2e941-8443-4bb0-b790-16041441b4e1)


### Program:
```
module full_add(a,b,c,sum,carry);
input a,b,c;
output sum,carry; 
xor(sum,a,b,c);
assign carry=a&b|b&c|a&c; 
endmodule
```
# RTL realization
![image](https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/fe8528ff-7196-47d9-a185-09884d82e0a4)

# TRUTH TABLE
![image](https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/0525f752-d305-4304-b6b0-af80be6bcc80)

### TIMING DIAGRAM
<img width="960" alt="fulladder(w)" src="https://github.com/KAVIYADHARANI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870680/0f77fbbd-e84b-4fcd-8a37-f1d0cc9c10cd">

### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming.

