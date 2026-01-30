## Overview

This repository provides MATLAB simulation code for the paper:

**“Advanced Codebook Generation Using High-Resolution k-Means Clustering to PMI Data”**

The proposed method generates an advanced beamforming codebook using **only PMI (Precoding Matrix Indicator) feedback** from UE, without requiring extra signaling or additional CSI exchange. The workflow is:

1. **PMI collection** from UE feedback (3GPP-compliant feedback assumption)
2. **PMI resolution enhancement** via **Kernel Density Estimation (KDE)**
3. **Codebook refinement** using **k-means clustering**
4. **Iterative codebook update** to adapt autonomously to environmental changes

As a result, the system can improve beamforming performance while maintaining **3GPP compliance** and avoiding additional overhead.

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

## Quick Notes

- If you encounter missing-function errors (e.g., `ksdensity`), confirm that the **Statistics and Machine Learning Toolbox** is installed and licensed.
- For reproducibility, consider setting the random seed (e.g., `rng(...)`) before running experiments.
