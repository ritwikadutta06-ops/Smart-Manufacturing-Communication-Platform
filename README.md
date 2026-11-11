# Smart Manufacturing Communication Platform

A Python-based simulation of a reliable digital communication system designed for smart manufacturing environments.

## 1. Project Overview

In smart manufacturing industries, machines and sensors continuously generate operational data such as temperature, pressure, and vibration. Reliable transmission of this data is essential for real-time monitoring and identifying abnormal machine conditions.

This project simulates an industrial communication system that transmits sensor data through a noisy communication channel while using error detection and correction techniques to improve communication reliability.

The system uses **CRC-16 error detection, Hamming (7,4) error correction, BPSK modulation, and an AWGN channel** to demonstrate reliable digital data transmission.

## 2. Project Objectives

- Simulate industrial sensor data acquisition.
- Convert sensor readings into digital data packets.
- Implement CRC-16 for error detection.
- Apply Hamming (7,4) coding for error correction.
- Transmit encoded data using BPSK modulation.
- Simulate channel noise using an AWGN model.
- Evaluate communication performance using BER and packet delivery ratio.
- Develop a receiver-based machine monitoring and alert system.

## 3. System Architecture

The proposed communication workflow is:

```text
Industrial Sensor Data
        |
        v
Data Acquisition
        |
        v
Data Packet Formation
        |
        v
CRC-16 Error Detection
        |
        v
Hamming (7,4) Encoding
        |
        v
BPSK Modulation
        |
        v
AWGN Communication Channel
        |
        v
BPSK Demodulation
        |
        v
Hamming Decoding
        |
        v
CRC Verification
        |
        v
Data Reconstruction
        |
        v
Industrial Monitoring
        |
        v
Machine Status and Alerts
```

## 4. Technologies and Techniques Used

| Technology / Technique | Purpose |
|---|---|
| Python | Main programming language |
| Google Colab | Development and simulation environment |
| NumPy | Numerical computation and signal processing |
| Pandas | Sensor data and packet handling |
| Matplotlib | Graphs and performance visualization |
| CRC-16 | Error detection |
| Hamming (7,4) | Error correction |
| BPSK | Digital modulation |
| AWGN | Communication channel noise simulation |

## 5. Project Implementation

### Module 1: Industrial Sensor Data Generation

Simulated industrial sensor readings are generated for:
- Temperature
- Pressure
- Vibration

The readings are organized into digital packets containing machine identification, sequence number, and sensor values.

### Module 2: Error Detection Using CRC-16

CRC-16 is implemented to detect errors in transmitted data packets. The receiver verifies the CRC after transmission to identify corrupted packets.

### Module 3: Digital Communication Simulation

The communication process includes:
- Hamming (7,4) encoding
- BPSK modulation
- AWGN channel simulation
- BPSK demodulation
- Hamming decoding
- CRC verification

### Module 4: Communication Performance Evaluation

The system evaluates communication performance through repeated transmission trials and calculates:
- Bit Error Rate (BER)
- Packet Error Rate (PER)
- Packet Delivery Ratio (PDR)
- Processing time
- Software processing throughput

### Module 5: Industrial Machine Monitoring

A monitoring system classifies machine conditions into:
- NORMAL
- WARNING
- CRITICAL

Illustrative sensor thresholds are used to demonstrate how abnormal machine conditions can be identified.

### Module 6: Receiver-Based Monitoring

The receiver reconstructs sensor readings from CRC-verified packets and displays the received data with corresponding machine status classifications.

### Module 7: Multi-SNR Performance Analysis

The communication system is tested at different signal-to-noise conditions (Eb/N0) to observe how channel quality affects BER and packet delivery.

## 6. Simulation Results

The following results were obtained in the simulated communication environment.

### Multi-SNR Performance

| Eb/N0 (dB) | BER | Valid Packets | Packet Delivery Ratio |
|---:|---:|---:|---:|
| 0 | 0.122875 | 0 | 0% |
| 2 | 0.055023 | 63 | 6.3% |
| 4 | 0.015307 | 445 | 44.5% |
| 6 | 0.002455 | 894 | 89.4% |
| 8 | 0.000068 | 995 | 99.5% |
| 10 | 0 | 1000 | 100% |

The simulation demonstrates that increasing Eb/N0 improves communication reliability by reducing bit errors and increasing successful packet delivery.

### End-to-End Transmission

At 10 dB Eb/N0, one simulation run produced:
- Original data bits: 88,000
- Encoded bits: 154,000
- Bit errors after decoding: 0
- CRC-verified packets: 1,000
- Corrupted packets: 0
- Packet delivery ratio: 100%

These are results from a finite simulation run, not a guarantee of error-free real-world communication.

## 7. Graphical Analysis

The repository includes graphs generated during the simulation:

1. BPSK Modulated Signal
2. BER Performance Comparison of Digital Modulation
3. BER Performance Comparison
4. Industrial Machine Sensor Monitoring
5. Receiver-Based Industrial Machine Monitoring
6. End-to-End BER Performance
7. Packet Delivery Performance

These visualizations help demonstrate the communication process, machine monitoring, and system performance.

## 8. How to Run the Project

The project is implemented in a Jupyter Notebook and can be executed using Google Colab.

1. Clone or download this repository.
2. Open Google Colab: https://colab.research.google.com/
3. Upload `Smart_Manufacturing_Communication_Platform.ipynb`.
4. Run the notebook cells sequentially.
5. Observe the generated outputs, performance metrics, and graphs.

### Requirements

- Python 3
- NumPy
- Pandas
- Matplotlib

## 9. Applications

The proposed simulation demonstrates concepts relevant to:
- Smart manufacturing systems
- Industrial sensor communication
- Machine condition monitoring
- Industrial IoT communication
- Reliable digital data transmission

## 10. Limitations and Future Scope

**Current limitations:**
- The project is a software-based simulation and does not use physical industrial sensors or communication hardware.
- Sensor readings and channel noise are simulated.
- The AWGN channel is a simplified model of communication noise.
- Monitoring thresholds are illustrative and are not certified industrial safety limits.

**Future enhancements:**
- Integration with ESP32 or other microcontrollers.
- Real-time sensor data acquisition.
- Implementation of wireless communication modules.
- Development of a live industrial monitoring dashboard.
- Testing with physical communication hardware and real-world channel conditions.

## 11. Conclusion

The Smart Manufacturing Communication Platform demonstrates how digital communication and error-control techniques can be combined to improve the reliability of industrial sensor data transmission.

By integrating CRC-16, Hamming coding, BPSK modulation, AWGN channel simulation, and receiver-based monitoring, the project provides a software-based demonstration of reliable communication in a smart manufacturing environment.

---

**Project Type:** Academic Project / B.Tech ECE  
**Domain:** Digital Communication, Signal Processing, Industrial IoT  
**Language:** Python  
**Platform:** Google Colab
