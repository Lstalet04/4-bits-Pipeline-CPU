
# 4-bit Pipeline CPU

Welcome to the repository for my 4-bit pipeline CPU project. This CPU is a simple yet functional design that implements a basic instruction set and pipeline architecture. The CPU can perform fundamental operations such as storing, loading, adding, and subtracting using 4-bit instructions. Below you will find detailed information about the CPU's components, functionality, and how to get started with this project.
## Table of content

- Overview

- Components

- Instruction Set

## Overview

This project is a functional 4-bit pipeline CPU composed of the following main components:

- Program Counter (PC) with automatic increment

- Arithmetic Logic Unit (ALU) using 2's complement

- 8 x 4-bit Instruction RAM

- 2 x 4-bit Data RAM

- Full Control Unit (CU)

- Register block with 2 registers (R0 and R1)

The CPU supports basic operations including storing and loading data from/to data RAM, adding, subtracting, and halting the system. The instruction set is designed to be simple and efficient, utilizing only 4-bit instructions.
## Components
### Program Counter (PC)
The program counter automatically increments to point to the next instruction in the instruction RAM. This ensures a sequential execution of instructions unless altered by control instructions (HALT which stops the incrementation of the counter).

### Arithmetic Logic Unit (ALU)
The ALU performs arithmetic operations (addition and substraction) using 2's complement for subtraction 

### Instruction RAM

The instruction RAM holds up to 8 instructions, each 4 bits wide.

### Data RAM
The Data RAM is able to hold up to two 4 bits numbers.

### Control Unit (CU)
The Control Unit manages the execution of instructions by decoding and generating the necessary control signals for each component based on the current instruction.

### Register Block
There are two temporary registers in the CPU, R0 and R1, which are used when loading, storing, and when performing operations.
## Instruction Set

The CPU supports a simple instruction set encoded in 4 bits as follows:

#### Storing (00)
Example: Storing R0 to RAM address 1 → 00 01
#### Loading (01)
Example: Loading data from RAM address 0 to R1 → 01 10
#### Adding (10)
Example: Adding contents of R0 and R1 → 10 01
#### Subtracting (11)
Example: Subtracting contents of R0 from R1 → 11 10
#### Halt (1111)
Complete stop of the system (note that halt replace the operation R1-R1)