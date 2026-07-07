# MSc Artificial Intelligence — Queen's University Belfast

My actual notebooks from the programme. The thinking is visible. The dead ends are in there too.

Each assignment below has a **case study** — a short, results-first summary you can read without opening the notebook. Browse all 12 in one place: [case-studies.html](https://cbrown564-alt.github.io/qub-msc-ai/case-studies.html#fai-cw1).

---

## Semester 1

### Foundations of AI · ECS8050

| # | Assignment | Topic |
|---|---|---|
| 1 | [Violent Crime Regression](semester-1/foundations-of-ai/cw1-violent-crime-regression/) ([case study](semester-1/foundations-of-ai/cw1-violent-crime-regression/case-study.html)) | Predicting US violent crime rates from 128 socioeconomic features — PCA/SVD for dimensionality reduction, linear regression. Key finding: reducing dimensions *hurt* performance; raw features won. |
| 2 | [Violent Crime Extended](semester-1/foundations-of-ai/cw2-violent-crime-extended/) ([case study](semester-1/foundations-of-ai/cw2-violent-crime-extended/case-study.html)) | Same dataset, deeper analysis — Ridge regression implemented from scratch with gradient descent, hyperparameter optimisation, residual analysis. Ridge beat SVD; regularisation handles noise better than dimension reduction. |

### Machine Learning · ECS8051

| # | Assignment | Topic |
|---|---|---|
| 1 | [ETF Return Prediction](semester-1/machine-learning/cw1-etf-return-prediction/) ([case study](semester-1/machine-learning/cw1-etf-return-prediction/case-study.html)) | Predicting next-H-day log returns for 6 sector ETFs (XLE, XLF, XLK…) — feature engineering across volume, volatility, trend and momentum indicators; Ridge/ElasticNet/RF/XGBoost/LightGBM compared via walk-forward validation. LightGBM won: +11pp directional accuracy over baseline, 34s vs 1152s for XGBoost. |
| 2 | [Market Regime Detection](semester-1/machine-learning/cw2-market-regime-detection/) ([case study](semester-1/machine-learning/cw2-market-regime-detection/case-study.html)) | Unsupervised regime identification on 1999–2025 ETF data using Gaussian Mixture Models — features include rolling volatility and an eigenvalue-based market synchronisation metric. BIC/silhouette scoring selected 3 regimes (Stable / Correction / Panic), correctly identifying 2000, 2008, and 2020 crashes. Regimes fed into the CW1 LightGBM pipeline as one-hot features. |

### Knowledge Engineering · ECS8052

| # | Assignment | Topic |
|---|---|---|
| 1 | [Oregano Knowledge Graph](semester-1/knowledge-engineering/cw1-oregano-knowledge-graph/) ([case study](semester-1/knowledge-engineering/cw1-oregano-knowledge-graph/case-study.html)) | Analysing the OREGANO biomedical knowledge graph (compounds, proteins, genes, diseases, pathways) — graph statistics, PyVis visualisation, and full formalisation of 17 ontology predicates into first-order logic with domain/range constraints. |
| 2 | [Drug Repurposing via Bayesian Network](semester-1/knowledge-engineering/cw2-bayesian-network-drug-interactions/) ([case study](semester-1/knowledge-engineering/cw2-bayesian-network-drug-interactions/case-study.html)) | SPARQL metapath queries (Compound→Protein→Gene→Disease) over OREGANO to surface novel drug-disease hypotheses — identified Pardoprunox as a candidate for 4 unindicated conditions (Dystonia, Tremor, Schizophrenia, ADHD) via dopamine receptor pathways, validated against NCBI. Bayesian network modelled treatment efficacy with PyMC. |

---

## Semester 2

### Computer Vision · ECS8053

| # | Assignment | Topic |
|---|---|---|
| 1 | [TinyImageNet Classification](semester-2/computer-vision/cw1-tinyimagenet-classification/) ([case study](semester-2/computer-vision/cw1-tinyimagenet-classification/case-study.html)) | Image classification without deep learning on 64×64 images — SIFT (with parameter tuning for tiny images) vs ORB, Bag of Words vs Fisher Vectors, Linear SVM. SIFT + Fisher Vectors hit 52% accuracy on 15 classes; honest failure analysis on where hand-crafted features break down. |
| 2 | [Neural Networks for Image Classification](semester-2/computer-vision/cw2-neural-networks/) ([case study](semester-2/computer-vision/cw2-neural-networks/case-study.html)) | Revisiting the same 15-class TinyImageNet100 split with deep learning — fully-connected MLPs (shallow/deep/wide configs) vs VGG- and ResNet-inspired CNNs, all trained with Adam + ReduceLROnPlateau and early stopping. Compares architectures, learning-rate sensitivity, and a data augmentation ablation against the Assignment 1 SIFT + Fisher Vectors baseline. |

### Natural Language Processing · ECS8054

| # | Assignment | Topic |
|---|---|---|
| 1 | [LLM Linguistic Structure](semester-2/natural-language-processing/cw1-llm-linguistic-structure/) ([case study](semester-2/natural-language-processing/cw1-llm-linguistic-structure/case-study.html)) | Analysing a corpus of 602 LLM-generated stories across six writing styles (legalistic, journalistic, descriptive, children's, hard-boiled, stream-of-consciousness) — Zipf's law (a power law in every style, but never at the canonical exponent), dependency-distance/syntactic complexity, and lexical stylometry. A two-feature classifier recovers writing style at far above chance, showing the stylistic differences are systematic. |
| 2 | [Classification, Sentiment Analysis & Q&A with LLMs](semester-2/natural-language-processing/cw2-classification-sentiment-q+a-LLMs/) ([case study](semester-2/natural-language-processing/cw2-classification-sentiment-q+a-LLMs/case-study.html)) | Applying encoder transformers (BERT, ModernBERT, RoBERTa, DistilBERT) to the same story corpus — fine-tuned country/theme classification (BERT beat ModernBERT, 89% vs 86%, due to overfitting on the small dataset), zero-shot sentiment/emotion analysis, and extractive Q&A (base vs fine-tuned BERT-SQuAD2, with token-F1 evaluation and error analysis by answer length and writing style). |

### AI for Health · ECS8055

| # | Assignment | Topic |
|---|---|---|
| 1 | [DNA Methylation Classification](semester-2/ai-for-health/cw1-dna-methylation-classification/) ([case study](semester-2/ai-for-health/cw1-dna-methylation-classification/case-study.html)) | End-to-end preprocessing of raw IDAT epigenomic data (Illumina 850K/450K arrays) for medulloblastoma subtype classification — NOOB background correction, dye bias correction, p-OOBAH masking, cross-platform probe integration down to a shared feature space, then PCA/UMAP for visualisation and KNN/MICE imputation, factorised into 16 NMF metagenes. Follows Sharma et al. (2019) protocol. |
| 2 | [Medulloblastoma Subtype Classification](semester-2/ai-for-health/cw2-dna-methylation-classification/) ([case study](semester-2/ai-for-health/cw2-dna-methylation-classification/case-study.html)) | Classifying medulloblastoma into 8 molecular subtypes from 16 NMF-derived methylation features — SVC vs KNN, with class-weighted hyperparameter tuning across 5 iterations of cross-validated grid search. Beat the Abid & Rafiee (2024) macro-F1 benchmark on both HM450 (0.97 vs 0.94) and cross-platform EPIC (0.94 vs 0.93) test sets; bias-variance and misclassification analysis included. |
