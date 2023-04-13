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
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: GURUMOORTHI R
RegisterNumber:  212222230042
*/
```
### HALF ADDER:
```
module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### FULL ADDER:
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```


### Output:

### RTL
### HALF ADDER:

![image](https://user-images.githubusercontent.com/118707009/231659421-0b100f7b-953f-4ee1-bd14-05602663b8a8.png)

### FULL ADDER:

![image](https://user-images.githubusercontent.com/118707009/231659481-bbc9bcb5-51fc-4d5a-9dd0-d097ac8608ef.png)

### TIMING DIAGRAM:
### HALF ADDER:

![image](https://user-images.githubusercontent.com/118707009/231659551-e52db5ba-81cd-4b1a-8bf0-495d2fc06085.png)

### FULL ADDER:

![image](https://user-images.githubusercontent.com/118707009/231659604-8adf9684-7d3e-4793-918b-77ee2f284fad.png)

### TRUTH TABLE:

### HALF ADDER:

![image](https://user-images.githubusercontent.com/118707009/231659682-56604aa0-244c-460c-a4d5-2e824792f30b.png)

### FULL ADDER:

![image](https://user-images.githubusercontent.com/118707009/231659756-f151f0ef-3c0a-46cc-9718-3acfe8c7cc59.png)




### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
