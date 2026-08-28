# T-SPR: Temporally-constrained Spatial Pattern Regression

Companion code repository for the manuscript:

**"Temporally-constrained Spatial Pattern Regression for Reconstruction of High-Resolution Hydrological Forcing"**
Vihotogbé Houssou, Julie Carreau
Polytechnique Montréal, GERAD, Mila, IVADO

Submitted to *Water Resources Research* (AGU).

---

## Overview

This repository contains the analysis code used to develop and evaluate **T-SPR**, an extension of the Spatial Pattern Regression (SPR) framework that combines anomaly-based interpolation with a first-order vector autoregressive (VAR(1)) temporal regularization for reconstructing gridded meteorological forcing fields (precipitation, minimum temperature, maximum temperature) from sparse station networks.

Three model variants are implemented and compared:

| Variant | Description |
|---|---|
| **SPR** | Original framework, operating directly on raw meteorological forcing |
| **A-SPR** | Anomaly-based variant, isolating the climatological decomposition |
| **T-SPR** | Anomaly-based variant with VAR(1) temporal regularization (main contribution) |

The methods are evaluated on:
- **Synthetic experiments**, using regional climate model (RCM) simulations as ground truth, across three virtual station densities (10%, 1%, 0.1%)
- **Real observations**, using station data from southern Québec, Canada

## Related repository

This work builds on the original SPR framework introduced in a previous article:

> Houssou, V., Carreau, J. (2026). Spatial pattern regression for meteorological fields interpolation. *EGUsphere* [preprint].

Code for the original SPR method (Article 1) is available at: **[TO COMPLETE — insert Article 1 repository URL]**

## Repository structure

```
├── data_preparation/       # [TO COMPLETE — adjust to your actual folder names]
├── spr/                    # SPR implementation
├── a_spr/                  # A-SPR implementation
├── t_spr/                  # T-SPR implementation (VAR(1) alternating minimization)
├── hyperparameter_selection/
├── evaluation_metrics/     # RMSE, SSIM, ACF, PSD, inter-day variability
├── figures/                # Scripts used to generate manuscript figures
├── real_observations/      # Real-data experiment (southern Québec)
├── LICENSE
└── README.md
```

> **Note:** the folder structure above is a template — please replace with your actual repository layout before publishing.

## Data sources

This repository contains **analysis code only**. It does not include raw input data, which are publicly available from their original sources:

- **Regional climate model simulations**: ClimEx project, CRCM5/CanESM2-driven simulations (ensemble member *kdj*)
  https://climex-data.srv.lrz.de/Public/

- **Real station observations**: Environment and Climate Change Canada (ECCC), historical climate data
  https://climate.weather.gc.ca/climate_data/bulk_data_e.html

## Requirements

- R (version 4.6.1)
- Python (version 3.10.12)
- Key Python packages: `numpy`, `pandas`, `scipy`, `matplotlib`, `seaborn`
- [TO COMPLETE — add any remaining packages, e.g. `scikit-learn`, and provide a `requirements.txt` or `environment.yml` if available]

## Citation

If you use this code, please cite the associated manuscript:

```bibtex
@article{houssou2026tspr,
  author  = {Houssou, Vihotogb{\'e} and Carreau, Julie},
  title   = {Temporally-constrained Spatial Pattern Regression for Reconstruction of High-Resolution Hydrological Forcing},
  journal = {Water Resources Research},
  year    = {2026},
  note    = {Submitted}
}
```

And the archived code itself:

```
[TO COMPLETE — Zenodo DOI will be generated automatically after the first GitHub Release]
```

## License

This project is licensed under the [TO COMPLETE — MIT or GPL-3.0] License — see the [LICENSE](LICENSE) file for details.

## Contact

Vihotogbé Houssou — vihotogbe-2.houssou@polymtl.ca
Julie Carreau — julie.carreau@polymtl.ca

Department of Mathematics and Industrial Engineering, Polytechnique Montréal
