# Assembly project
Contribution of each member:

Ikrame worked on the R and S instructions , J and U , and S compressed instructions.
Maram worked on the I instructions, Ecall, I and R compressed instruction.
Mohamed worked on the B, J instructions and the string ABI names function.
Ikrame and Maram took care of debugging and creating the test files in several meetings.  

Implementation details: 

We used the skeleton provided by the Dr. And expended it to all other instructors of 32 and 16 bits (compressed) instructions. We decided to keep everything in one function called instDecExec that takes the instruction word from the binary file. The 32 and compressed instructions are separated by an if statement. The function first checks the first 2 bits of the opcode and accordingly it decides if the instruction is 32 instructions or compressed. For each type, it checks the different fields from the instruction word and stores them in different variables. Then, it uses if else statements and switch cases to decide on which instruction it is.
The instDecExec function returns a boolean value that tells if the instruction is compressed, and in the main we use its return value to make the memory increase by 2 bytes instead of 4 if the instruction is compressed.
We used another function called ABI_name to display the ABI names of the registers as required in the handout. 

Limitations: 

We were not able to print the label names. 

Known issues: 

There are no known issues with the logic of the code, but one of the binary files we made to test the compressed instructions is displaying the right instructions but after each one there is a line with "Unknown compressed instruction" that we couldn't figure out its cause. 

 
