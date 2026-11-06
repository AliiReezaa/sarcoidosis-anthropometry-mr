<p align="center"><img src="assets/header.svg" width="100%" alt="Body shape and sarcoidosis"></p>

<p align="center">![Co-author](https://img.shields.io/badge/Co--author-0f6e6a?style=flat-square) ![Robust MR](https://img.shields.io/badge/Robust%20MR-5b4bb7?style=flat-square) ![R](https://img.shields.io/badge/R-276DC3?style=flat-square) ![Stata](https://img.shields.io/badge/Stata-1a5f91?style=flat-square)</p>

> **Status:** manuscript in preparation
>
> This repository is a public overview of an unpublished study. It shows the research question, design and methods. **Results, data and analysis code are withheld until peer-reviewed publication**, and will be released here at that point.

## Research question
Which measures of body size and fat distribution (body-fat %, BMI, hip and waist circumference) **causally** influence sarcoidosis risk?

## Study design
```mermaid
flowchart LR
  E1[Body-fat %<br/>3 GWAS] --> O[Sarcoidosis]
  E2[BMI<br/>3 GWAS] --> O
  E3[Hip circumference<br/>3 GWAS] --> O
  E4[Waist circumference<br/>3 GWAS] --> O
  O --> S[25+ estimators<br/>& sensitivity suite]
  style E3 fill:#fbe9e1,stroke:#c2552b
```

## Data sources
| Role | Dataset | Notes |
|---|---|---|
| Exposures | 12 anthropometric GWAS (IEU OpenGWAS) | 3 independent sources per trait |
| Outcome | Sarcoidosis GWAS (GWAS Catalog) | European ancestry |

## Methods
| Component | Approach |
|---|---|
| Primary | IVW random effects |
| Robust estimators | MR-RAPS, MR-Lasso, cML, contamination mixture, dIVW, and more |
| Diagnostics | Cochran Q, I², I²GX, MR-PRESSO, radial MR, Cook's distance, Steiger, leave-one-out |

## Why it matters
Obesity is a suspected risk factor for sarcoidosis. Separating overall adiposity from fat distribution points to more specific biology.

## Team & role
Co-author **A. R. Soleymani Taloubaghi** (analysis) with D. Habibi (corresponding) and colleagues.

## Reproducibility
- Analysis pipeline written in R 4.4 and Stata (mrrobust), with pinned package versions and a single entry-point script
- Public summary statistics only; no individual-level data is used or shared
- Reported according to STROBE-MR

---
<sub>Contact: <a href="mailto:alirezasoleymani24@gmail.com">alirezasoleymani24@gmail.com</a> · <a href="https://aliireezaa.github.io">aliireezaa.github.io</a></sub>
