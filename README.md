## Overview

This repository provides MATLAB simulation code for the paper:

**Advanced Codebook Generation Using High-Resolution k-Means Clustering to PMI Data**  
DOI: https://doi.org/10.1109/LWC.2024.3516076

The proposed method generates an advanced beamforming codebook using **only PMI (Precoding Matrix Indicator) feedback** from UE, without requiring extra signaling or additional CSI exchange. The workflow is:

1. **PMI collection** from UE feedback (3GPP-compliant feedback assumption)
2. **PMI resolution enhancement** via **Kernel Density Estimation (KDE)**
3. **Codebook refinement** using **k-means clustering**
4. **Iterative codebook update** to adapt autonomously to environmental changes

As a result, the system can improve beamforming performance while maintaining **3GPP compliance** and avoiding additional overhead.

---

## Quick Start (Run Scripts)

You can directly run the following scripts to reproduce key results and compare performance:

- **`Demo.m`**
  - End-to-end demo that compares:
    - **Proposed PMI-based enhanced codebook**
    - **Baseline: perfect location-based approach**
    - **Baseline: conventional DFT codebook**
  - Metrics:
    - **Sum-rate**
    - **Beamforming gain**
  - Also helps compare **parameter selection/decision behavior** across methods.

- **`Figure_3.m`**
  - Reproduces results corresponding to **Figure 3** in the paper (or the accompanying document).

- **`Figure_6and7.m`**
  - Reproduces results corresponding to **Figures 6 and 7** in the paper (or the accompanying document).

> Tip: For reproducibility, consider setting a fixed random seed (e.g., `rng(0)`) before running experiments.

---

## Documentation (Detailed Explanation)

For more detailed descriptions of assumptions, parameter settings, and implementation notes, please refer to the PDF:

https://drive.google.com/file/d/18wfVdFwV4ZBds786L49ddFAyyQUDEI0C/view?usp=drive_link

---

## Requirements

### Main Application
- **Application**: MATLAB  
- **Recommended Version**: R2023a  
  - Other versions are also likely to be compatible, but behavior may vary depending on toolbox functions.
- **Description**: A high-level language and interactive environment for numerical computation, visualization, and programming; widely used for data analysis, algorithm development, and modeling.
- **Download**: https://mathworks.com/products/matlab.html

### Required MATLAB Toolbox
- **Toolbox**: Statistics and Machine Learning Toolbox  
- **Description**: Provides functions and tools for data analysis, statistical modeling, machine learning, and predictive analytics.  
  - In this simulator, **`ksdensity`** is used for **Kernel Density Estimation (KDE)**.
- **Download**: https://mathworks.com/products/statistics.html

---

## Contact

Questions and feedback are welcome.  
Please contact: ppp103207@gmail.com
