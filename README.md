# Entangled Photon Distribution - Data Analysis

Data acquisition and processing notebooks for my Bachelor's Thesis, focused on the experimental characterization and quantum state tomography of an entangled photon pair distribution system. 

This repository contains the Python scripts and analytical pipelines used to process raw laboratory data, reconstruct quantum states, and evaluate the physical properties of the optical distribution link.

## 🔬 Core Functionalities & Notebooks

### 1. Quantum State Tomography & Entanglement Metrics (`Tomography_QST*.ipynb`)
* **Density Matrix Reconstruction:** Implements both analytical (Moore-Penrose pseudoinverse) and Maximum Likelihood Estimation (MLE) methods with Cholesky parameterization to ensure physical (positive semi-definite, trace 1) density matrices.
* **Entanglement Characterization:** Calculates key quantum information metrics including Von Neumann entropy, Concurrence (Wootters), Entanglement of Formation, Negativity (Peres-Horodecki), and Fidelity to standard Bell states.
* **Monte Carlo Error Analysis:** Simulates the propagation of instrumental angular uncertainties (e.g., $\pm 1^\circ$ in waveplates) to establish 95% confidence intervals for purity and entanglement metrics.

### 2. TCSPC Data Processing (`Histogram.ipynb`)
* **Coincidence Logic:** Processes raw time-tagged data from SPAD detectors to analyze temporal correlations.
* **Signal Analysis:** Evaluates Coincidence-to-Accidental Ratio (CAR), Signal-to-Noise Ratio (SNR), and true coincidences by applying dynamic integration windows to experimental histograms[cite: 7]. 
* **System Comparison:** Compares singles and coincidence rates between direct source-detector connections and long-distance fiber distribution configurations[cite: 7].

### 3. Optical Link Characterization (`OTDR ANALYSIS.ipynb`)
* **Fiber Attenuation Analysis:** Processes Optical Time-Domain Reflectometer (OTDR) data at 1310 nm to break down span losses, identifying specific connector and splice attenuation events across the distribution channels[cite: 8].
* **Performance Prediction:** Compares measured coincidence reductions against theoretical expectations derived from power meter and OTDR transmission efficiency calculations[cite: 8].

### 4. Simulations & Modeling (`PMD Evolution.ipynb`, `Gaussian.ipynb`)
* **Decoherence Modeling:** Simulates the effect of Polarization Mode Dispersion (PMD) on the purity and concurrence of entangled states propagating through Polarization-Maintaining (PM) fibers[cite: 9].
* **Statistical References:** Generates standard Gaussian distribution plots for theoretical baseline comparisons[cite: 6].

## 🛠️ Tech Stack
* **Language:** Python
* **Data Processing:** NumPy, SciPy (L-BFGS-B optimization for MLE)
* **Visualization:** Matplotlib, Jupyter Notebook

## 📄 License
This project is licensed under the MIT License.
