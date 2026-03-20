# 🧑‍💻 Introduction to Quantum Programming with CUDA-Q

> **Workshop materials for [PythonAsia 2026](https://2026.pythonasia.org/)**  
> 📅 March 22, 2026 · 13:15–15:15 · Yuchengco Hall 4F, Room Y409 · De La Salle University, Manila  
> 🎟️ [View session on schedule](https://pretalx.com/python-asia-2026/talk/AJHSH8/)

---

## 🔭 About this Workshop

The age of quantum computing is upon us — and you don't need a quantum computer or a physics degree to get started.

This workshop covers the fundamentals of quantum programming using **NVIDIA CUDA-Q**, the open-source platform that lets you write hybrid quantum-classical programs that run on both GPUs and real quantum hardware. We work through everything from first principles using Python — no prior quantum background required.

**By the end you will be able to:**

- Write and run a quantum circuit using `@cudaq.kernel`
- Measure superposition and entanglement with `cudaq.sample()`
- Compute expectation values with `cudaq.observe()`
- Swap between CPU, GPU, and QPU backends with one line
- Formulate a combinatorial optimisation problem with JijModeling
- Solve it with QAOA using Qamomile + CUDA-Q Solvers
- Compare classical (OpenJij SA) vs quantum (VQE / QAOA) results

---

## 📓 Notebooks

All notebooks run on **Google Colab with a T4 GPU runtime**.  
`Runtime → Change runtime type → T4 GPU` before installing.

| Notebook | Topic | Open |
|---|---|---|
| `cudaqx_fundamentals_pythonasia2026.ipynb` | Qubits · Gates · Circuits · Measurement · Bell State · GHZ · `observe()` · Backend swap | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dyjdlopez/intro_2_quantum/blob/main/cuda-q/pythonasia26/cudaqx_fundamentals_pythonasia2026.ipynb) |
| `cudaqx_qaoa_maxcut_pythonasia2026.ipynb` | VQC · Max Cut · QUBO · OpenJij SA · Qamomile · VQE · QAOA | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dyjdlopez/intro_2_quantum/blob/main/cuda-q/pythonasia26/cudaqx_qaoa_maxcut_pythonasia2026.ipynb) |

---

## ⚡ Quickstart

```bash
# Notebook 1 — CPU runtime is fine
!pip install cudaq -q

# Notebook 2 — requires GPU runtime (T4 or better)
!pip install cudaq -q
!pip install cudaq-solvers==0.3.0 -q
!pip install jijmodeling jijmodeling-transpiler openjij -q
!pip install "qamomile[cudaq]" -q
```

---

## 📦 Packages

| Package | What it does | Docs |
|---|---|---|
| [`cudaq`](https://pypi.org/project/cudaq/) | NVIDIA CUDA-Q Python API — kernels, sampling, simulation | [docs.nvidia.com/cuda-q](https://nvidia.github.io/cuda-quantum/latest/) |
| [`cudaq-solvers`](https://pypi.org/project/cudaq-solvers/) | VQE and QAOA solver loops built on CUDA-Q | [cudaqx docs](https://nvidia.github.io/cudaqx/components/solvers/introduction.html) |
| [`jijmodeling`](https://pypi.org/project/jijmodeling/) | Symbolic mathematical modelling language (Jij Inc.) | [jijmodeling docs](https://jij-inc.github.io/JijModeling-Tutorials/introduction.html) |
| [`jijmodeling-transpiler`](https://pypi.org/project/jijmodeling-transpiler/) | Compiles JijModeling problems to QUBO/Ising dictionaries | [transpiler docs](https://www.documentation.jijzept.com/docs/jijmodelingtranspiler/) |
| [`openjij`](https://pypi.org/project/openjij/) | Ising/QUBO solver — Simulated Annealing classical baseline | [openjij docs](https://openjij.github.io/OpenJij/) |
| [`qamomile[cudaq]`](https://pypi.org/project/qamomile/) | Converts JijModeling QUBO → QAOA circuit + Hamiltonian for CUDA-Q | [qamomile docs](https://jij-inc.github.io/Qamomile/en/) |
| [`networkx`](https://pypi.org/project/networkx/) | Graph construction and visualisation | [networkx docs](https://networkx.org/documentation/stable/) |

---

## 🗺️ Workshop Flow

```
Notebook 1                             Notebook 2
───────────────────                    ───────────────────
Section 0  Setup                       Section 0  Setup (GPU)
Section 1  Qubits, Gates,              Section 1  VQC & QAOA theory
           Circuits, Measurement       Section 2  Max Cut problem
Section 2  Bell State                  Section 3  NetworkX graph
Section 3  GHZ State                   Section 4  JijModeling + OpenJij SA
Section 4  cudaq.sample()              Section 5  Qamomile → CUDA-Q circuit
Section 5  cudaq.observe()             Section 6  VQE + QAOA + comparison
Section 6  Backend swap                Section 7  Wrap-up
Section 7  Wrap-up
```

---

## 👤 Speaker

**Dylan Josh Lopez, M.Sc.**  
Ph.D. Candidate · Chung Yuan Christian University (CYCU), Taoyuan, Taiwan  
Director for Partnerships & Collaboration · [Quantum Computing Society of the Philippines (QCSP)](https://qcsp.ph)  

Special thanks to NVIDIA AI Technology Center (NVAITC), Taipei, for supporting this talk!

---

## 🔗 Further Resources

- 📦 **CUDA-Q Academic** — self-paced modules from basics to research-grade algorithms  
  [github.com/NVIDIA/cuda-q-academic](https://github.com/NVIDIA/cuda-q-academic)
- 🌐 **CUDA-Q documentation** — [nvidia.github.io/cuda-quantum](https://nvidia.github.io/cuda-quantum/latest/)
- ☁️ **qBraid** — GPU-enabled cloud for CUDA-Q notebooks — [qbraid.com](https://qbraid.com)
- 🇵🇭 **QCSP** — [qcsp.ph](https://qcsp.ph)

---

## 📄 License

Workshop materials are released under the [Apache License 2.0](../../LICENSE).  
© 2026 Dylan Josh Lopez
