# Yonsei Qiskit Fall Fest (Beginner & Challenger) — Short README

Overview
--------
This workspace contains two tutorial notebooks for the Qiskit Fall Fest @ Yonsei 2025 event:

- [YonseiQiskitFallFest/qff25_yonsei_challenger.ipynb](YonseiQiskitFallFest/qff25_yonsei_challenger.ipynb) — challenger-level notebook (main focus).
- [YonseiQiskitFallFest/qff25_yonsei_beginner.ipynb](YonseiQiskitFallFest/qff25_yonsei_beginner.ipynb) — beginner-level notebook.

Both notebooks demonstrate quantum simulation and experiment design using Qiskit and Qiskit addons. They include hands-on tasks (graded via an included grader) and example pipelines for Operator Backpropagation and the Elitzur–Vaidman bomb detector.

Key code highlights
-------------------
- Operator Backpropagation (Challenger notebook)
  - Uses the `backpropagate()` routine from the OBP addon: [`qiskit_addon_obp.backpropagation.backpropagate`](qiskit_env/Lib/site-packages/qiskit_addon_obp/backpropagation.py)
  - Builds Hamiltonians and time-evolution circuits via:
    - [`qiskit_addon_utils.problem_generators.generate_xyz_hamiltonian`](qiskit_env/Lib/site-packages/qiskit_addon_utils/problem_generators/generate_xyz_hamiltonian.py)
    - [`qiskit_addon_utils.problem_generators.generate_time_evolution_circuit`](qiskit_env/Lib/site-packages/qiskit_addon_utils/problem_generators/generate_time_evolution_circuit.py)
  - Circuit slicing utilities:
    - [`qiskit_addon_utils.slicing.slice_by_gate_types`](qiskit_env/Lib/site-packages/qiskit_addon_utils/slicing/__init__.py)
    - [`qiskit_addon_utils.slicing.combine_slices`](qiskit_env/Lib/site-packages/qiskit_addon_utils/slicing/__init__.py)

- Bomb detector interferometer (Beginner & Challenger notebooks)
  - Implements Mach–Zehnder interferometer circuits and grader-driven tasks:
    - `make_no_bomb_circuit()` and `make_bomb_circuit()` appear in the challenger notebook (see the file link above).

How to run
----------
1. Create / activate the Python venv (the repo already contains an example environment at `qiskit_env/`).
2. Install the notebook prerequisites (notebook cells already show these commands):
   - pip install qiskit_addon_obp qiskit_addon_utils
   - pip install "qiskit[visualization]" qiskit-ibm-runtime qiskit-aer qiskit-addon-cutting
3. Open and run the notebooks in order. Start with the beginner notebook to get familiar, then run the challenger notebook.

Notes
-----
- The challenger notebook demonstrates trade-offs of OBP: reduced quantum circuit depth vs larger classical observable complexity and truncation error control.
- The grader used by the notebooks is imported inside the notebooks (see the challenger notebook header). Run the setup cell before the graded cells.
- Relevant source files for the addon functions are included in the Python site-packages under `qiskit_env/Lib/site-packages/` (links above).

If you want a longer README or a CONTRIBUTING guide, I can expand this file.