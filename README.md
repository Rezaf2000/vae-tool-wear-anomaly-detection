# Beta-VAE for Tool Wear Anomaly Detection

An educational view of a disentangled variational autoencoder for monitoring milling-tool wear using the UC Berkeley milling dataset. The upstream study combines a temporal convolutional network with anomaly scores in input and latent spaces.

## Problem and method

Tool degradation is inferred from sensor signals collected during machining. A beta-VAE learns a compact representation; reconstruction and latent-space behavior support anomaly detection. The notebook presents data preparation, modeling, threshold selection, and visual analysis.

## Repository map

| Path | Purpose |
| --- | --- |
| `milling-tool-wear-beta-vae.ipynb` | Main experimental notebook |
| `data_prep.py`, `tcn.py`, `threshold.py` | Preparation, temporal modeling, and threshold analysis |
| `models/best_models/` | Upstream saved model artifacts |
| `images/` | Existing result figures |
| `hahn2021self.pdf` | Upstream research paper |

## Upstream reported results

The upstream README reports PR-AUC **0.45** across cutting parameters and **0.80** for shallow-depth cuts. These are the original study's results and were not rerun for this fork.

![Latent-space anomaly evaluation](images/prauc_lowres.png)

The [original README](UPSTREAM_README.md) preserves the paper citation, links to further explanations, and additional figures.

## Source and license

Based on and adapted from [tvhahn/ml-tool-wear](https://github.com/tvhahn/ml-tool-wear), by Tim von Hahn and Chris K. Mechefske. The original code, paper, documentation, and [MIT license](LICENSE) are retained.