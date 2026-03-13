# Predicting Human Decision-Making in Autonomous Vehicle Moral Dilemmas

> Advanced Machine Learning (AML) 수업 팀 프로젝트 | Team 12  
> Aileen Li · Alex Edwards · Carol Le · **Aubrey Oh** · Radha Pawar

---

## 🚗 Overview

Imagine a self-driving car forced to choose: stay on course and hit a jaywalker, or swerve and hit two pedestrians on the sidewalk. There is no safe option — only a choice about *who* is put at risk.

Using outcome-level data from MIT's **Moral Machine experiment** (40M+ responses from 200+ countries), we trained machine learning models to predict which outcomes humans are most likely to choose in AV moral dilemmas — and used SHAP to interpret the patterns behind those decisions.

---

## 🎯 Key Results

| Model | Accuracy | Precision | Recall | ROC-AUC |
|-------|----------|-----------|--------|---------|
| **CatBoost** | **0.711** | **0.712** | **0.720** | **0.776** ✅ |
| XGBoost | 0.709 | 0.711 | 0.715 | 0.773 |
| Random Forest | 0.676 | 0.676 | 0.690 | 0.724 |
| Logistic Regression | 0.649 | 0.658 | 0.639 | 0.709 |

**CatBoost** achieved the best performance, handling categorical variables and missing values natively with minimal preprocessing.

---

## 🔍 What We Found

**Consistent moral patterns across countries:**
- People prefer saving **larger groups** (utilitarian preference)
- Strong prioritization of **children and younger individuals** over elderly
- **Humans over animals** — consistently across cultures
- **Legal crossers** saved at much higher rates than jaywalkers
- Higher saved rates for high-status groups (doctors, executives, athletes)
- Lower saved rates for stigmatized groups (criminals, homeless)

**Model performance was stable across countries** — despite cultural differences, global moral patterns are surprisingly consistent. However, **Social Status and Gender scenarios** were notably harder to predict, suggesting more context-dependent reasoning.

---

## 🧩 Approach

### 1. Predictive Modeling
Binary classification: `Saved = 1` if the outcome was chosen, `Saved = 0` otherwise.
Models compared: Logistic Regression, Random Forest, XGBoost, CatBoost.

### 2. Segmentation & Cross-Sectional Analysis
- **Supervised:** performance by country (`UserCountry3`) and scenario type (`ScenarioTypeStrict`)
- **Unsupervised:** K-Means clustering (k=8) on structural + character features → "moral personas"

### 3. Interpretability
SHAP values reveal which features most influence predictions:
- `NumberOfCharacters`, `CrossingSignal`, character type (Girl, Boy, Criminal, Homeless, etc.)

---

## 📊 K-Means Moral Personas (k=8)

K-Means clustering on scenario features revealed 8 distinct outcome profiles — latent "moral personas" that humans save at different rates:

| Cluster | Saved Rate | Profile |
|---------|-----------|---------|
| 2 | 0.666 | Children & families |
| 0 | 0.634 | Mixed adult groups |
| 4 | 0.586 | Professionals (doctors, executives) |
| 7 | 0.537 | Athletes |
| 5 | 0.481 | General adult scenarios |
| 3 | 0.473 | Elderly groups |
| 1 | 0.325 | Animals (dogs, cats) |
| 6 | 0.224 | Stigmatized groups (homeless, criminals) |

---

## 🛠 Tech Stack

```
Python
├── CatBoost         — best-performing classifier
├── XGBoost          — gradient boosting baseline
├── scikit-learn     — Random Forest, Logistic Regression, K-Means, preprocessing
├── SHAP             — model interpretability
├── Pandas / NumPy   — data processing
└── Matplotlib       — visualization
```

---

## 📁 Repository Structure

```
├── PredictiveModels_EthicalDilemma   # Supervised learning models (CatBoost, XGBoost, RF, LR)
├── K-Means_Segmentation              # Unsupervised clustering & moral personas
├── EDA_Visuals.ipynb                 # Exploratory data analysis
├── Team12_Project.pptx               # Final presentation slides
└── README.md
```

---

## 📖 Data

**Source:** MIT Moral Machine experiment (Awad et al., 2018)  
**Dataset:** `SharedResponse.csv` — ~40M rows; we used a random 100,000-row subset  
**Access:** [Open Science Framework](https://osf.io/3hvt2/)

---

## 📚 References

- Awad et al. (2018). The Moral Machine experiment. *Nature*, 563, 59–64.
- Bonnefon et al. (2016). The social dilemma of autonomous vehicles. *Science*, 352(6293).
- Lundberg & Lee (2017). A unified approach to interpreting model predictions. *NeurIPS*.
- Prokhorenkova et al. (2018). CatBoost: Unbiased boosting with categorical features. *NeurIPS*.

---

*Advanced Machine Learning | University of Texas at Austin · 2025*
