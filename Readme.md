# Quantum Support Vector Machines for High-Energy Physics Data

Over the past several years, quantum machine learning (QML) has provided new
perspectives on how parameterized quantum circuits can be interpreted and
trained as machine learning models. Beyond early analogies with neural networks,
it has become increasingly clear that a large class of QML models is more
naturally understood through the lens of kernel methods, with the Support Vector
Machine (SVM) playing a central role.

In particular, quantum feature maps and fidelity-based kernels enable the
construction of quantum kernel SVMs (QSVMs), where the role of the kernel is
played by the overlap between quantum states encoding classical data. This
connection has been explored extensively in the literature, including works by
Schuld and Killoran (2018), Havlíček et al. (2018), Liu et al. (2020), Huang et
al. (2020), and the systematic overview by Schuld (2021), which serves as a
conceptual reference for this notebook.

---

## Quantum Chromodynamics and Equation-of-State Classification

Quantum Chromodynamics (QCD) predicts that strongly interacting matter undergoes
distinct phase transitions under extreme conditions of temperature and baryon
density. In particular, a quark–gluon plasma (QGP) is expected to form in the
early universe and can be recreated experimentally in relativistic heavy-ion
collisions.

A central objective of heavy-ion physics is the determination of the QCD
equation of state (EoS) governing these transitions. Because the microscopic
dynamics of the collision are highly complex and non-equilibrium in nature, the
EoS cannot be measured directly. Instead, it must be inferred from correlations
and collective observables measured in the final-state particle distributions,
such as flow harmonics and event-plane correlations.

Previous studies have demonstrated that classical machine learning models,
including linear classifiers and deep neural networks, can successfully
distinguish between different EoS scenarios using such observables. These
results suggest that meaningful information about the underlying phase structure
survives the full dynamical evolution of the collision.

---

## Scope of this work

Motivated by these findings, this notebook explores quantum machine learning
approaches—specifically quantum kernel methods and variational quantum
classifiers—as alternative models for EoS-related classification tasks.

The focus here is **not** on outperforming classical deep learning models, but
rather on:

- Verifying the correct construction of quantum kernels for physically motivated
  observables
- Demonstrating the trainability of variational quantum models on QCD-inspired
  data
- Analyzing qualitative behavior and computational scaling in a controlled
  verification regime

Due to the known computational cost of quantum kernel methods, experiments are
performed on reduced, representative subsets of the dataset. This approach
follows standard practice in quantum machine learning studies and allows for
transparent validation of model behavior without overextending computational
resources.
