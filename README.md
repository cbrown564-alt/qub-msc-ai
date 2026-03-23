# MSc Artificial Intelligence — Queen's University Belfast

My actual notebooks from the programme. The thinking is visible. The dead ends are in there too.

---

## Semester 1

### Foundations of AI · ECS8050

| # | Assignment | Topic |
|---|---|---|
| 1 | [Violent Crime Regression](semester-1/foundations-of-ai/cw1-violent-crime-regression/) | Predicting US violent crime rates from 128 socioeconomic features — PCA/SVD for dimensionality reduction, linear regression. Key finding: reducing dimensions *hurt* performance; raw features won. |
| 2 | [Violent Crime Extended](semester-1/foundations-of-ai/cw2-violent-crime-extended/) | Same dataset, deeper analysis — Ridge regression implemented from scratch with gradient descent, hyperparameter optimisation, residual analysis. Ridge beat SVD; regularisation handles noise better than dimension reduction. |

### Machine Learning · ECS8051

| # | Assignment | Topic |
|---|---|---|
| 1 | [ETF Return Prediction](semester-1/machine-learning/cw1-etf-return-prediction/) | Predicting next-H-day log returns for 6 sector ETFs (XLE, XLF, XLK…) — feature engineering across volume, volatility, trend and momentum indicators; Ridge/ElasticNet/RF/XGBoost/LightGBM compared via walk-forward validation. LightGBM won: +11pp directional accuracy over baseline, 34s vs 1152s for XGBoost. |
| 2 | [Market Regime Detection](semester-1/machine-learning/cw2-market-regime-detection/) | Unsupervised regime identification on 1999–2025 ETF data using Gaussian Mixture Models — features include rolling volatility and an eigenvalue-based market synchronisation metric. BIC/silhouette scoring selected 3 regimes (Stable / Correction / Panic), correctly identifying 2000, 2008, and 2020 crashes. Regimes fed into the CW1 LightGBM pipeline as one-hot features. |

### Knowledge Engineering · ECS8052

| # | Assignment | Topic |
|---|---|---|
| 1 | [Oregano Knowledge Graph](semester-1/knowledge-engineering/cw1-oregano-knowledge-graph/) | Analysing the OREGANO biomedical knowledge graph (compounds, proteins, genes, diseases, pathways) — graph statistics, PyVis visualisation, and full formalisation of 17 ontology predicates into first-order logic with domain/range constraints. |
| 2 | [Drug Repurposing via Bayesian Network](semester-1/knowledge-engineering/cw2-bayesian-network-drug-interactions/) | SPARQL metapath queries (Compound→Protein→Gene→Disease) over OREGANO to surface novel drug-disease hypotheses — identified Pardoprunox as a candidate for 4 unindicated conditions (Dystonia, Tremor, Schizophrenia, ADHD) via dopamine receptor pathways, validated against NCBI. Bayesian network modelled treatment efficacy with PyMC. |

---

## Semester 2

### Computer Vision · ECS8053

| # | Assignment | Topic |
|---|---|---|
| 1 | [TinyImageNet Classification](semester-2/computer-vision/cw1-tinyimagenet-classification/) | Image classification without deep learning on 64×64 images — SIFT (with parameter tuning for tiny images) vs ORB, Bag of Words vs Fisher Vectors, Linear SVM. SIFT + Fisher Vectors hit 52% accuracy on 15 classes; honest failure analysis on where hand-crafted features break down. |

### Natural Language Processing · ECS8054

| # | Assignment | Topic |
|---|---|---|
| 1 | [LLM Linguistic Structure](semester-2/natural-language-processing/cw1-llm-linguistic-structure/) | Analysing a corpus of 602 LLM-generated stories conditioned on structured templates (theme, setting, style, country) — Zipf's law, dependency parsing (spaCy/Stanza), phoneme richness, WordNet semantic similarity, and constituency tree analysis to quantify how template variables shape linguistic output. |

### AI for Health · ECS8055

| # | Assignment | Topic |
|---|---|---|
| 1 | [DNA Methylation Classification](semester-2/ai-for-health/cw1-dna-methylation-classification/) | End-to-end preprocessing of raw IDAT epigenomic data (Illumina 850K/450K arrays) for medulloblastoma subtype classification — NOOB background correction, dye bias correction, p-OOBAH masking, cross-platform probe integration, then PCA/t-SNE/UMAP for visualisation and KNN/MissForest imputation. Follows Sharma et al. (2019) protocol. |

---

*Dissertation topic TBD — choosing April 2026.*
