# UART Transmitter and Receiver using Verilog

## Overview
This project implements a UART transmitter and receiver using Verilog HDL. It converts parallel data into serial data and reconstructs the received serial stream into an 8-bit parallel output.

## Features
- 8-bit data transmission and reception
- Configurable clock cycles per bit
- Start and stop bit handling
- Finite State Machine (FSM)-based design
- Self-checking testbench
- Automatic data comparison and error reporting

## UART Frame Format
`Start Bit (0) + 8 Data Bits (LSB First) + Stop Bit (1)`

## Test Cases
The testbench checks the following data patterns:
- `0x00`
- `0xFF`
- `0xA5`
- `0x3C`
- `0x81`

It compares transmitted and received data and reports PASS or FAIL for each test.

## Tools
- Verilog HDL
- Icarus Verilog or EDA Playground
- GTKWave (optional, for waveform analysis)

## How to Run
Compile and simulate using Icarus Verilog:

```bash
iverilog -g2012 -s tb_uart -o uart_sim uart_tx.v uart_rx.v tb_uart.v
vvp uart_sim
```

## Learning Outcomes
- Understanding UART serial communication
- Designing FSM-based digital circuits
- Implementing Verilog transmitter and receiver modules
- Developing self-checking testbenches
- Debugging RTL through simulation waveforms

## Future Enhancements
- Configurable baud-rate generator
- Parity-bit support
- Error detection and handling
- Randomized verification
- SystemVerilog assertions and functional coverage

## Author
Harshitha
