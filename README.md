# AV Moral Dilemma Prediction and Segmentation

## Project Overview
This project analyzes large-scale moral decision data to build predictive and segmentation-based analytics that explain how people respond to autonomous vehicle (AV) dilemma scenarios. The goal was to move beyond descriptive statistics and develop an interpretable analytics workflow that could support structured decision-making, behavioral insight generation, and stakeholder-facing communication.

This project is especially relevant to analytics consulting work because it combines applied modeling, clustering, feature interpretation, and business-style explanation in a single end-to-end workflow.

---

## Business / Analytical Objective
The project was designed around three core questions:

1. **Prediction:** Can we accurately predict respondent choices in AV moral dilemma scenarios using demographic and scenario-related features?
2. **Segmentation:** Are there distinct groups of respondents with different ethical decision patterns?
3. **Interpretation:** Which variables matter most, and how can the model outputs be translated into clear, decision-ready insights?

Rather than treating the problem as a purely academic exercise, the analysis was structured as a practical modeling prototype focused on classification performance, segmentation logic, and explainability.

---

## My Role
I developed the analytical workflow end to end, including:

- cleaning and structuring the dataset for modeling
- engineering features for classification and segmentation
- training and comparing multiple machine learning models
- evaluating model performance using appropriate classification metrics
- performing clustering analysis to identify respondent segments
- interpreting feature importance and model behavior using explainability methods
- packaging the results into a clear, presentation-ready analytics narrative

---

## Data Scope
The project used a large-scale response dataset containing over **40 million records** from moral dilemma scenarios involving autonomous vehicles.

The data included respondent- and scenario-level variables that could be used to:
- predict decision outcomes
- compare model performance across algorithms
- identify behavioral segments through clustering
- examine feature importance and decision drivers

---

## Methods and Tools
### Programming and Analytics Stack
- **Python**
- **Pandas / NumPy**
- **scikit-learn**
- **CatBoost / XGBoost / Random Forest / Logistic Regression**
- **K-means clustering**
- **SHAP for model interpretation**
- **Matplotlib / visualization tools**

### Modeling Workflow
The project was structured as a reproducible analytics pipeline:

1. **Data preparation**
   - cleaned and transformed raw records
   - selected modeling variables
   - prepared data for classification and clustering

2. **Predictive modeling**
   - built and compared multiple classification models
   - evaluated performance using ROC-AUC and related metrics
   - identified the strongest-performing model for prediction

3. **Segmentation analysis**
   - used clustering to identify groups with different response patterns
   - profiled segments to support higher-level interpretation

4. **Explainability**
   - used SHAP and model-based interpretation to identify the most influential variables
   - translated technical results into human-readable insights

---

## Key Outputs
This project produced four decision-ready outputs:

- **a predictive classification workflow** for AV dilemma outcomes
- **a comparative model evaluation framework** across multiple algorithms
- **a respondent segmentation analysis** using clustering
- **an explainability layer** showing the variables driving model predictions

The strongest-performing model in the project was **CatBoost**, which delivered the best classification performance among the models tested.

---

## Why This Project Matters
This project is relevant to consulting-style analytics roles because it shows the ability to:

- build and compare applied machine learning models, not just one-off analyses
- combine **prediction + segmentation + interpretation** in a single workflow
- handle large-scale structured data in a disciplined way
- translate technically complex outputs into stakeholder-friendly insights
- prototype an analytics solution that can support broader business or policy discussions

It also demonstrates several capabilities that align well with fast-paced analytics teams:
- **applied modeling** rather than purely theoretical work
- **evaluation discipline** through model comparison and performance metrics
- **segmentation analysis** for behavioral insight generation
- **explainability** to improve trust and usability of results

---

## Relevance to Analytics Consulting
This project reflects the kind of work often needed in analytics consulting and prototyping environments:

- rapidly structuring a large dataset into an analysis-ready form
- comparing multiple methods to identify practical model choices
- building interpretable outputs rather than black-box-only solutions
- creating insights that can inform critical decisions, not just model scores

In the context of consulting-style analytics, this project highlights strong capability in:
- **Python-based modeling**
- **classification and tree-based methods**
- **segmentation / clustering**
- **explainability and stakeholder communication**
- **packaging technical work into business-facing outputs**

---

## Repository Contents
Typical contents of this repository include:

- notebooks or scripts for data preparation
- model training and evaluation workflows
- clustering / segmentation analysis
- interpretation outputs and visualizations
- supporting documentation for methods and findings

---

## Summary
This repository showcases an end-to-end analytics project that combines predictive modeling, segmentation, and explainability using a large real-world dataset. It demonstrates the ability to build practical machine learning workflows, evaluate them rigorously, and communicate the results in a way that supports meaningful decision-making.
