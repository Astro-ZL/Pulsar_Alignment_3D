# Pulsar Alignment 3D
This repository contains the Python-based implementation and data for the paper:

"**Constraining the Pulsar 3D Velocity Distribution: The Impact of Spin-Velocity Alignment**" Zheng Li, Xing-Jiang Zhu, et al. (2026)

## Overview

This project reconstructs the intrinsic 3D velocity distribution of pulsars by incorporating the observational constraint of spin-velocity alignment. We utilize a hierarchical Bayesian framework to compare various velocity models (e.g., Maxwellian, Bimodal Maxwellian, Log-Normal) against traditional isotropic assumptions.

## Directory Structure

• code/: Jupyter notebooks for Bayesian sampling, data processing, and figure generation.

• data/: Input datasets, including pulsar kinematic parameters and polarization geometry sourced from the ATNF catalogue and recent literature.

## Code Descriptions

### 1. Primary Analysis (18-Pulsar Sample)

File/Description

V_3D_18_20err_aligment.ipynb:  Generates 3D data for the 18-pulsar sample under the alignment assumption with a 20% distance error.

pulsar_kick_fixed.ipynb	：Main Bayesian sampling program for the aligned case.

pulsar_kick_fixed_isotropy.ipynb: Bayesian sampling program assuming spatial isotropy (comparative analysis).

pulsar_kick_fixed_radial.ipynb:Bayesian reconstruction of the radial velocity distribution under alignment.

### 2. Robustness & Sensitivity Tests

• pulsar_kick_fixed_50_percent.ipynb & pulsar_kick_fixed_100_percent.ipynb: Bayesian sampling results when increasing distance uncertainties to 50% and 100%.

• pulsar_kick_fixed_noback.ipynb & pulsar_kick_fixed_noback_isotropy.ipynb: Test programs for 7 pulsars older than 10 Myr without applying dynamical backtracking.

### 3. Population Synthesis (Full Catalogue)

Scripts for analyzing the broader pulsar population as presented in the Appendix:

• Pulsar_kick_all_465_3D.ipynb: Analysis for the full sample of 465 pulsars.

• Pulsar_kick_isolated_154_3D.ipynb: Analysis for 154 isolated young pulsars.

• pulsar_kick_recycled_225.ipynb: Analysis for 226 recycled pulsars.

### 4. Visualization and Post-processing

• pulsar_aligment_Gamma.ipynb: Posterior extraction and plotting for the Gamma distribution model.

• angle_pulsar.ipynb: Source code for generating Figure 2.

• Appendix.ipynb: Code for generating all figures in the paper's Appendix.

## Dependencies

The analysis is primarily conducted in Python using the following libraries:

• bilby: For Bayesian inference and nested sampling.

• numpy, pandas, matplotlib, seaborn: For data manipulation and plotting.

• galpy: For Galactic potential modeling and dynamical backtracking

## Citation

If you use this code or our results in your research, please cite:

Li, Z., Zhu, X.-J., et al. (2026). Constraining the Pulsar 3D Velocity Distribution: The Impact of Spin-Velocity Alignment. The Astrophysical Journal.
