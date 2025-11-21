# HALF_ADDER_SUBTRACTOR
DATE: 21/11/2025
Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Half Adder
------------------------------------------------
```
module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule
```

Half Sub
-------------------------------------
```
module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule
```




Developed by: Brindha A R


RegisterNumber:25013493

**RTL Schematic**

HALF ADDER:-

<img width="608" height="305" alt="Screenshot 2025-11-21 202252" src="https://github.com/user-attachments/assets/505f2e11-b288-4b15-bd07-f8555faeb6a1" />


HALF SUBTRACTOR:-

<img width="771" height="403" alt="Screenshot 2025-11-21 202511" src="https://github.com/user-attachments/assets/f450f065-2af1-4f5b-816b-74193b3049a7" />



**Output/TIMING Waveform**

HALF ADDER:-

<img width="795" height="162" alt="Screenshot 2025-11-21 202635" src="https://github.com/user-attachments/assets/c475b054-98ea-4d43-9489-bc6fd7718b82" />

HALF SUBTRACTOR:-

<img width="878" height="155" alt="Screenshot 2025-11-21 202748" src="https://github.com/user-attachments/assets/07ed64ba-0099-4557-96e2-1850e40e988d" />

**Result:**

Thus, the given logic functions are implemented using and their operations are verified using Verilog programming.
