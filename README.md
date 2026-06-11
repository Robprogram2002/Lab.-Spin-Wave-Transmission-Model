# Thermo-Optical Magnonic Crystals: Stratified Transfer Matrix Model

## Overview
This repository contains the Python source code and Jupyter Notebooks developed to numerically simulate the propagation of spin waves through dynamically reconfigurable thermal landscapes in Yttrium Iron Garnet (YIG) thin films. 

The numerical routine implements a **Stratified Transfer Matrix Method (TMM)** to calculate the power transmission spectra and predict the formation of magnonic band gaps. Unlike traditional TMM approaches designed for discrete geometrical steps, this code is generalized to handle continuous impedance mismatches arising from optically induced thermal gradients.

## Key Features
* **Thermal Landscape Synthesis:** Generates analytical temperature profiles $T(x)$ using standard Gaussian ($p=1$) and top-hat Super-Gaussian ($p>1$) distributions to simulate lateral thermal diffusion from laser-induced heating.
* **Magnetization Dynamics:** Maps the continuous spatial temperature profile to the saturation magnetization $M_s(x)$ using a linear approximation valid within the operational regime (298 K - 398 K), based on the Néel model.
* **Multimode Support:** Includes dispersion relation definitions to compute local wavenumbers $k(x)$ and group velocities $v_g$ for:
  * Magnetostatic Surface Waves (MSSW)
  * Backward Volume Magnetostatic Waves (BVMSW)
* **Bragg Scattering via Impedance Mismatch:** Discretizes the continuous profiles into infinitesimal strata, calculating local reflection coefficients $\Gamma$ to precisely model the Bragg scattering efficiency and band gap depths.

## Prerequisites
The project is built in Python 3. To run the simulations and visualize the theoretical predictions, the following standard scientific libraries are required:
* `numpy`
* `matplotlib`
* `jupyter`

## Repository Structure
* `matrix_transfer_temperature.ipynb`: The core Jupyter Notebook containing the full pipeline: variable definitions, continuous thermal profile generation, TMM matrix loop implementation, and visualization of the transmission spectra.
* `README.md`: Project documentation.

## Usage
1. Clone this repository to your local machine:
   ```bash
   git clone [https://github.com/your-username/thermo-optical-magnonics.git](https://github.com/your-username/thermo-optical-magnonics.git)
