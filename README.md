# Verilog Modules Project
Name: Kesheng Wang
Netid: kw457
## Overview

This project contains several Verilog modules to design and simulate a register file which supports 2 read ports, 1 write port and 32 registers, including a register file, D flip-flop with enable, a decoder, and a tristate buffer.

## Modules

### 1. `regfile.v`

- **Purpose**: Implements a register file with 32 registers, supporting read and write operations.
- **Inputs**:
  - `clock`: Clock signal.
  - `ctrl_writeEnable`: Enables writing to the register.
  - `ctrl_reset`: Resets all registers.
  - `ctrl_writeReg`: Specifies which register to write to.
  - `ctrl_readRegA`, `ctrl_readRegB`: Specify which registers to read from.
  - `data_writeReg`: Data to be written to the register.
- **Outputs**:
  - `data_readRegA`, `data_readRegB`: Data read from the registers.

### 2. `dffe.v`

- **Purpose**: Implements a D flip-flop with enable and clear.
- **Inputs**:
  - `d`: Data input.
  - `clk`: Clock signal.
  - `en`: Enable signal.
  - `clr`: Clear signal.
- **Output**:
  - `q`: Output data.

### 3. `decoder_5to32.v`

- **Purpose**: 5-to-32 line decoder.
- **Inputs**:
  - `in`: 5-bit input.
- **Outputs**:
  - `out`: 32-bit output, where only one bit is high based on the input.

### 4. `tristate_32bit.v`

- **Purpose**: Implements a 32-bit tristate buffer.
- **Inputs**:
  - `in`: 32-bit data input.
  - `en`: Enable signal.
- **Output**:
  - `out`: 32-bit output, high impedance if not enabled.

### 5. `register.v`

- **Purpose**: Implements a 32-bit register using D flip-flops.
- **Inputs**:
  - `d`: 32-bit data input.
  - `clk`: Clock signal.
  - `en`: Enable signal.
  - `clr`: Clear signal.
- **Output**:
  - `q`: 32-bit data output.

