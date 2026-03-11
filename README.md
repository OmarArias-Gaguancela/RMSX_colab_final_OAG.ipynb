# RMSX Google Colab Notebook: User-Friendly Adaptation

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1QurBP0dpuu3uKvKq88_cU49qpDZln9Xg?usp=sharing)

## Overview

This repository contains a Google Colab notebook that adapts the [RMSX and Flipbook package](https://github.com/AntunesLab/rmsx) by AntunesLab into a guided, user-friendly workflow. The original package is a powerful tool for high-resolution mapping of protein motions over time, combining the features of RMSD and RMSF into a unified metric called RMSX.

The **novelty of this notebook** is accessibility: the original codebase assumes a local Python/R/ChimeraX environment. This notebook removes that barrier by running entirely in Google Colab — no local installation required. It is restructured with step-by-step cells, inline explanations, and simplified parameter inputs so that researchers can get results quickly, even without a dedicated computational setup.

## What is RMSX?

RMSX (Root Mean Square X) is a time-series RMSF metric that combines the positional deviation sensitivity of RMSD with the per-residue resolution of RMSF. It divides a trajectory into time slices and computes residue-level fluctuations within each slice, producing a heatmap that shows *where* and *when* a protein moves.

The package also includes **Flipbook**, a 3D visualization tool that generates multi-model PDB files colored by RMSX values, viewable in ChimeraX or VMD.

**Original paper:**
> Beruldsen, F., de Freitas, M.V. & Antunes, D.A. High resolution mapping of protein motions in time and space with RMSX and Flipbook. *Scientific Reports* (2026). https://doi.org/10.1038/s41598-026-39869-7

**Original repository:** https://github.com/AntunesLab/rmsx

## What This Notebook Adds

The original QuickStart notebook (`RMSX_FlipBook_Quickstart.ipynb`) is designed for a local Jupyter environment with Git, R, and ChimeraX pre-installed. This Colab adaptation:

- Installs all dependencies (Python packages, R, required R libraries) directly in the Colab runtime
- Provides clearly labeled input cells for uploading trajectory and topology files
- Adds inline markdown explanations for each analysis step
- Handles Colab-specific display for output heatmaps and plots
- Includes inline GIF display for PyMOL-generated animations
- Covers single-chain RMSX, multi-chain RMSX, and RMSF fluctuation reporting

## How to Use

1. Click the **Open in Colab** badge above
2. Upload your topology file (`.pdb` or `.gro`) and trajectory file (`.xtc` or `.dcd`) when prompted
3. Set your parameters (chain ID, number of slices, color palette) in the designated input cell
4. Run cells sequentially — each section is self-contained with explanations

## Requirements

No local installation needed. The notebook installs everything at runtime in Colab:

- Python 3.8+
- `rmsx` (installed via pip from the AntunesLab repo)
- MDAnalysis
- R + ggplot2, viridis, dplyr (auto-installed on first run)

## Citation

If you use this notebook in your work, please cite the original RMSX paper:
```
@article{Beruldsen2026RMSXFlipbook,
  author = {Beruldsen, F. and de Freitas, M. V. and Antunes, D. A.},
  title = {High resolution mapping of protein motions in time and space with RMSX and Flipbook},
  journal = {Scientific Reports},
  year = {2026},
  doi = {10.1038/s41598-026-39869-7}
}
```

## Acknowledgments

This notebook adapts code from the [AntunesLab/rmsx](https://github.com/AntunesLab/rmsx) repository. Full credit for the RMSX algorithm, Flipbook visualization, and underlying R/Python implementation goes to the original authors. This work only repackages their tool for a Colab-friendly environment.
