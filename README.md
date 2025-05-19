🧠 Quantum Variational Rewinding for Time Series Anomaly Detection
This repository contains the implementation and experiments from the research project:
"Time Series Anomaly Detection Using Hybrid Quantum Variational Rewinding"
by Priyavrata Tiwari.

🚀 Overview
Time Series Anomaly Detection (TAD) is essential in identifying unusual behaviors in complex systems. This project explores a novel quantum-inspired method called Quantum Variational Rewinding (QVR) and its hybrid extensions using classical neural networks to improve detection accuracy and robustness.

We compare:

1. Original QVR model.

2. Neural-enhanced QVR model.

3. Simplified variational quantum circuit.

🧠 Key Concepts
1. Quantum Variational Rewinding (QVR): Uses time devolution via variational circuits to detect anomalies.
2. Hybrid Neural-QVR: A feedforward neural network replaces stochastic parameter initialization to generate dynamic parameters.
3. Simplified Variational Circuit: A static, trainable unitary circuit with entangling gates improves noise tolerance and implementation efficiency.

🧪 Dataset
We used Cosmic Microwave Background (CMB) data from NASA containing:
1. Temperatures
2. Luminosities
3. Spectral Densities\
4. Optical Depth
5. Baryon Densities
6. Hubble Parameters
7. Dark Matter Density

Each time series has 7 features and is processed over 50 time points.

🛠️ Architecture Summary

📌 1. QVR Model
   a.  Angle encoding of time-series data
   b.  Time devolution using parameterized Hamiltonians
   c.  Loss function clusters expectation values near a fixed center

📌 2. Neural QVR Model
Neural network (layers: 50 → 128 → 64 → 32 → 7) replaces normal distributions

Output fed into modified QVR circuit

Loss function simplified due to deterministic parameter generation

📌 3. Static Variational Circuit
Removes time dependence for faster training

Introduces entangling layers

Mitigates barren plateau using partial measurements

📊 Performance Summary
Model	Max Validation Accuracy	Balanced Accuracy (Test)	Optimum ζ
QVR	0.69	0.70	0.0046
Neural-enhanced QVR	0.685	0.68	0.0045
Static Variational Circuit	0.66	0.68	0.00445
Threshold Method	—	0.61	—

📉 Training
QVR & Neural-QVR trained for 400 epochs

Variational circuit achieved convergence within 100 epochs

Barren plateau mitigated via partial measurement strategy

✅ Key Observations
All quantum models outperform the classical threshold method.

Neural network can replace probabilistic sampling in QVR with no significant accuracy loss.

Static variational circuits are lightweight and practical for NISQ devices.

Models are robust to noise, needing no pre-filtering.

📦 Dependencies
PennyLane

IBM Quantum Device Simulators

NumPy, PyTorch

🔮 Future Work
Train models on actual quantum sensor data

Explore weight initialization strategies for quantum circuits

Run models on noisy real quantum hardware with mitigation techniques

🙏 Acknowledgments
IBM Quantum services

NASA for CMB data
WMAP CMB Data
