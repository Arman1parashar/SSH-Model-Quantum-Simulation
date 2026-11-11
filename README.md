# 1D SSH Model - Quantum Simulation

A Qiskit-based quantum simulation of the 1D Su-Schrieffer-Heeger (SSH) topological insulator model built on a 4-qubit circuit.

I created this project to observe topological phase transitions by dynamically building parameterized circuits and running them on IBM's `AerSimulator`.

## Quantum Circuit
The circuit initializes boundary qubits with Hadamard gates and maps tight-binding electron interactions using $R_{XX}$ and $R_{YY}$ rotation gates via Suzuki-Trotter decomposition:

[Quantum Circuit](circuit_diagram.png)

## Results & Phase Transition
By varying the hopping parameter ratio ($v/w$ from 0.1 to 2.0), the boundary correlation $\langle Z_0 Z_3 \rangle$ shows a clear breakdown at the topological phase boundary ($v/w = 1.0$):

[Phase Transition Graph](phase_transition.png)

- **$v/w < 1.0$**: Stable topological edge states (high boundary amplitude).
- **$v/w = 1.0$**: Phase transition threshold.
- **$v/w > 1.0$**: Trivial phase breakdown.

## Tech used
- **Quantum Framework: Qiskit, Qiskit Aer
- **Language: Python 3
- **Analysis & Visualization: NumPy, Matplotlib
