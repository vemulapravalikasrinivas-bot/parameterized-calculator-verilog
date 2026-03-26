# parameterized-calculator-verilog
A parameterized calculator design in Verilog supporting basic arithmetic operations (add, subtract, multiply, divide) using synchronous RTL design.

# Verilog Calculator
This project implements a parameterized digital calculator using Verilog HDL.  
The design performs basic arithmetic operations based on a control signal.

## Features
- Parameterized bit-width (N-bit inputs)
- Signed arithmetic support
- Operations:
  - Addition
  - Subtraction
  - Multiplication
  - Division (with divide-by-zero protection)
- Synchronous design using clock and reset
- Synthesizable RTL code

## Inputs
- `a`, `b` : Signed operands
- `sel` : Operation select
- `clk` : Clock signal
- `reset` : Reset signal

## Output
- `out` : Result (2N-bit signed output)

## Operation Table

| sel | Operation |
|-----|----------|
| 00  | Addition |
| 01  | Subtraction |
| 10  | Multiplication |
| 11  | Division |

## Notes
- Division by zero returns 0 to ensure safe operation.
- The design can be extended with flags (overflow, zero, etc.).

## Future Improvements
- Add ALU module separation
- Include status flags
- Add testbench and waveform verification
- FSM-based calculator control
