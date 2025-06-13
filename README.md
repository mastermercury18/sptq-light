# 🔬 Single-Photon 2-Qubit Quantum Experiments (Qiskit + Perceval)

This project explores the simulation and verification of entanglement and quantum search algorithms within a **single-photon, two-qubit system**, leveraging both **Qiskit** and **Perceval**. By encoding two qubits into a photon's spatial and polarization modes, the system models key quantum operations in a highly scalable, resource-efficient format—bypassing the need for multi-photon entanglement and enabling clearer experimental fidelity.

---

## 🧠 Motivation

The scalability of quantum systems is often bottlenecked by the complexity of entangling and tracking multiple photons or particles. This project introduces a linear optics-based approach to encode **multiple qubits within a single photon** using **spatial modes** and **polarization**, reducing manufacturing complexity and loss, while maintaining quantum mechanical behavior such as **entanglement**, **interference**, and **nonlocality**.

---

## 📌 What's Included

- **Bell_State_Entanglement (Qiskit + Perceval):**  
  Simulates the creation of the third Bell state (|Ψ+⟩) within a single photon's degrees of freedom.  
  - In Qiskit, waveplate-equivalent quantum gates model polarization rotations and interactions.
  - In Perceval, optical elements like beam splitters, HWPs, and PBSs are used to demonstrate the Hong-Ou-Mandel (HOM) effect and verify entanglement via simulated photon detection histograms.

- **Grover's Algorithm (Qiskit + Perceval):**  
  Demonstrates Grover’s quantum search on a 2-qubit register encoded in spatial mode basis.  
  - The oracle marks a single state.
  - The diffusion operator is constructed using photonic components.
  - In both backends, the algorithm achieves 100% success rate in the noiseless case and robust performance with added phase noise (Qiskit).

---

## 🔧 Key Concepts Modeled

### ✨ Bell State Entanglement
- Uses HOM interference to produce indistinguishable spatial mode bunched states.
- Validates entanglement by simulating violation of the **CHSH inequality** in Qiskit.
- Confirmed entanglement if results exceed **Tsirelson’s bounds** (|S| > 2).

### 🔍 Grover's Algorithm
- Modeled over the 2-qubit basis formed by spatial modes A and B.
- Constructs both the **oracle** and **diffusion** operator using either quantum gates (Qiskit) or beam splitter matrices (Perceval).
- Accuracy tracked as a function of **noise strength** to simulate real-world instability.

---

## 🧪 Technical Highlights

- **Single-Photon Source Simulation:**  
  The Qiskit model treats each qubit as a superposition of polarization basis vectors. The Perceval model simulates realistic photon paths via Fock states.

- **Gate ↔ Optics Mapping:**  
  - Hadamard → Quarter-Wave Plate  
  - Pauli-X → Half-Wave Plate  
  - CNOT → HOM interference modeled via beam splitters  
  - RY(θ) → Polarization rotation

- **Verification Metrics:**  
  - Uniform photon detections across ports (HOM success)  
  - CHSH inequality violations (|S| > 2)  
  - Accuracy drop-off curves for Grover's algorithm under noise

---

## 🔭 Broader Applications

- Secure quantum communication protocols (e.g. E91, BB84)
- Quantum teleportation setups with fewer resources
- Future development of **qudit systems** via hybrid encoding (polarization, momentum, spin)
- Photonic quantum processors using **linear optics alone**

---

This repo represents a research-grade photonic simulation framework demonstrating that powerful quantum behaviors such as entanglement and Grover’s search can emerge within a minimal, highly interpretable model: a single photon, and just two degrees of freedom.
