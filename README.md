# Custom 8-Bit Instruction / 16-Bit Datapath Processor

A simple custom processor architecture designed in **SystemVerilog** and simulated using **Vivado 2019.1**.

This project demonstrates how the main building blocks of a processor work together, including the Program Counter, Instruction Memory, Register File, ALU, instruction decoding, and write-back path.

## Processor Architecture

The processor uses:

- 8-bit instruction width
- 16-bit datapath
- Four 16-bit registers
- Four ALU operations
- Four instruction memory locations

The instruction carries control and register address information, while the actual 16-bit data is stored inside the Register File.

## Instruction Format

Each 8-bit instruction is divided into four 2-bit fields:

| Bits | Field | Description |
|------|-------|-------------|
| `[7:6]` | `rd` | Destination register |
| `[5:4]` | `rs2` | Second source register |
| `[3:2]` | `rs1` | First source register |
| `[1:0]` | `opcode` | ALU operation |

Example:

```text
01_10_11_00
