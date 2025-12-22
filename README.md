# ML From Scratch

Machine learning algorithms implemented **from first principles**, using **Python for clarity** and **C++ for performance-critical core computations**.

This repository focuses on understanding how machine learning works at a fundamental level — from mathematical formulation and numerical optimization to low-level performance considerations.

---

## Motivation

Modern machine learning workflows often rely on high-level libraries that abstract away crucial details such as:

- optimization dynamics  
- numerical stability  
- computational complexity  
- performance bottlenecks  

This project rebuilds core machine learning algorithms **from scratch** in order to:

- develop a deep, principled understanding of ML algorithms  
- implement models correctly and transparently  
- identify and optimize performance-critical components in C/C++

---

## Design Principles

- **Minimal dependencies**  
  No scikit-learn, PyTorch, or TensorFlow implementations of the target algorithms.

- **Separation of concerns**  
  - Models define parameters and forward logic  
  - Optimizers handle parameter updates  
  - C++ modules accelerate computation-heavy kernels

- **Correctness and reproducibility first**  
  Each algorithm includes:
  - unit tests
  - numerical gradient checks (where applicable)
  - deterministic benchmarks

---

## What “From Scratch” Means

### Allowed
- NumPy (arrays and linear algebra)
- SciPy (basic utilities)
- matplotlib (visualization)
- pybind11 (Python ↔ C++ bindings)

### Not Allowed
- scikit-learn implementations of the same algorithms
- high-level autodiff or training frameworks

---

## Repository Structure

```text
ml-from-scratch/
├── algorithms/        # Core ML models
│   ├── linear/
│   ├── logistic/
│   ├── knn/
│   ├── trees/
│   └── clustering/
│
├── optim/             # Optimization algorithms
│   ├── gd.py
│   ├── sgd.py
│   ├── momentum.py
│   └── adam.py
│
├── cpp_core/          # Performance-critical C++ kernels
│   ├── distance/
│   ├── tree_split/
│   └── bindings/
│
├── datasets/          # Toy and synthetic datasets
│
├── benchmarks/        # Runtime and memory benchmarks
│
├── tests/             # Unit tests and gradient checks
│
└── README.md

