# Portfolio Construction via Black-Litterman Model

## Overview
Implementation of the Black-Litterman asset allocation framework, translating macro views from a monthly Market Insight Letter into a quantitative portfolio. Built as a bridge between qualitative macro analysis and systemic portfolio construction. 

## Methodology
- **Prior**: Market equilibrium returns derived from AUM-based weights via reverse CAPM optimizaption
- **Views**_ 4 active macro views extracted from the March 2026 Market Insight Letter
- **Blending**: Bayesian posterior (tau = 0.075) combining prior and views
- **Optimization**: Max Sharpe with long-only and 25% per-high-quality asset constraints and 15% per-niche-quality asset

- ## Views Implemented
- | View | Expected Return Differential |
- |------|--------------------------------|
- | India > Japan | +3% p.a. |
- | Healthcare > MSCI World Quality | +2% p.a. |
- | Euro IG Bonds > US Treasuries | +1.5% p.a. |
- | Infrastructure (absolute) | +8% p.a. |

- ## Asset Universe
- 10 ETFs across equities, fixed income and real assets - covering MSCI World Quality, Healthcare, Robotics, Infrastructure, India, Japan, Euro IG Bonds, US Treasuries, Gold and Energy.

- ## Output
- - Correlation heatmap
  - BL return adjustments vs market equilibrium
  - Efficient fronties (BL vs historical Markowitz)
  - Portfolio allocation comparison (Max Sharpe / Min Variance / Equal Weight)
  - VaR and CVaR at 95% and 99%
  - Sensitiity analysis on tau parameter
 
  - ## Requirement
  - pip install yfinance scipy matplotlib seaborn pandas numpy
 
  - ## Related
  - Monthly Market Insight letter: https://medium.com/@angelobruni60
  - LinkedIn: https://www.linkedin.com/in/angelobruni
