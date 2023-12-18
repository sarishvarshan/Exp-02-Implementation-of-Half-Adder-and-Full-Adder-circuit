## Name: Sarish Varshan.V
## Reg no: 23012018

## Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

## Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.


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
### Program:

HALFSUBTRACTOR:
module halfsubtractor(a,b,diff,borrow);
input a,b;
output diff,borrow;
assign diff=a^b;
assign borrow=~a&b;
endmodule
FULLSUBTRACTOR:
module fullsubtractor(a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
assign diff=a^b^c;
assign borrow=~a&b|c&~(a^b);
endmodule
## Logic symbol:
![Screenshot 2023-12-18 153515](https://github.com/sarishvarshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152167665/a967fdcb-2f7e-4412-8ac9-a0c17c013508)

![Screenshot 2023-12-18 153524](https://github.com/sarishvarshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152167665/b84a53d8-533f-4743-8f2d-2f5f463259c9)


## Truth table:
![286511396-8e10cf55-5b1a-4089-b750-49f6acdad175](https://github.com/sarishvarshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152167665/ac64873b-671b-4e1e-8ea7-79808e18d839)
uthtable:

![Screenshot 2023-12-18 153211](https://github.com/sarishvarshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152167665/4dd6d2d3-34b0-4015-8e4f-d08467b12411)

## RTL realization:

![Screenshot 2023-12-18 153227](https://github.com/sarishvarshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/152167665/4257dc66-5b52-46ef-a2b9-258cd9845141)

### Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
