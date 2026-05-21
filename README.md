# HALF_ADDER_SUBTRACTOR

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

half adder
module exp3 (
    input  wire a, b,     
    output wire sum,     
    output wire carry    
);

    
    assign sum   = a ^ b;   
    assign carry = a & b;   
    endmodule

    half subracter

    module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule



**RTL Schematic**
half adder
<img width="389" height="269" alt="Screenshot 2026-05-21 113751" src="https://github.com/user-attachments/assets/bbdfff22-edc8-4fe9-b8e7-bbc73fcf0269" />
half subractor

<img width="564" height="329" alt="Screenshot 2026-05-21 113755" src="https://github.com/user-attachments/assets/8410834d-3aaf-4a55-a4d9-1f11743cfdd6" />



**Output/TIMING Waveform**
half adder
<img width="1419" height="650" alt="Screenshot 2026-05-21 113815" src="https://github.com/user-attachments/assets/a807cbc3-1f52-4e8b-99ad-5a225093c51a" />
half subractor
<img width="1285" height="629" alt="Screenshot 2026-05-21 113832" src="https://github.com/user-attachments/assets/94700387-7cd5-4e52-949b-f4ec7b2ec1fb" />



**Result:**
This Program was excecuted successfully
