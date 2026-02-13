# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JNC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4301H;
HLT; largest
```

## Output:
<img width="801" height="424" alt="LIC GN (2)" src="https://github.com/user-attachments/assets/cdaa5d72-1d73-45d8-9214-f30f7637035b" />

<img width="760" height="428" alt="LIC GN" src="https://github.com/user-attachments/assets/e6fe8b36-0dd7-4a33-9e78-1e4fa7b8c98f" />

## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4301H;
HLT; smallest
```
## Output:
<img width="698" height="584" alt="LIC SM" src="https://github.com/user-attachments/assets/5f85470c-9b65-4a88-bffc-466f315b5875" />

<img width="629" height="387" alt="LIC SM (2)" src="https://github.com/user-attachments/assets/8d85d627-8844-436e-b88f-3f5e8cedf2b6" />

## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
