# Spectral Signatures of Sector Bubbles: AI Era vs Dot-Com

A correlation structure analysis comparing the current AI sector with the dot-com bubble (1997–2002), using spectral decomposition of rolling correlation matrices on Fama-French 49 industry portfolios.

## Summary

I test whether the AI era reproduces the spectral signatures observed during the dot-com bubble — eigenvalue spikes, tech-vs-rest eigenvector splits, and rising herding gaps. It doesn't.

📄 [Read the full article](https://aymaneelam.dev/blog/spectral-signatures-ai-vs-dot-com)  
📓 [View the notebook](spectral_signatures.ipynb)

## Methodology

- Rolling 60-day correlation matrices on 49 industry portfolios
- Eigenvalue decomposition (`scipy.linalg.eigh`)
- Three diagnostics: λ₁ market mode, λ₂ decoupling, herding gap
- Window sensitivity validation (30, 45, 60, 90, 120 days)

## Key Finding

The dot-com bubble showed a clear spectral signature — tech herding gap rising from 0.15 to 0.45, with a clean tech-vs-rest eigenvector split. The AI era (2023–2026) shows none of this. The herding gap is flat, and λ₂ reflects macro rotation, not tech decoupling.

## Requirements
- numpy
- pandas
- matplotlib
- scipy
- pandas-datareader
- yfinance

## Run

Open in [Google Colab](https://colab.research.google.com/) or run locally:

```bash
pip install numpy pandas matplotlib scipy pandas-datareader yfinance
jupyter notebook spectral_signatures.ipynb
```

## References

1. Buccheri, Marmi & Mantegna (2013). *Physical Review E*, 88, 012806
2. Fama & French (1997). *Journal of Financial Economics*, 43(2), 153–193
3. Laloux et al. (1999). *Physical Review Letters*, 83, 1467–1470

## Author

**Aymane El Amrani** — [aymaneelam.dev](https://aymaneelam.dev)
