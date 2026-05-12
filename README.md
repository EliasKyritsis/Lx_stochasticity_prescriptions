# Prescriptions for the calculation of the total X-ray luminosity of star-forming galaxies accounting for stochastic sampling of the HMXBs XLF


Repository for the application of the prescriptions presented in the paper "Prescriptions for the stochasticity effect on the integrated X-ray luminosity of star-forming galaxies:Implications for selecting star-forming galaxies and AGN in X-ray surveys"\

Astronomy & Astrophysics\
ArXiv: TBW \
ADS: TBW \
Publisher (A&A): TBW 

## Authors: 
Elias Kyritsis, Andreas Zezas, and Konstantinos Kovlakas

## Abstract 
**Context.**  The integrated X-ray luminosity (L$_{X}$) of star-forming galaxies originates primarily by populations of high-mass X-ray binaries (HMXB). However, the discrete nature of these populations introduces stochastic sampling effects, affecting the shape of their underlying X-ray Luminosity function (XLF), and biasing the interpretation of observed scaling relations. \
**Aims.** In this work we investigate how stochastic sampling of the HMXB XLF impacts the predicted integrated L$_{x}$ of galaxies across a broad range of star-formation and metallicity conditions, and quantify the resulting scatter in order to provide a statistical framework for interpreting X-ray observations of galaxies. \
**Methods.** By performing Monte Carlo (MC) simulations  we derived distributions of the integrated L$_{X}$ of galaxies over a wide grid of star-formation rate (SFR) and metallicity, covering the broad range of conditions observed in star-forming galaxies. By measuring statistical quantities that delineate the complex shapes of these distributions, we parametrized the luminosity scatter by fitting surfaces to the upper and lower L$_{X}$ bounds as function of SFR and gas-phase metallicity. \
**Results.** We provide a practical set of prescriptions to calculate the expected integrated L$_{X}$ for a given SFR and metallicity, fully accounting for stochastic effects without the need to rerun the computationally expensive sampling of the HMXB XLF for each individual galaxy. Application of these prescriptions to local and higher-redshift galaxy samples, shows that stochasticity must be considered before attributing differences in L$_{X}$ to intrinsic population properties. Furthermore, a galaxy simulation study across z =0.5–5 showed mild intrinsic redshift evolution of the stochastic scatter, mirroring the evolution of SFR and metallicity, with minimum scatter at z$\sim$2.5 where the cosmic star-formation density reached its maximum. In addition, our prescritions can be used to quantify the bias introduced in the redhsift dependent L$_{X}$-SFR-Metallicity scaling relations due to the flux-limited nature of the X-ray surveys. Finally, we find that at low redshifts, stochastic effects can raise L$_{X}$ by up to 1 dex with respect to the mean relation, leading to overlap with the regime of low-luminosity AGN (LLAGN), thus potentially biasing the classification of X-ray sources in deep-field surveys.  \
**Conclusions.** Our results demonstrate that stochastic sampling of the HMXB XLF is a fundamental source of scatter in the L$_{X}$/SFR relation, especially at low SFRs. The intrinsic scatter shows a mild evolution with redshift, and its imprint is modulated by the evolving SFR and metallicity of galaxies across cosmic time. Accounting for these effects is essential for interpreting the X-ray emission of galaxies, exploring potential biases of the current scaling relation imposed by the flux-limited surveys, and disentangling X-ray emission from normal star-forming galaxies from AGN activity in deep X-ray surveys. The prescriptions presented here offer a practical framework for constraining the scatter around the scaling relations, quantifying the likelihood of extreme outliers, and refining the classification of X-ray sources in current and future surveys.

## Application of the prescriptions
This repository contains all the needed files and the jupyter notebook (Python3) for the application of our prescreptions presented in the paper mentioned above. 

We provide a file that has a test sample of galaxies *(example_sample)* to test that your code works correctly. In addition, we provide the best-fit coefficients in the following files
- `Upper_bound_HDIs_best_fit_results.csv`
- `Low_bound_HDIs_best_fit_results.csv`


The code reproduces the lower and upper Highest Density Intervals (HDIs) of the total X-ray luminosity produced by high-mass X-ray binaries (HMXBs) for different confidence intervals: 68%, 90% ,99%, 99.9%. When you want the predictions for your own catalog of galaxies change this file with your catalog. The supported formats for your catalog is either 'fits' or 'csv'. 

- **Input**\
The input catalogue should contain at least the following columns:

| Column | Description |
|---|---|
| `SFR` | Star formation rate |
| `Metal` | Metallicity |


- **Output**\
Our code computes the predicted lower and upper luminosity logLx bounds for multiple confidence intervals.
**Produced columns** 
- `logLx_lower_68, logLx_upper_68`
- `logLx_lower_90, logLx_upper_90`
- `logLx_lower_99, logLx_upper_99`
- `logLx_lower_999, logLx_upper_999`




## Additional files
Along with all the required files and the code for the application of our prescriptions we also provide to the users the following:
- In file `L21_20000_draws.csv.zip` we provide the Lx draws of the HMXBs XLF from [Lehmer et al. 2021](https://ui.adsabs.harvard.edu/abs/2021ApJ...907...17L/abstract)
- Under the directory `Lx_SFR_metallicity_projections/` we provide the plots of the Lx vs SFR projections (for fixed Metallicity bins) and the Lx vs Metallicity (for fixed SFR bins).

## Contact author
ekyritsis@mpe.mpg.de
