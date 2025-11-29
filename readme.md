# PulmoProbe AI

## Overview

PulmoProbe AI is a large-scale machine learning initiative engineered to detect and classify lung diseases and predict survival outcomes using structured clinical datasets and synthetic medical features. Designed as a scalable and deployable AI solution, it integrates advanced preprocessing, Exploratory Data Analysis (EDA), feature engineering, and chunked training methodologies to handle massive datasets efficiently.

This project demonstrates how high‑volume data can be leveraged for healthcare analytics while maintaining memory efficiency, high predictive performance, and production‑ready architecture.

---

## Project Objectives

* Build scalable machine learning models to support lung disease diagnosis and survival prediction.
* Analyze and preprocess high‑dimensional medical datasets for clinical insights.
* Implement chunked training to manage model learning across 20M+ rows without memory failures.
* Optimize predictive performance using advanced techniques such as HistGradientBoosting and XGBoost.
* Provide deployable model artifacts with strong inference capability.

---

## Dataset Overview

### PulmoProbe Medical Dataset

* **Rows:** 20,000,000
* **Features:** Demographic, clinical, lifestyle, biomarker, environmental, and treatment‑related variables.
* **Target Column:** `Survived` (1 = survived, 0 = not survived)

### Key Classes

* Gender, Country, Cancer Stage, Smoking Status, Treatment Type
* Tumor size, metastasis sites, treatment cycles and duration
* Biomarkers including LDH, CEA
* BMI ranges & pack‑year history

---

## EDA Summary

* Comprehensive analysis of numeric and categorical features
* Missing value profiling and automated cleanup
* Distribution plots, correlation heatmaps, and survival analysis trends
* Top medical and lifestyle factors influencing outcomes
* Exported EDA summaries and visual reports for documentation

---

## Modeling Approach

### Algorithms Trained

| Model                     | Training Strategy                       | Scalability | Key Metrics Performance |
| ------------------------- | --------------------------------------- | ----------- | ----------------------- |
| Logistic Regression (SGD) | Incremental partial_fit                 | High        | ROC‑AUC ~0.75           |
| HistGradientBoosting      | Chunk‑wise incremental                  | High        | Best performance ~0.763 |
| XGBoost (Fine‑Tuned)      | Randomized optimization + full training | High        | ROC‑AUC ~0.752          |

### Evaluation Metrics

* Accuracy
* ROC‑AUC
* F1‑Score

Metrics and reports exported as CSV for formal model comparison.

---

## Key Deliverables

* Full EDA outputs and dataset summaries
* Enriched dataset with 24+ engineered medical features
* Trained model artifacts: `logistic_sgd.pkl`, `hgb_model.pkl`, `xgb_final_model.pkl`
* Feature importance visualizations and performance reports

---

## Deployment Opportunities

* Clinical decision support workflows
* Integration with EMR / PACS systems
* Real‑time inference pipelines
* Imaging + structured data fusion for hybrid AI diagnosis

---

## Future Roadmap

* Integrate CNN‑based medical image analysis
* Real patient validation for clinical benchmarking
* Federated learning for privacy‑preserving training
* Explainable AI via SHAP‑based interpretability

---

## Conclusion

PulmoProbe AI establishes a high‑performance, scalable foundation for lung disease prediction using large‑scale synthetic medical datasets. The project demonstrates excellence in data engineering, modeling, and healthcare AI readiness, with real‑world deployment potential for predictive diagnostics and personalized treatment planning.

---

## Repository Structure

```
pulmo-probe-ai
│
├── data/
├── eda_outputs/
├── models/
├── plots/
├── scripts/
└── README.md
```

---

## Author

**Costas Pinto**
Machine Learning & Healthcare AI Research

---

## License

MIT License — Free to use with attribution.
