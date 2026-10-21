# Correlations in Oscillation Data and Their Impact on Neutrino Mixing Models

## Neutrino Mixing Schemes and NuFIT Correlations

This repository contains materials for the publication *Correlations in Oscillation Data and Their Impact on Neutrino Mixing Models*. It provides a Mathematica notebook for studying neutrino mixing schemes, including TM₁, TM₂, and partial μ–τ reflection symmetry.

The notebook includes usage examples and a function that constructs correlations involving up to six oscillation parameters from NuFIT correlation data. It also generates one-, two-, and three-dimensional plots of the resulting χ².

## Repository contents

- **`correlations.nb`** — Mathematica notebook containing the analysis functions, usage examples, and code for generating plots.

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

The analysis uses NuFIT χ² datasets for individual parameters and their correlations. The required one-dimensional tables are for θ₁₂, θ₁₃, θ₂₃, δCP, Δm²₂₁, and Δm²₃ℓ.

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
- `wget` and `xz` (for downloading and extracting the datasets on Linux)

## Downloading and preparing the NuFIT datasets

The NuFIT datasets are not included in this repository. The following commands download the NuFIT data files for both normal ordering (NO) and inverted ordering (IO), then extract them into a `datasets` directory.

Run the commands from the directory containing `correlations.nb`.

### NuFIT v6.1


```bash
mkdir -p datasets
cd datasets

wget https://www.nu-fit.org/sites/default/files/v61.release-TByes-NO.txt.xz
wget https://www.nu-fit.org/sites/default/files/v61.release-TByes-IO.txt.xz

xz -d v61.release-TByes-NO.txt.xz
xz -d v61.release-TByes-IO.txt.xz

cd ..
```
### NuFIT v6.0
```bash

mkdir -p datasets
cd datasets

wget https://www.nu-fit.org/sites/default/files/v60.release-TByes-NO.txt.xz
wget https://www.nu-fit.org/sites/default/files/v60.release-TByes-IO.txt.xz

xz -d v60.release-TByes-NO.txt.xz
xz -d v60.release-TByes-IO.txt.xz

cd ..
```
The xz -d command decompresses each .xz file and removes the compressed version. To keep the .xz files after extraction, use xz -dk instead.

After extraction, check that the files are present:
```bash

ls -lh datasets
```
Make sure the downloaded files and their paths match those expected by the Mathematica notebook.



## How to use

1. Open `correlations.nb` in Mathematica.
2. Make sure the `datasets` directory is in the location expected by the notebook.
3. Run the notebook cells to explore the examples, use the correlation-building function, and generate plots.

   
## Data format 

The NuFIT datasets are provided as text files containing tabulated χ² values. Depending on the dataset, the tables describe one-, two-, or three-dimensional distributions.

## Citation

If you use the code or other materials in this repository, please cite the associated publication:

[J. Gluza, B. Karmakar, and S. Zieba]], “Correlations in Oscillation Data and Their Impact on Neutrino Mixing Models,” https://doi.org/10.48550/arXiv.2610.27270, arXiv:2610.27270 [hep-ph].

The NuFIT data files included in this repository were obtained from www.nu-fit.org. If you use the NuFIT data or results, please also cite:

I. Esteban et al., “NuFit-6.0: Updated global analysis of three-flavor neutrino oscillations,” JHEP 12 (2024) 216, https://doi.org/10.1007/JHEP12(2024)216, arXiv:2410.05380 [hep-ph].

Please also cite NuFIT 6.1 (2025) and acknowledge www.nu-fit.org.

The license for the NuFIT data files is not specified on the NuFIT website. Any license applying to the original code and materials in this repository does not automatically apply to these third-party data files.

## Funding

This work was supported by the Polish National Science Centre (NCN) under grant No. 2020/37/B/ST2/02371, the Research Excellence Initiative of the University of Silesia in Katowice, and the Swiss National Science Foundation (SNSF) under grant No. MAPS IZ11Z0 230193.

## Contact

For questions about this repository, please contact szymon.zieba@us.edu.pl
