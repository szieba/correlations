# Correlations in Oscillation Data and Their Impact on Neutrino Mixing Models

## Neutrino Mixing Schemes and NuFIT Correlations

This repository contains materials for the publication *Correlations in Oscillation Data and Their Impact on Neutrino Mixing Models*. It provides a Mathematica notebook and NuFIT datasets for studying neutrino mixing schemes, including TM₁, TM₂, and partial μ–τ reflection symmetry.

The notebook includes usage examples and a function that constructs correlations involving up to six oscillation parameters from the available NuFIT correlation data. It also generates one-, two-, and three-dimensional plots of the resulting χ².

## Repository contents

- **Mathematica notebook** — contains the analysis function, usage examples, and code for generating plots.
- **`datasets/`** — contains NuFIT datasets in text format, used as input for the analysis.
- **`correlations.tar.gz`** — a compressed archive containing all the materials in this repository.

## Oscillation parameters

The datasets cover six neutrino-oscillation parameters. The labels used in the data files correspond to the following standard notation:

- `T12` — θ₁₂
- `T13` — θ₁₃
- `T23` — θ₂₃
- `DCP` — δCP
- `DMS` — Δm²₂₁
- `DMA` — Δm²₃ℓ

In the rest of this description, the parameters are referred to using the standard notation.

## Available NuFIT correlation data

The analysis uses the NuFIT χ² datasets available for individual parameters and their correlations. The repository includes one-dimensional tables for θ₁₂, θ₁₃, θ₂₃, δCP, Δm²₂₁, and Δm²₃ℓ.

Available two-dimensional correlation tables cover:

- θ₂₃–Δm²₃ℓ
- θ₁₃–θ₁₂
- θ₁₃–Δm²₂₁
- θ₁₂–Δm²₂₁
- θ₁₃–θ₂₃
- θ₁₃–Δm²₃ℓ
- θ₁₃–δCP
- θ₂₃–δCP
- Δm²₃ℓ–δCP
- θ₁₂–θ₂₃
- θ₁₂–δCP
- θ₁₂–Δm²₃ℓ
- Δm²₂₁–θ₂₃
- Δm²₂₁–δCP
- Δm²₂₁–Δm²₃ℓ

The available three-dimensional correlation table covers θ₂₃, Δm²₃ℓ, and δCP. These NuFIT datasets provide the experimental input used to explore the implications of different neutrino mixing schemes.

## Requirements

- Wolfram Mathematica

## How to use

1. If you have downloaded the compressed archive, extract it in the directory where you want to use the files:

   ```bash
   tar -xzf correlations.tar.gz

    Open the Mathematica notebook.
    Make sure the datasets directory is available at the path expected by the notebook.
    Run the notebook cells to view the examples, use the correlation-building function, and generate the plots.

Data format

The NuFIT datasets are provided as text files containing tabulated χ² values. Depending on the dataset, the tables describe one-, two-, or three-dimensional distributions.
Citation

If you use the code or other materials in this repository, please cite the associated publication:

[J. Gluza, B. Karmakar, and S. Zieba]], “Correlations in Oscillation Data and Their Impact on Neutrino Mixing Models,” arXiv:XXXX.XXXXX [hep-ph].

The NuFIT data files included in this repository were obtained from www.nu-fit.org. If you use the NuFIT data or results, please also cite:

I. Esteban et al., “NuFit-6.0: Updated global analysis of three-flavor neutrino oscillations,” JHEP 12 (2024) 216, https://doi.org/10.1007/JHEP12(2024)216, arXiv:2410.05380 [hep-ph].

Please also cite NuFIT 6.1 (2025) and acknowledge www.nu-fit.org.

The license for the NuFIT data files is not specified on the NuFIT website. Any license applying to the original code and materials in this repository does not automatically apply to these third-party data files.
Funding

This work was supported by the Polish National Science Centre (NCN) under grant No. 2020/37/B/ST2/02371, the Research Excellence Initiative of the University of Silesia in Katowice, and the Swiss National Science Foundation (SNSF) under grant No. MAPS IZ11Z0 230193.
Contact

For questions about this repository, please contact [szymon.zieba@us.edu.pl].
