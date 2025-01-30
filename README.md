# MIPS-Simulator
## Overview
This Python-based **MIPS Simulator** is designed to parse, translate, and execute MIPS assembly language programs. It provides a complete pipeline for processing `.data` and `.text` sections, translating instructions into binary, simulating the MIPS datapath, and executing instructions in a step-by-step manner.

## Key Features
### Instruction Parsing
- Supports **R-type, I-type, and J-type** MIPS instructions.
- Handles additional pseudo-instructions like `li`, `la`, and `move`.
- Includes opcode and function code maps for accurate instruction translation.

### Memory and Register Simulation
- Simulates memory and register states, including address mapping for variables and labels.
- Implements memory allocation for `.word` and `.asciiz` declarations in the `.data` section.
- Supports registers `$zero` to `$ra` with binary encoding.

### Instruction Translation
- Converts MIPS assembly instructions into **32-bit binary format**.
- Writes translated instructions to an **output file** for further processing.

### Instruction Execution
- Decodes and executes **binary MIPS instructions**.
- Simulates program execution using the **program counter (PC)**.
- Implements **arithmetic, logical, branching, and memory access operations**.

### Debugging and Visualization
- Prints each executed instruction and its corresponding **register states**.
- Provides the option to **view memory contents** during or after execution.

## Components
### Instruction Decoder
- Parses and decodes binary instructions to human-readable assembly.

### MIPSProcessor Class
- Handles the execution of instructions, maintaining memory and register states.

### Data Section Parser
- Maps variables and strings to memory addresses and stores their values.

### Execution Engine
- Executes **R-type instructions** like `add`, `sub`, `and`, `or`, and `slt`.
- Handles **I-type instructions** for load/store (`lw`, `sw`), arithmetic immediate (`addi`), and branching (`beq`, `bne`).
- Executes **J-type instructions** for jumps (`j`, `jal`).

## Workflow
### Input Handling
- Reads a MIPS assembly file (`input.txt`).
- Parses `.data` and `.text` sections to map labels and translate instructions.

### Translation
- Converts MIPS assembly into binary instructions and writes them to an output file (`output.txt`).

### Execution
- Loads binary instructions into memory.
- Executes each instruction while maintaining and displaying the program state.

### Output
- Displays **execution trace, register states, and memory contents**.

## Applications
This simulator is a valuable tool for:
- **Educational Purposes**: Understanding the MIPS architecture and instruction set.
- **Debugging**: Testing MIPS assembly programs for functional correctness.
- **Architecture Simulation**: Simulating basic operations and dataflow in a MIPS processor.

## Example Use
To use this simulator:
1. Provide a **MIPS assembly file** (`input.txt`) containing `.data` and `.text` sections.
2. Run the script to **translate and execute** the program.
3. Review the execution trace and debug using **printed memory and register states**.

This comprehensive simulator bridges the gap between **theoretical MIPS concepts** and **practical implementation**, making it an essential tool for students and developers working with assembly languages.

## License
This project is open-source and free to use for educational and research purposes.

