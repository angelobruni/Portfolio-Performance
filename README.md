# Portfolio Construction via Black-Litterman Model
 
## Overview
 
Implementation of the Black-Litterman asset allocation framework, translating macro views from a monthly Market Insight letter into a quantitative portfolio. Built as a bridge between qualitative macro analysis and systematic portfolio construction.
 
## Methodology
 
- **Prior**: Market equilibrium returns derived from AUM-based weights via reverse CAPM optimisation
- **Views**: 4 active macro views extracted from the March 2026 Market Insight letter
- **Blending**: Bayesian posterior (tau = 0.075) combining prior and views
- **Optimisation**: Max Sharpe with long-only constraints — 25% cap for core assets, 15% cap for satellite/niche assets
## Views Implemented
 
| View | Expected Return Differential |
|------|-------------------------------|
| India > Japan | +3% p.a. |
| Healthcare > MSCI World Quality | +2% p.a. |
| Euro IG Bonds > US Treasuries | +1.5% p.a. |
| Infrastructure (absolute) | +8% p.a. |
 
## Asset Universe
 
10 ETFs across equities, fixed income and real assets — covering MSCI World Quality, Healthcare, Robotics & Automation, Infrastructure, India, Japan, Euro IG Bonds, US Treasuries, Gold and Energy.
 
| Asset | Ticker | Category |
|-------|--------|----------|
| MSCI World Quality | IWQU.L | Core Equity |
| Healthcare | XLV | Satellite Equity |
| Robotics & Automation | IRBO | Satellite Equity |
| Infrastructure | IGF | Real Assets |
| India | NDIA.L | Emerging Markets |
| Japan | EWJ | Developed Markets |
| Euro IG Bonds | IEAC.L | Core Fixed Income |
| US Treasuries 7-10Y | IEF | Core Fixed Income |
| Gold | GLD | Commodities |
| Energy | XLE | Commodities |
 
## Output
 
- Correlation heatmap across all assets
- BL return adjustments vs market equilibrium (visualising view impact)
- Efficient frontier comparison: Black-Litterman vs historical Markowitz
- Portfolio allocation comparison (Max Sharpe / Min Variance / Equal Weight)
- Value-at-Risk (VaR) and Expected Shortfall (CVaR) at 95% and 99%
- Sensitivity analysis on tau parameter
## Why Black-Litterman over Markowitz?
 
| Issue with Markowitz | Black-Litterman Solution |
|---|---|
| Extreme concentration in few assets | Starts from diversified market equilibrium |
| Sensitive to historical return estimates | Blends estimates with market-implied returns |
| No room for manager views | Explicitly incorporates forward-looking views |
| Unstable weights across periods | More stable, intuitive allocations |
 
## Requirements
 
```
pip install yfinance scipy matplotlib seaborn pandas numpy
```
 
## Related
 
- Monthly Market Insight letter: https://medium.com/@angelobruni60
- LinkedIn: https://www.linkedin.com/in/angelobruni
 
