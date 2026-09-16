
# realFluid-OpenFOAM

[![Latest Release](https://img.shields.io/badge/latest%20release-v1.0.0-blue)](https://github.com/danhnam11/DTLreactingFoam-12/releases)
[![Contributions](https://img.shields.io/badge/contributions-welcome-brightgreen)](https://github.com/danhnam11/DTLreactingFoam-12/pulls)
[![License](https://img.shields.io/badge/license-GPL--3.0-yellow)](https://github.com/danhnam11/DTLreactingFoam-12/blob/main/LICENSE)

[![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.cpc.2021.108264-red)](https://doi.org/10.1016/j.cpc.2021.108264) 
[![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.cpc.2025.109600-red)](https://doi.org/10.1016/j.cpc.2025.109600)

## Overview

A collection of different packages developed for numerical studies of real-fluid thermophysical properties and high-pressure reactive flows.

## Packages

### 1. realFluidThermophysicalModels library

A library of real-fluid thermophysical models for OpenFOAM: 
- Modified Soave-Redlich-Kwong (SRK) model for equation of state [1, 2].
- Peng-Robinson (PR) model for equation of state [3]
- JANAF-based model for real-fluid thermodynamic properties.
- Chung's model (1988) for dynamic viscosity and thermal conductivity [4].
- Mixture averaged model for mass diffusivity of individual species in a mixture in which the binary diffusion coefficients are based on Fuller's model and Takahashi correction at high pressure [5].
- Mixture averaged model for mass diffusivity of individual species in a mixture in which the binary diffusion coefficients are based on Standard Kinetic Theory [6].


| OpenFOAM Version | Source Code |
|---|---|
| OpenFOAM 6 | [realFluidThermophysicalModels-6](https://github.com/danhnam11/realFluidThermophysicalModels-6) |
| OpenFOAM 8 | [realFluidThermophysicalModels-8](https://github.com/danhnam11/realFluidThermophysicalModels-8) |

---

### 2. realFluidFoam solver

A low Mach number solver for simulations of turbulent flows at trancritical and supercritical conditions. In this solver, a pressure-based solution method with a modified PIMPLE algorithm [7] is employed to improve the stability while a fast and robust coupling Newton-Bisection algorithm is utilized to guarantee the convergency of fluid flow simulations under transcritical and supercritical conditions.


| OpenFOAM Version | Source Code |
|---|---|
| OpenFOAM 6 | [realFluidFoam-6](https://github.com/danhnam11/realFluidFoam-6) |
| OpenFOAM 6 | [LEMOS-6](https://github.com/danhnam11/LEMOS-6) (BCs for LES) |
| OpenFOAM 8 | [realFluidFoam-8](https://github.com/danhnam11/realFluidFoam-8) |
| OpenFOAM 8 | [LEMOS-8](https://github.com/danhnam11/LEMOS-8) (BCs for LES) |



## Installation

Please refer to the README.md file in the corresponding version-specific source repository for installation instructions.

## Documentation

Documentation and usage examples are provided in the respective source repositories. 

The detail implementation and extension guide are also provided. They are written for the development in OpenFOAM-6 but they can be referred for the development in other versions. 

## Authors 
This package was developed at the Clean Combustion & Energy Research Lab., Dept. of Mech. Engineering, Ulsan National Institute of Science and Technology (UNIST), Korea ([Prof. C.S. Yoo](https://csyoo.unist.ac.kr/)). If you publish results obtained by using this package, please cite our paper as follows:

- D. N. Nguyen, K. S. Jung, J. W. Shim, C. S. Yoo, Real-fluid thermophysicalModels: An OpenFOAM-based library for reacting flow simulations at high pressure, Comput. Phys. Commun. 273 (2022) 108264.

- D. N. Nguyen, C. S. Yoo, An OpenFOAM-based solver for modeling low Mach number turbulent flows at high pressure with real-fluid effects, Comput. Phys. Commun. 312 (2025) 109600.


If you need help with installation or have any questions, feel free to reach out: 
- danhnam11@gmail.com or nam.nguyendanh@hust.edu.vn 


## Reference
- [1] G. Soave, Equilibrium constants from a modified Redlich-Kwong equation of state, Chem. Eng. Sci. 27 (1972) 1197-1203.
- [2] D. Peng, D. Robinson, New two-equation of state, Ind. Eng. Chem. Fundam. 15(1976) 59-64. 
- [3] M. S. Graboski, T. E. Daubert, A modified Soave equation of state for phase equilibrium calculations. 1. Hydrocarbon systems, Ind. Eng. Chem. Process. Des. Dev. 17 (1978) 443-448.
- [4] T. C. Horng, M. Ajlan, L. L. Lee, K. E. Starling, M. Ajlan, Generalized multiparameter correlation for nonpolar and polar fluid transport properties, Ind. Eng. Chem. Res. 27 (1988) 671-679.
- [5] S. Takahashi, S. Takahashi, Preparation of a generalized chart for the diffusion coefficients of gases at high pressures, J. Chem. Eng. Japan 7 (1975) 417-420. 
- [6] R. J. Kee, F. M. Rupley, E. Meeks, J. A. Miller, CHEMKIN-III: a fortran chemical kinetics package for the analysis of gas-phase chemical and plasma kinetics, SAND96-8216 (1996). 
- [7] M. Jarczyk, M. Pfitzner, Large eddy simulation of supercritical nitrogen jets, in: 50th AIAA Aerospace Sciences Meeting Including the New Horizons Forum and Aerospace Exposition, Nashville, Tennessee, 2012. 
