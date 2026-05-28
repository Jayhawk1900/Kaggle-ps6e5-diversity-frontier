# The Diversity–Strength Frontier — PS6E5 Post-Mortem

A technical writeup of my [Kaggle Playground Series S6E5](https://www.kaggle.com/competitions/playground-series-s6e5) competition entry (F1 pit-stop prediction, top-15% finish at 0.95390 ROC-AUC).

**[Read the writeup →](https://YOUR-USERNAME.github.io/ps6e5-diversity-frontier/)**

## What's here

- `index.html` — the full standalone writeup (also available as a [hosted page](https://YOUR-USERNAME.github.io/ps6e5-diversity-frontier/))
- `PS6E5_diversity_strength_capstone.pdf` — print/share-friendly version
- `PS6E5_diversity_strength.ipynb` — Kaggle community notebook version

## The finding

Across nine model families on this dataset — three gradient-boosted trees, two from-scratch PyTorch neural networks (RealMLP, FT-Transformer), the TabPFN-2.5 foundation model, plus instance-based and linear baselines — every model is either **strong-but-correlated** with the existing pool, or **diverse-but-weak**. There is no point in the strong-and-diverse quadrant, because the signal is unimodal: every capable model converges on the same predictive structure.

The investigation maps this tradeoff with full pairwise correlations, blend-weight assignments, and a from-scratch implementation of each neural architecture.

## Also published

A [companion notebook](https://www.kaggle.com/code/YOUR-KAGGLE-USERNAME/the-diversity-strength-frontier-an-honest-ps6e5-po) is published on Kaggle.
