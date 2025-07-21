# 🔌 Verilog UART Transmitter and Receiver Simulation

This project implements a basic UART-style serial communication system in Verilog, featuring both transmit (TX) and receive (RX) logic with baud rate generation and loopback verification using a self-checking testbench.

---

## 📄 Project Description

- A UART TX module sends an 8-bit data frame with start and stop bits.
- A UART RX module receives serialized bits using mid-bit sampling logic.
- A single wire (`txrx`) is used for loopback, simulating both transmit and receive paths.
- A testbench stimulates the system by sending random data, waits for transmission and reception to complete, and dumps the waveform for verification.

---

## ⚙️ Configuration Parameters

| Parameter      | Description                        | Default Value |
|----------------|------------------------------------|---------------|
| clk_value      | System clock frequency in Hz       | 100_000       |
| baud           | UART baud rate                     | 9600          |
| wait_count     | Number of clock cycles per bit     | Auto-calculated (clk_value / baud) |

---

## ✅ Features

- UART bit framing (1 start bit, 8 data bits, 1 stop bit)
- Bit-level transmit and receive logic
- Parameterized baud rate generator
- Mid-bit sampling on RX to improve noise immunity
- Handshake output signals: `txdone` and `rxdone`
- Self-checking loopback testbench using random data

---

## ▶️ How to Simulate

Use any Verilog-compatible simulator such as Icarus Verilog.

iverilog -o design.v tb.v
vvp uart_sim


