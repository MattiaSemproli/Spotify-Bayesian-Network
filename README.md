# Spotify Bayesian Network

Project for the **Fundamentals of AI and Knowledge Representation** course (Module 3 —
Bayesian Networks), Master's Degree in Artificial Intelligence, University of Bologna.

## Overview

This project builds a custom Discrete Bayesian Network to model which musical characteristics
of a Spotify track (genre, tempo, danceability, energy, mood/valence, explicit content) are
associated with its popularity. The network structure is manually defined and justified by
domain reasoning and verified correlations in the data, with parameters fit via Maximum
Likelihood Estimation and exact inference performed via Variable Elimination.

The notebook covers predictive, diagnostic, and intercausal ("explaining away") reasoning,
along with conditional independence / d-separation checks, Markov blankets, the local
semantics (chain-rule factorization), and a comparison against automated structure-learning
algorithms (Hill-Climb Search and PC).

## Contents

| File | Description |
|---|---|
| `spotify_bayesian_network.ipynb` | Full notebook: data preprocessing, network definition, parameter learning, inference queries, and supplementary theoretical analysis |
| `main.pdf` | 2-page project report (course template format) |
| `main.tex` | LaTeX source for the report |
| `network_diagram.png` | Bayesian Network structure diagram |
| `dataset.csv` | Spotify Tracks Dataset (see source below) |

## Dataset

[Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)
(Kaggle, maharshipandya) — track-level audio features and popularity scores across 114 genres.

## Setup

Requires Python 3.10+. Recommended: use a virtual environment.

```bash
python -m venv faikr-venv
faikr-venv\Scripts\activate      # Windows
source faikr-venv/bin/activate   # macOS/Linux
pip install ipykernel
```

Then open `spotify_bayesian_network.ipynb` and select the `faikr-venv` kernel. The notebook's
setup cell checks for and installs any missing dependencies (`pandas`, `networkx`,
`matplotlib`, `pgmpy`) automatically.

## Running

Run all cells top to bottom. The notebook is self-contained: it loads `dataset.csv`,
preprocesses it, builds and fits the network, and runs all inference queries and analyses.
