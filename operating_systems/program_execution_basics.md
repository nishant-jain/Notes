### Basics of program execution
- Instruction execution cycle
	- It is the process by which a computer retrieves a program instruction from its memory, determines what actions the instruction dictates, and carries out those actions.
	- Fetch -> decode -> read -> execute --> repeat
	- Fetch(Read fetch step on wiki for details)
	- Next instruction whose address is stored in PC is fetched and stored in IR. PC then points to the next instruction.
	- MAR/MBR used here for fetching instructions.
	- Decode
	- Instruction present in IR is interpreted by the decoder.
	- Done by the CU
	- Read
	- Any required data is fetched from memory and placed in registers
	- Executes I/O and register instructions
	- Direct memory operation - Nothing is done.
	- Indirect memory operation - The effective address is read from memory.
	- Execute
	- CU passes signals to units of CPU according to the decoded instruction in IR. Ex- reading value from register, performing mathematical operations using ALU, then writing the result back into a register.
	- May change the value of PC on the basis of output generated
- Programs
	- sequence of opcodes and operands stored in memory
	- Converted to binary representation before CPU can understand
- Program load process
	-  HDD -> RAM -> Cache -> Registers -> CPU

#### Components:
- Program counter (PC)
	- Incrementing counter which holds the memory location of the next instruction to be executed
	- Contains the address to ROM at the time of boot(which boots up the system)
- Instruction register(IR)
	- Temporarily holds the instruction fetched from memory.
- MAR(Memory address register)
	- Holds the address of a block of memory for reading from or writing to.
- MBR/MDR(Memory buffer register/memory data register)
	- A two-way register that holds data fetched from memory (and ready for the CPU to process) or data waiting to be stored in memory.
- CU(Control unit)    
	- Decodes the program instruction in the IR, selecting machine resources, such as a data source register and a particular arithmetic operation, and coordinates activation of those resources.
- ALU(arithmetic logic unit)
- FLU(floating point unit)

#### Machine code instructions
- Consists of operation code(opcode) and operand (LOAD A, 100001)
	- Can contain opcode only too, sometimes
	- Opcode - An opcode is a single instruction that can be executed by the CPU
	- Operand - Operands are manipulated by the opcode
- MOV AL, 34h
	- Opcode - MOV
	- Operand - AL(register), 34h- 
- Both are binary codes
- Structure of program in RAM - {[opcode, operand], [opcode, operand], [opcode].....}- 

##### References:
- [How does CPU execute program](https://www.youtube.com/watch?v=42KTvGYQYnA)
- [Machine Code Instructions](https://www.youtube.com/watch?v=Mv2XQgpbTNE)
- [Wiki](https://en.wikipedia.org/wiki/Instruction_cycle)
