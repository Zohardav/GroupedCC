
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

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or later  
- `virtualenv` or similar for environment isolation  

### Installation

```bash
git clone https://github.com/yourusername/GroupedCC.git
cd grouped-mlem-compton
pip install -r requirements.txt
```

### Run a Basic Example
```bash
python src/grouped_mlem.py --config configs/example_config.json
```

## ⚙️ Features

- Flexible voxel grid configuration  
- Multiple event grouping strategies (energy-based, spatial, or custom)  
- Support for both cone and line-of-response imaging models  
- Built-in evaluation metrics: PSNR, SSIM, convergence tracking  
- Modular and extensible codebase for research or deployment  
- Compatible with NumPy, SciPy, and Matplotlib ecosystems  

## 📊 Visualization

Example output of the reconstructed gamma source using grouped MLEM:

![Reconstruction Example](results/reconstruction.png)

## 🧪 Testing

```bash
# activate virtual environment
source venv/bin/activate

# run test suite
pytest --maxfail=1 --disable-warnings -q
```
## 📚 References

- Z. Davidov et al., “Grouped MLEM Reconstruction for Efficient Gamma Imaging Using Compton Cameras,” *IEEE TIM*, Submitted - 2025.  
- L. A. Shepp and Y. Vardi, “Maximum Likelihood Reconstruction for Emission Tomography,” *IEEE Transactions on Medical Imaging*, vol. 1, no. 2, pp. 113–122, 1982.  

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👨‍🔬 Author

**Zohar Davidov**  
Email: davidov.zohar@gmail.com  
GitHub: [https://github.com/Zohardav](https://github.com/Zohardav)


