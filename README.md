# Syntonic Portfolio — Financial Walk-Forward Validation

**The Syntony Principle applied to adaptive portfolio management.**

Jean-Pierre Bronsard · SyntonicAI Recherche · Montréal  
ORCID: [0009-0008-6639-7553](https://orcid.org/0009-0008-6639-7553)

---

## Version 2.0 (March 2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19021835.svg)](https://doi.org/10.5281/zenodo.19021835)

**Multi-asset, multi-norm, multi-decade out-of-sample evidence.**

This version extends and strengthens V1.0 (17 folds, t = 3.15) with 42× more folds, real daily market data, dual-norm validation (L² + C41), naive benchmarks with paired t-tests, and honest identification of which geometric components generate alpha in financial markets.

### Four Principal Results

**Result 1: Two Syntonic components generate highly significant alpha.**  
Vol scaling (UTAE Axiom U2) and coherence-gated momentum direction achieve t\_NW > 17 (p < 0.001) with κ = 1.0 untuned, across all configurations, both norms, and seven major crises from 1973 to 2022.

**Result 2: τ\* ≈ 1/√2 for the tested financial assets.**  
Under both L² and C41 norms, τ\* ≈ 0.71 days for stocks, bonds, gold, and Bitcoin. This provides a continuous, quantitative empirical indicator of proximity to the IID/random-walk limit under the tested estimators.

**Result 3: C41 detects fat tails but the IID signature persists.**  
The tail ratio ρ ≈ 1.32 > √(π/2) = 1.253 yields C41 weight w ≈ 0.40, correctly shifting toward L¹. Yet τ\*\_L1 ≈ τ\*\_L2 ≈ 0.71, providing strong evidence that the degeneracy reflects the IID structure of financial returns rather than a norm artifact. C41 nonetheless improves coherence estimation (paired t = −2.76 on 709 folds).

**Result 4: The naive benchmark is operationally equivalent.**  
Vol targeting + trend following, developed empirically over decades, is operationally equivalent to the Syntonic geometry under the present empirical design. The naive daily benchmark reproduces the Enhanced strategy identically (paired t = 0.00), because round(τ\*) = round(0.71) = 1 day.

### Key Metrics (Config A: Stocks+Bonds, 709 folds, 59 years)

| Metric | Value |
|---|---|
| C41 Enhanced mean α | +1.31%/month |
| t-statistic (Newey-West) | 17.40 (p < 0.001) |
| Win rate | 76.6% |
| Conservative (no momentum) | t = −1.72 (n.s.) |
| Sub-period: first half | t = 10.09 (p < 0.001) |
| Sub-period: second half | t = 14.77 (p < 0.001) |
| Bootstrap 95% CI | [+1.16%, +1.46%] |
| Crisis: Dot-Com Bust | α = +55.3% |
| Crisis: 2008 GFC | α = +30.6% |
| Crisis: COVID-19 | α = +11.5% |
| κ | 1.0 (Theory 5, not tuned) |

---

## Files

| File | Description |
|---|---|
| `Syntony_Financial_WalkForward_Definitive.ipynb` | Companion Colab notebook — reproduces all results |
| `Syntony_Financial_WalkForward_Validation_V2.pdf` | Publication PDF (14 pages, 5 figures) |
| `Syntony_Financial_WalkForward_Validation_V2.tex` | LaTeX source |
| `figures/` | Figures used in the PDF |

---

## Related Work

| Document | DOI |
|---|---|
| The Syntony Principle V4.1 — Canonical Edition | [10.5281/zenodo.17254395](https://doi.org/10.5281/zenodo.17254395) |
| Conjecture 41: Optimal Norm Selection | [10.5281/zenodo.18911127](https://doi.org/10.5281/zenodo.18911127) |
| Deep Learning Validation V3.0 | [10.5281/zenodo.18527033](https://doi.org/10.5281/zenodo.18527033) |
| Financial Validation V2.0 (this work) | [10.5281/zenodo.19021835](https://doi.org/10.5281/zenodo.19021835) |
| Financial Validation V1.0 | [10.5281/zenodo.18642833](https://doi.org/10.5281/zenodo.18642833) |

---

## Version History

### V2.0 (March 2026)
- 709 folds spanning 59 years (vs. 17 folds, 17 months)
- Real daily prices from Yahoo Finance (vs. biweekly interpolation)
- Dual L² + C41 adaptive norm (vs. L² only)
- Naive daily/weekly/monthly benchmarks with paired t-tests
- 7 major crises tested (1973 Oil Crisis through 2022 Rate Shock)
- TX costs proportional to turnover (vs. flat per rebalance)
- Mechanism isolation: precise identification of active geometric components
- τ\* degeneracy diagnosed and explained (IID random-walk limit)

### V1.0 (February 2026)
- 17 monthly folds (Sep 2024 -- Jan 2026)
- 3 assets (SPY, BTC-USD, GLD), interpolated anchor prices
- t = 3.15 (p < 0.01), 88% win rate
- Initial mechanism isolation (conservative fails)

---

## License

- Documentation: CC BY 4.0
- Code: MIT

**Disclaimer:** Research and educational tool. NOT investment advice. Past performance does not guarantee future results.
