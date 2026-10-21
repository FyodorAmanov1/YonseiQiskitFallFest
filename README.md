# Yonsei Qiskit Fall Fest 2025

**A notebook collection progressing from quantum-circuit fundamentals to hybrid circuit/observable experiments.**

The repository contains the beginner and challenger materials for Yonsei's 2025 Qiskit Fall Fest. They combine explanations, circuit-building tasks, supplied grader calls and worked code for exploring quantum computation with Qiskit.

## Choose a notebook

| Notebook | Topics |
|---|---|
| [Beginner](qff25_yonsei_beginner.ipynb) | Pauli and rotation gates, entanglement, dynamic circuits, visualization, parameterized circuits, transpilation, primitives and BB84 |
| [Challenger](qff25_yonsei_challenger.ipynb) | Interferometer/bomb-detector experiments and operator backpropagation with Qiskit add-ons |

Start with the beginner notebook for circuit conventions and measurement. Move to the challenger notebook to inspect the trade-off between quantum circuit depth, classical observable complexity and approximation error.

## Environment

Use a fresh Python environment with Jupyter. The notebooks contain their own setup cells for Qiskit, Aer, IBM Runtime and the relevant add-ons.

```bash
python -m pip install jupyterlab
python -m jupyter lab
```

Open a notebook and read its installation and grader-import cells before running later sections. The event grader is an external dependency, not a Python package bundled in this repository. Event-specific grading services may require their original environment.

Most circuit examples can be studied locally. Hardware-specific sections additionally require your own provider access; the existence of a submission cell does not establish a completed physical-device run.

## How to use the material

- Inspect the circuit before its histogram or score.
- Complete TODO cells and compare their output with the stated target behavior.
- Separate sampling variation from a change in the underlying circuit.
- For operator backpropagation, inspect both the reduced circuit and the transformed observable.

These are educational and event materials, not an independent benchmark or a production quantum application. Retain the notebooks' original Quantum Informatics at Yonsei Academy copyright and attribution notices when sharing them.
