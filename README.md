# UART Transmitter & Receiver in SystemVerilog
Simulation of a UART protocol with integrated TX/RX logic, built in SystemVerilog and tested using Aldec Riviera Pro.
Project Description: This repository contains a SystemVerilog implementation of a UART transmitter and receiver in a single top module, tested using a self-contained testbench. The testbench feeds random data to the UART transmitter and verifies reception via a loopback connection.
Features: 
  Configurable baud rate and clock
  Full UART protocol (start bit, data bits, stop bit)
  Loopback test with random stimulus
  Start/stop/done signal handling
  Self-checking testbench
Simulation Setup:
  1. Go to https://edaplayground.com/
  2. Select:
     - Language: SystemVerilog
     - Simulator: Aldec Riviera Pro 2023.04
  3. Paste your `top` module in the "Design" section.
  4. Paste the testbench code in the "Testbench" section.
  5. Enable waveform viewer (EPWave).
  6. Click "Run".
  7. Observe the TX/RX activity and signal transitions.
