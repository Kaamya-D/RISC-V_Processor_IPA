# RISC-V Processor

This repository contains the implementation of a **RISC-V Processor**, designed to execute a subset of the RISC-V instruction set architecture (ISA). The project includes Verilog HDL implementation, testbenches, and simulations for verification.

## Features
- Implements a **5-stage pipeline** (IF, ID, EX, MEM, WB)
- Supports **RV32I base integer instruction set**
- **Hazard detection** and forwarding mechanisms
- **Branch prediction** for performance optimization
- Simulation and verification using **Verilog testbenches**

## Project Structure
```
├── src/                 # Source code for the processor
│   ├── alu.v            # Arithmetic Logic Unit
│   ├── control_unit.v   # Control Unit
│   ├── datapath.v       # Datapath
│   ├── register_file.v  # Register File
│   ├── memory.v         # Memory Module
│   └── processor.v      # Top-level Processor Module
├── test/                # Testbench files
│   ├── processor_tb.v   # Processor testbench
│   ├── alu_tb.v         # ALU testbench
│   └── memory_tb.v      # Memory testbench
├── README.md            # Project documentation
└── LICENSE              # License information
```

## Getting Started
### Prerequisites
- **Verilog Simulator** (e.g., ModelSim, Icarus Verilog, Vivado)
- **Git** for version control
- **RISCV-GCC Toolchain** (for compiling RISC-V assembly programs)

### Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/MadhanSaiKrishna/RISC-V-Processor.git
   cd RISC-V-Processor
   ```
2. Set up the RISC-V toolchain (if needed) to compile and test programs.

### Running the Simulation
1. Open a terminal and navigate to the testbench directory:
   ```sh
   cd test
   ```
2. Run the testbench using your Verilog simulator:
   ```sh
   iverilog -o processor_tb.out processor_tb.v ../src/*.v
   vvp processor_tb.out
   ```
3. View waveforms using GTKWave (if enabled in the testbench):
   ```sh
   gtkwave processor_tb.vcd
   ```

## Supported Instructions
The processor currently supports the following RISC-V **RV32I** instructions:
- **Arithmetic**: ADD, SUB, AND, OR, XOR, SLL, SRL, SRA
- **Load/Store**: LW, SW
- **Branch**: BEQ, BNE, BLT, BGE
- **Immediate Operations**: ADDI, ANDI, ORI

## Contributing
Contributions are welcome! If you find issues or have improvements, please:
1. Fork the repository
2. Create a new branch (`feature-xyz`)
3. Commit your changes
4. Open a Pull Request

## License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## Contact
For any queries or discussions, feel free to open an issue or reach out via GitHub!

---

Happy Coding! 🚀

