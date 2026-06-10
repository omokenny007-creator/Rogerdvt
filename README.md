# Mixture Model Comparison on Noisy 16‑QAM Triplets

**Nonlinear Distortion Analysis in Optical Fibre Communications**

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Overview

This repository contains my MSc Data Science dissertation at Aston University. I investigate how **Kerr nonlinearity** and **EDFA amplifier noise** distort 16‑QAM signals in optical fibre networks – a key problem for increasing data capacity.

Using **probabilistic mixture models**, I characterise the nonlinear noise distribution and compare:

- Gaussian Mixture Model (GMM)
- Student‑t Mixture Model (tMM)
- Dirichlet Process GMM (DPGMM)

## Key Results

- **Optimal launch power**: −1.03 dBm → minimum BER = `2.23×10⁻⁴`
- **Multi‑component models** are strongly preferred at high power (nonlinear regime)
- **GMM and tMM** perform similarly; tMM converges reliably only at low power
- **Soft‑decision demapper** (using GMM noise model) gives negligible gain over hard decision – the covariance structure already captures the nonlinear distortion
- Noise distribution becomes increasingly **anisotropic** with higher launch power

## Repository Contents

- `dissertation_final_v8.ipynb` – main Jupyter notebook with all analysis (EDA, model fitting, BER evaluation, figures)
- `requirements.txt` – Python dependencies
- `LICENSE` – MIT license

## Getting Started

Clone the repo, install dependencies, and run the notebook:

```bash
git clone https://github.com/omokenny007-creator/Rogerdvt.git
cd Rogerdvt
pip install -r requirements.txt
jupyter notebook dissertation_final_v8.ipynb

