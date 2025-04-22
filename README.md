
# Grouped MLEM Algorithm for Compton Cameras
This repository contains the code and simulated datasets developed for the paper titled "A Compton Camera Resolution Enhancement by Increasing the Number of Sensors per Readout Channel," authored by Zohar Davidov.

This repository contains a Python implementation of a **Grouped Maximum Likelihood Expectation Maximization (MLEM)** algorithm for image reconstruction in **Compton camera systems**. The grouped approach improves computational efficiency and can enhance convergence behavior by exploiting event or voxel grouping strategies.

## 🔬 Overview

Compton cameras provide gamma‑ray imaging capabilities by utilizing Compton scattering kinematics. The reconstruction process involves solving a highly underdetermined inverse problem due to the conical nature of Compton scattering.

The **Grouped MLEM algorithm** modifies the classical MLEM by partitioning events or reconstruction voxels into structured groups, enabling:

- Parallel or staged updates  
- Improved memory management  
- Accelerated convergence in certain configurations  

This method is particularly suitable for high‑resolution or large‑scale detectors, such as in medical imaging, security scanning, or astrophysical applications.

## 📁 Repository Structure
```bash
grouped-mlem-compton/
├── src/
│   ├── grouped_mlem.py      # Main implementation of the Grouped MLEM algorithm
│   ├── compton_geometry.py  # System geometry, event generation, and kinematics
│   ├── utilities.py         # Helper functions for normalization, metrics, and plotting
│
├── data/
│   └── example_events.npz   # Sample input data (events, positions, energies)
│
├── results/
│   └── reconstruction.png   # Sample output image of reconstructed source
│
├── test/
│   └── test_mlem.py         # Unit tests for algorithm components
│
├── README.md                # This file
└── requirements.txt         # List of dependencies
```

