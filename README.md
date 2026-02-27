# QPSK Wireless Baseband Transceiver Simulation
## Wireless Communication Receiver Algorithm Project
---

## Requirements

- Python 3.x
- NumPy
- Matplotlib

Install dependencies:
pip install numpy matplotlib

---

## How to Run

Run the Jupyter Notebook or Python script:
python QPSK_project.py

---

## Author

Zhangxy Li  

##  Project Overview

This project implements a simplified wireless baseband communication system using Python.  
It demonstrates the fundamental structure of a digital communication chain:

Random Bit Generation → QPSK Modulation → AWGN Channel → Hard Decision Demodulation → BER Evaluation

The simulation focuses on understanding modulation mapping, noise impact, and bit error rate performance.

---

## Objectives

- Understand QPSK constellation mapping
- Simulate white Gaussian noise (AWGN) channel
- Implement hard decision demodulation
- Evaluate system performance using Bit Error Rate (BER)

---

## System Model

The communication chain implemented in this project: 
Bit Source → QPSK Modulator → AWGN Channel → Demodulator → BER Calculation

---

## Implementation Details

### 1 Bit Generation

Random binary bits are generated using NumPy:
bits = np.random.randint(0, 2, N)


---

### 2️ QPSK Modulation

Each pair of bits is mapped to a complex symbol:

| Bits |  Symbol |
|------|---------|
| 00   | 1 + 1j  |
| 01   | 1 - 1j  |
| 10   | -1 + 1j |
| 11   | -1 - 1j |

Symbols are normalized by √2.

---

### 3️ AWGN Channel

Complex Gaussian noise is added to simulate wireless channel conditions.

---

### 4️ Hard Decision Demodulation

The received symbols are decoded based on the sign of their real and imaginary parts.

---

### 5️ BER Calculation

Bit Error Rate (BER) is calculated by comparing transmitted and received bits.

---

## Example Result

For noise level = 0.3:
The constellation diagram shows four clustered clouds around ideal QPSK points.

---

## Key Observations

- Increasing noise level results in higher BER.
- Constellation points become more dispersed as noise increases.
- The simulation verifies the impact of noise on digital modulation.
