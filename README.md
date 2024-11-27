# ICS3203-CAT2-Assembly----150479-Onyonka-James-Magara


1. Control Flow and Conditional Logic
a. Overview:
The code contains a program to classify a number as "POSITIVE," "NEGATIVE," or "ZERO." It uses conditional (cmp and je, jl) and unconditional (jmp) jumps effectively.
b. Compiling and Running:
Save the code in a file named control_flow.asm.
Use the assembler (e.g., NASM) to create an object file: 'nasm -f elf32 control_flow.asm -o control_flow.o'
Link the object file to create an executable: 'ld -m elf_i386 control_flow.o -o control_flow'
Execute the program: './control_flow'
c. Insights/Challenges:
Managing conditional jumps (je, jl) required clear ordering to avoid logic errors.
Proper handling of inputs was critical. The implementation assumes basic integer input and required enhancements for error handling.
Using both conditional and unconditional jumps made the flow efficient but it demands careful alignment of labels and paths.

2. Array Manipulation with Looping and Reversal
a. Overview:
This program reverses an array of integers in-place using two pointers (ecx and edx) and swaps elements iteratively.
b. Compiling and Running:
Save the code in a file named array_reversal.asm.
Assemble: 'nasm -f elf32 array_reversal.asm -o array_reversal.o'
Link: 'ld -m elf_i386 array_reversal.o -o array_reversal'
Run: './array_reversal'
c. Insights/Challenges:
Implementing the reversal without additional memory required careful use of registers and pointer calculations.
The program uses index comparisons (cmp ecx, edx) to ensure swapping stops when indices meet or cross.
The array is initialized programmatically instead of accepting user input for simplicity.

3. Modular Program with Subroutines for Factorial Calculation
a. Overview:
This program calculates the factorial of a given number using a recursive subroutine and preserves context using the stack.
b. Compiling and Running:
Save the code in a file named factorial_subroutine.asm.
Assemble: 'nasm -f elf32 factorial_subroutine.asm -o factorial_subroutine.o'
Link: 'ld -m elf_i386 factorial_subroutine.o -o factorial_subroutine'
Run: './factorial_subroutine'
c. Insights/Challenges:
Managing recursive calls in assembly is challenging due to the need to explicitly save and restore registers using the stack.
Implementing the base case (cmp eax, 1; jle factorial_end) is crucial to avoid infinite recursion.
The result is stored in the eax register, simplifying its use in subsequent steps but also required careful stack management to avoid overwrites.

4. Data Monitoring and Control Using Port-Based Simulation
a. Overview:
Reads a sensor value stored in memory (sensor) and performs actions based on the sensor value:
High level (3): Activates the alarm (alarm = 1).
Moderate level (2): Turns off the motor (motor = 0).
Low level (1): Turns on the motor (motor = 1).
b. Compiling and Running:
Save the code in a file named port_simulation.asm.
Assemble: 'nasm -f elf32 port_simulation.asm -o port_simulation.o'
Link: 'ld -m elf_i386 port_simulation.o -o port_simulation'
Run: './port_simulation'
c. Insights/Challenges:
Memory initialization and correct port/memory mapping required careful handling.
Conditional logic must account for all sensor values to avoid undefined behavior.



