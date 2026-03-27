# Enterprise Risk Management Analytics: Microsoft Cybersecurity Acquisition

## Project Overview

This project presents a comprehensive enterprise risk management (ERM) analytics assessment for Microsoft Corporation's proposed acquisition of a mid-sized cybersecurity-as-a-service (CaaS) platform company. The analysis integrates qualitative and quantitative risk assessment methodologies to evaluate three competitive risks and deliver actionable insights for executive decision-makers.

**Course:** ALY 6130 – Risk Management for Analytics, Northeastern University  
**Authors:** Honglin Wang, Chuanli Yang, Raymond Twumasi Opoku  
**Date:** March 2026

---

## Risk Areas Assessed

| # | Risk Area | Type | I&W Warning | MC P(High) |
|---|-----------|------|-------------|------------|
| 1 | Loss of Cybersecurity Market Share to Specialized Competitors | Negative | YELLOW (3.40) | 98.4% |
| 2 | Critical Data Breach During Platform Integration | Negative | RED (4.00) | 100% |
| 3 | Accelerated Enterprise Customer Acquisition via Bundled Offerings | Positive | GREEN (2.40) | 86.5% |

## Methodologies

- **SWOT Analysis** with ERM focus (Hopkin, 2018)
- **Scenario Analytics** — best/likely/worst case modeling (Fleisher & Bensoussan, 2015, Ch. 22)
- **Industry Fusion Analytics** — convergence force assessment (Fleisher & Bensoussan, 2015, Ch. 17)
- **Indicators & Warning (I&W) Analysis** — composite scoring with threshold-based warnings (Grabo et al., 2004)
- **Monte Carlo Simulation** — 10,000 iterations per risk area with VaR at 95th percentile (Vose, 2008)
- **Random Forest ML Classification** — severity validation with Monte Carlo-enhanced features (Breiman, 2001)
- **Sensitivity Analysis** — tornado charts identifying highest-influence indicators
- **Key Risk Indicators (KRIs)** — leading indicators with Green/Amber/Red thresholds (COSO, 2017)

---

## Repository Structure

```
enterprise-risk-project/
│
├── README.md
├── requirements.txt
│
├── data/
│   ├── raw/
│   │   └── risk_register.xlsx              # Original 40-item risk register
│   └── processed/
│       └── risk_register_updated.xlsx      # Updated with MC/I&W annotations
│
├── notebooks/
│   ├── eda.ipynb                           # Exploratory data analysis
│   ├── qualitative_analysis.ipynb          # Scenario & Industry Fusion Analytics
│   ├── quantitative_analysis.ipynb         # I&W scoring, ML classification, sensitivity
│   └── monte_carlo.ipynb                   # Monte Carlo simulation (10,000 iterations)
│
└── report/
    └── final_report.pdf                    # Signature Assessment (7+ pages, APA format)
```

## Setup and Installation

```bash
# Clone the repository
git clone https://github.com/<username>/enterprise-risk-project.git
cd enterprise-risk-project

# Install dependencies
pip install -r requirements.txt

# Run notebooks in order
# 1. eda.ipynb
# 2. qualitative_analysis.ipynb
# 3. quantitative_analysis.ipynb
# 4. monte_carlo.ipynb
```

## Key Results

### Quantitative Risk Summary

| Risk Area | Avg Score | MC Mean | MC VaR (95%) | P(High) | I&W | Warning |
|-----------|-----------|---------|--------------|---------|-----|---------|
| Market Share Loss | 66.5 | 65.2 | 86.5 | 98.4% | 3.40 | YELLOW |
| Data Breach (Integration) | 75.8 | 74.6 | 95.3 | 100% | 4.00 | RED |
| Enterprise Acq. (Bundled) | 57.2 | 55.4 | 79.0 | 86.5% | 2.40 | GREEN |

### ML Validation
- **Model:** Random Forest (50 estimators, max depth 3, balanced class weights)
- **Accuracy:** 88% (stratified 3-fold cross-validation)
- **Weighted F1-Score:** 0.89
- **Top features:** Likelihood Score (0.36), Impact Score (0.30), MC Std (0.15)

## References

- Breiman, L. (2001). Random forests. *Machine Learning, 45*(1), 5–32.
- Bromiley, P., McShane, M., Nair, A., & Rustambekov, E. (2015). Enterprise risk management: Review, critique, and research directions. *Long Range Planning, 48*(4), 265–276.
- COSO. (2017). *Enterprise risk management—Integrating with strategy and performance.*
- Fleisher, C. S., & Bensoussan, B. E. (2015). *Business and competitive analysis* (2nd ed.). FT Press.
- Fraser, J. R. S., & Simkins, B. J. (2016). The challenges of and solutions for implementing ERM. *Business Horizons, 59*(6), 689–698.
- Grabo, C. M., Goldman, J., & Wasik, J. M. (2004). *Anticipating surprise: Analysis for strategic warning.* CSIR.
- Hopkin, P. (2018). *Fundamentals of risk management* (5th ed.). Kogan Page.
- Vose, D. (2008). *Risk analysis: A quantitative guide* (3rd ed.). Wiley.
