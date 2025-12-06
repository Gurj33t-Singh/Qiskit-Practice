# QiskitLearning

A collection of Qiskit notebooks implementing and analysing foundational quantum algorithms, with reproducible circuits, state-vector checks, and measurement analysis.

## Contents

- Environment files
  - [env_qiskit.yml](env_qiskit.yml) — conda env for Qiskit-based notebooks
  - [pip-requirements.txt](pip-requirements.txt) — pip dependencies for Qiskit-based notebooks
- Notebooks
	- [Notebooks/Berinstein-Vazarani.ipynb](Notebooks/Berinstein-Vazarani.ipynb) — Bernstein–Vazirani algorithm and oracle helpers for secret bit string.
	- [Notebooks/Deutsch-Jozsa.ipynb](Notebooks/Deutsch-Jozsa.ipynb) — n-qubit Deutsch–Jozsa and oracle builders.
	- [Notebooks/Deutsch.ipynb](Notebooks/Deutsch.ipynb) — single-qubit Deutsch algorithm and simple oracles.
	- [Notebooks/Quantum-Teleportation.ipynb](Notebooks/Quantum%20Teleportation.ipynb) — teleportation examples (classical and statevector variants).
	- [Notebooks/Bell-State.ipynb](Notebooks/Bell%20State_Qiskit.ipynb) — Bell states, simulation, and noise experiments.

> Open any notebook from the `Notebooks/` folder to inspect the implemented circuits, helper functions, and simulation calls.

## Quick start

1. Create a conda environment (recommended)
   - Qiskit environment:
     ```sh
     conda env create -f env_qiskit.yml
     conda activate qiskit-env
     ```
   - Or create a fresh env:
     ```sh
     conda create --name <env_name> python=3.13.5
     conda activate <env_name>
     ```
   - Or install dependencies with pip:
     ```sh
     pip install -r pip-requirements.txt
     ```
2. Install Jupyter (if not included) and launch:
   ```sh
   jupyter lab
   ```
   Then open any notebook in the `Notebooks/` directory.

3. Run simulations
   - Many notebooks use `qiskit_aer.AerSimulator()` or `qiskit_aer.Aer.get_backend('qasm_simulator')`.
   - Some examples demonstrate `FakeManilaV2` from IBM fake provider for device-like behaviour.


## Tips & notes

- Qiskit and notebook code assume Qiskit Aer is available (check `env_qiskit.yml`).
- Notebook cell comments document function and variable names; open the notebook to jump to helper functions such as [`deutsch_jozsa`](Notebooks/Deutsch-Jozsa.ipynb) and [`bernstein_vazarani`](Notebooks/Berinstein-Vazarani.ipynb).
- Qiskit uses little-endian qubit ordering (LSB→MSB). Some notebooks print reversed strings to match physics notation — see Bernstein–Vazirani outputs.

## Contributing

- Add new notebooks to the `Notebooks/` folder.
- If you add dependencies, update the corresponding environment file (`env_qiskit.yml`) and describe the change in this README.

## License & Contact

- This repository is for learning and demonstration. Use and adapt the code as needed.
- For questions, open an issue or edit the repository to add clarifying examples.
