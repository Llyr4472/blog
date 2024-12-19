---
title: "RISC vs CISC : IIT Sem1 Assignment 1"
date: "2024-11-28"
description: Detailed comparison of RISC and CISC architectures
tags:
  - Assignment
  - IIT

categories:
  - CSIT
  - Semester 1
---
# RISC vs CISC: An IIT Assignment

### RISC (Reduced Instruction Set Computing)

#### Definition
RISC is a CPU design architecture that utilizes a small set of simplified instructions, each executable within a single clock cycle, focusing on optimizing the execution of basic operations through register-to-register operations and a load-store memory access model.

#### Key Features
- Fixed-length instruction format
- Single clock cycle execution per instruction
- Load-store architecture
- Large register set
- Hardware-based pipelining
- Register-to-register operations
- Limited addressing modes

#### Advantages
1. Simplified hardware design
2. Better instruction pipelining
3. Lower power consumption
4. Faster instruction execution
5. Easier to implement and debug

#### Disadvantages
1. Requires more RAM for program storage
2. More lines of code needed for complex operations
3. Higher complexity in compiler design
4. Limited instruction functionality
5. Requires more registers

### CISC (Complex Instruction Set Computing)

#### Definition
CISC is a CPU design architecture that implements a large set of complex instructions of varying lengths, capable of performing multi-step operations within a single instruction, with direct memory-to-memory operations support.

#### Key Features
- Variable-length instruction format
- Multi-clock cycle instructions
- Memory-to-memory operations
- Smaller register set
- Multiple addressing modes
- Hardware-handled complexity
- Microcode implementation

#### Advantages
1. Efficient memory usage
2. Backward compatibility support
3. Fewer lines of assembly code needed
4. Direct memory-to-memory operations
5. Complex operations in single instructions

#### Disadvantages
1. Complex decoder circuitry required
2. Higher power consumption
3. Longer instruction execution time
4. More complex hardware design
5. Difficult to implement efficient pipelining

##       Detailed Comparison Table

<iframe 
    src="/downloads/CSIT/Sem1/IIT/risc-vs-cisc.pdf"
    width="100%"
    height="600px">
    >
    </iframe>

[Download PDF](/downloads/CSIT/Sem1/IIT/risc-vs-cisc.pdf)
[Cover Page](/downloads/CSIT/Sem1/IIT/coverpage.pdf)
