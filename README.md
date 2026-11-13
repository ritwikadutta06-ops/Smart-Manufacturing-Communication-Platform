# Smart Manufacturing Communication Platform

## Project Overview
The Smart Manufacturing Communication Platform is a proof-of-concept project designed to demonstrate industrial machine monitoring and reliable data communication.

The project consists of two parts:

1. **Python Simulation:** Demonstrates packet formation, CRC-16 error detection, Hamming (7,4) error correction, BPSK modulation, AWGN channel simulation, and communication performance analysis.
2. **Arduino Hardware Prototype:** Uses three potentiometers to simulate temperature, pressure, and vibration sensors. An LCD displays sensor readings, while LEDs and a buzzer indicate machine conditions.

## Technologies Used
- Python
- Google Colab
- Arduino Uno
- Tinkercad
- CRC-16
- Hamming Code (7,4)
- BPSK Modulation
- AWGN Channel
- 16×2 LCD
- LEDs and Piezo Buzzer

## Hardware Monitoring
The prototype classifies machine conditions into:
- NORMAL
- WARNING
- CRITICAL

## Communication Simulation
The Python simulation evaluates communication performance using:
- Bit Error Rate (BER)
- Packet Delivery Ratio (PDR)
- Packet Error Rate (PER)
- Throughput
- Latency

## Repository Structure
- Python simulation notebook
- Arduino hardware code
- Performance graphs
- Hardware circuit screenshot

## Important Note
The potentiometers represent simulated industrial sensors. The Arduino monitoring prototype and Python communication simulation are separate demonstrations and are not directly connected.

This project is developed for academic purposes as a proof of concept.
