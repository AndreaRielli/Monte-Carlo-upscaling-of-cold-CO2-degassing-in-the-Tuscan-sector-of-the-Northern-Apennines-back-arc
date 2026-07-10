# Monte Carlo upscaling of cold CO₂ degassing in the Tuscan sector of the Northern Apennines back-arc

This repository contains the input data and Python scripts used to reproduce the Monte Carlo upscaling of cold CO₂ degassing in the Tuscan sector of the Northern Apennines back-arc.

The scripts generate Figure 8A, Figure 8B, and Supplementary Figure S9A-C.

Input data are site-integrated cold CO₂ outputs from five quantified cold-degassing localities:

- Micciano
- Libbiano
- Palazzo al Piano
- Montemiccioli
- Occhibolleri

Monte Carlo uncertainty is reported as the 5th-95th percentile range.

## Repository contents

This repository includes:

- input data for the five quantified cold-degassing sites;
- Python scripts for Monte Carlo upscaling;
- scripts to reproduce Figure 8A, Figure 8B, and Supplementary Figure S9A-C;
- exported figure files;
- summary outputs from the Monte Carlo runs.

## Software and reproducibility

The archived simulations were run using:

- Python 3.11.15
- NumPy
- Matplotlib
- NumPy random generator seed = 42

Curves and probability contours are smoothed for plotting only. Printed statistics are calculated from the original unsmoothed Monte Carlo outputs. Point clouds are horizontally jittered only for visualisation.

## Release history

### v1.0.2

Diagnostic update for the leave-one-out sensitivity test.

This release:

- unifies the Monte Carlo workflow used for Figure 8A, Figure 8B, and Supplementary Figure S9A-C;
- calculates the all-sites Dirichlet-weighted Monte Carlo matrix once and reuses it across figures;
- updates the Figure S9C leave-one-out diagnostics;
- reports log-space sigma, p5, p95, p95/p5, and p5/reference values directly from the archived run;
- replaces the ambiguous term `reduction factor` with `median ratio all-sites/LOO`;
- adds a symmetric deviation factor, calculated as `max(ratio, 1 / ratio)`;
- corrects the diagnostic check for non-Montemiccioli exclusions by reporting the largest deviation from unity.

These changes ensure that the values reported in the Supporting Information are calculated directly from the archived v1.0.2 run.

### v1.0.1

Archived release for Zenodo.

### v1.0

First public release of the input data and Python scripts used to reproduce the Monte Carlo upscaling of cold CO₂ degassing.

## License

The Python scripts are released under the MIT License.

The input data, figures, and documentation are released under the Creative Commons Attribution 4.0 International License (CC-BY-4.0), unless otherwise stated.
