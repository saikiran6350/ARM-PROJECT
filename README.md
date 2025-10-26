# AUTOMOTIVE ECU COMMUNICATION USING CAN PROTOCOL
A real-time vehicle lighting control system demonstrating Controller Area Network (CAN) communication between two LPC2129 ARM7 microcontrollers. This project implements interrupt-driven message passing for controlling headlights and turn indicators.


# Overview

This project demonstrates automotive Electronic Control Unit (ECU) communication using the CAN protocol. Two nodes communicate over a CAN bus:

Node A (Master/Transmitter): Sends control commands via button presses (external interrupts)
Node B (Slave/Receiver): Receives commands and controls LED outputs (headlight & indicators)


# Problem Statement

Traditional vehicle wiring systems are complex and prone to faults. This project demonstrates how CAN protocol:

Reduces wiring complexity
Provides reliable, real-time communication
Enables modular, scalable automotive networks
Implements fault-tolerant messaging


# Hardware Requirements
Component                                    Description                              Quantity
LPC2129 Microcontroller(Vector Board)       ARM7TDMI-S with built-in CAN controller    2

Push Buttons                                For triggering external interrupts (EINT0, EINT1, EINT2)3

LEDs                                        Representing headlight and indicators      3

Jumper Wires                                For CAN bus connection (CAN_H, CAN_L, GND)

Power Supply                                5V regulated supply for both boards         1


⚠️ Important Note: Built-in CAN Transceiver
Unlike typical CAN projects, this implementation uses the LPC2129 vector board's integrated CAN transceiver circuitry. Therefore:

No external MCP2551/TJA1050 transceiver needed
CAN_H and CAN_L are directly available on board pins
Simplified hardware setup
Refer to your vector board's schematic for exact CAN pin locations


# Software Requirements

Keil µVision IDE (v5 or later) - For compilation and debugging
Flash Magic - For programming LPC2129 via UART
Proteus Design Suite (optional) - For simulation
Git - For version control



# System Architecture



<img width="560" height="349" alt="image" src="https://github.com/user-attachments/assets/e02192b4-e0f2-480f-b422-4868e409a7ea" />



# CAN Bus Physical Layer   


<img width="556" height="118" alt="image" src="https://github.com/user-attachments/assets/61ecdba0-ec6d-4d55-8ff6-bf313e9ab9d3" />



# Pin Configuration


<img width="608" height="496" alt="image" src="https://github.com/user-attachments/assets/18c224b8-868b-409e-9ee2-8d9e1f3a3baa" />


# MIT LICENSE 📔

Copyright (c) 2025 K.Saikiran

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
