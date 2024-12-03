# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

###### FULL ADDER

![Screenshot 2024-12-02 202212](https://github.com/user-attachments/assets/e7b19ed8-3a76-45a4-9ed0-ed001a5dc3bc)

###### FULL SUBTRACTOR

<img src='https://github.com/user-attachments/assets/c2a79505-22e5-4939-b5b4-7f45d1dd1ff1' width='500' >


**Procedure**

###### Full Adder:

1. Open Quartus II and create a new project.
2. Use schematic design entry to draw the full adder circuit. 
3. The circuit consists of XOR, AND, and OR gates. 
4. Compile the design, verify its functionality through simulation. 
5. Implement the design on the target device and program it.

###### Full Subtractor: 

1. Follow the same steps as for the full adder. 
2. Draw the full subtractor circuit using schematic design. 
3. The circuit includes XOR, AND, OR gates to perform subtraction. 
4. Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

Developed by: Kishorekavin s
RegisterNumber: 24005324

###### FULL ADDER

```
module full_adder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule

```

###### FULL SUBTRACTOR

```
module full_subtracter(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```



**RTL Schematic**

###### FULL ADDER

![Screenshot 2024-12-02 202340](https://github.com/user-attachments/assets/240ef848-554b-4489-971c-f9ce77959af5)

###### FULL SUBTRACTOR

![Screenshot 2024-12-02 202448](https://github.com/user-attachments/assets/eb30ca1c-e9a8-4972-abc2-73697f6944e4)


**Output Timing Waveform**

###### FULL ADDER

![Screenshot 2024-12-02 202352](https://github.com/user-attachments/assets/2cae555e-efd5-4415-aecf-f7f9933e0e13)

###### FULL SUBTRACTOR

![Screenshot 2024-12-02 202403](https://github.com/user-attachments/assets/55c09aad-424a-40de-b2f6-617bbf096053)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



