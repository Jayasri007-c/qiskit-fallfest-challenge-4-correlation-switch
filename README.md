# Challenge 4: Quantum Correlation Switch

**Event:** Qiskit Fall Fest 2026 (IBM Quantum)
**Venue:** Vishnu Institute of Technology, Bhimavaram
**Participant:** [Your Name] · [Roll Number]

## Problem
Design a two-qubit circuit that switches between correlated outcomes (`00`, `11`) and opposite outcomes (`01`, `10`).

## Design
A function `correlation_switch(opposite=True/False)` builds both circuits. The shared core is the Bell state (H, CNOT). The switch is an optional X gate on qubit 1.

| Part | Gates | Dominant outcomes |
|---|---|---|
| A: correlated | H, CNOT | `00`, `11` |
| B: opposite | H, CNOT, X | `01`, `10` |

## Explanation
Entanglement from H + CNOT fixes the *relationship* between the qubits, while each individual result stays random. The X gate flips qubit 1 in every branch of the superposition, which switches the relationship from equal to opposite. Only two of the four outcomes appear in each circuit.

## Files
- `Challenge_4_Quantum_Correlation_Switch.ipynb`: the notebook with both circuits, predictions, results, histograms and comparison

## How to run
```bash
pip install qiskit qiskit-aer matplotlib pylatexenc jupyter
jupyter notebook Challenge_4_Quantum_Correlation_Switch.ipynb
```

## Tools
Python, Qiskit, Qiskit Aer simulator, Matplotlib
