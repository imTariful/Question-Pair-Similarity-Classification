# Question Pair Similarity Classification

This README documents the Jupyter notebook `Question_Pair_Similarity_Classification (1).ipynb` in this repository. The notebook performs experiments for classifying whether two questions are similar (duplicate / paraphrase detection), including data preparation, feature extraction, model training, evaluation, and example predictions.

**Repository**: `D:\assignments\assignment_1_Kalpit`
**Notebook**: `Question_Pair_Similarity_Classification (1).ipynb`

**Purpose**: Provide a clear, reproducible workflow for training and evaluating models that determine similarity between pairs of questions. The notebook is suitable for experimentation, quick prototyping, and demonstration.

**Contents**
- Overview: high-level goals and dataset description.
- Setup: required Python packages and environment steps.
- Data loading & preprocessing: cleaning, tokenization, and pair formatting.
- Feature engineering: TF-IDF, embeddings, or other similarity metrics.
- Modeling: baseline classifiers (Logistic Regression, SVM) and optionally simple neural models.
- Evaluation: accuracy, precision, recall, F1, ROC/AUC, confusion matrix, sample predictions.
- Notes & next steps: tips for improvement and reproducibility.

**Requirements**
- Python 3.8+ (3.11 recommended).
- The repository's `requirements.txt` (if present) contains dependencies. To install:

```powershell
py -3 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

If you prefer, install the minimal packages used by the notebook (example):

```powershell
python -m pip install jupyter pandas scikit-learn numpy matplotlib seaborn
```

**How to open and run**
- Launch Jupyter from the project root and open the notebook:

```powershell
jupyter notebook "Question_Pair_Similarity_Classification (1).ipynb"
```

- Or run Jupyter Lab if installed:

```powershell
jupyter lab
```

- In the notebook UI: run cells sequentially (Kernel → Restart & Run All) to reproduce the analysis.

**Notebook structure (high level)**
- Section 1 — Imports & configuration: imports, random seeds, display settings.
- Section 2 — Data load: reading `csv`/`tsv`/other sources or inline sample pairs.
- Section 3 — Preprocessing: lowercase, strip, remove punctuation, optional stopwords.
- Section 4 — Feature extraction: TF-IDF vectorizer, count vectors, or precomputed embeddings.
- Section 5 — Model training: train/validation split, train baseline models.
- Section 6 — Evaluation & visualization: metrics, confusion matrices, ROC curves.
- Section 7 — Sample predictions & error analysis: show example pairs with model outputs.

**Data**
- train.csv

**Reproducibility tips**
- Ensure the same Python environment and package versions are used (consider `pip freeze > requirements.txt`).
- Set deterministic random seeds found in the notebook (e.g., `random.seed`, `np.random.seed`, and model-specific seeds).
- If using external embeddings or large models, download them beforehand and verify paths.

**Expected outputs**
- Trained baseline model artifacts (in-memory or saved via `joblib`).
- Evaluation report with metrics: accuracy, precision, recall, F1, ROC-AUC.
- Visualization plots: confusion matrix, ROC curve, metric bar charts.

**Possible improvements / next steps**
- Add cross-validation and hyperparameter search (GridSearchCV or RandomizedSearchCV).
- Use contextual embeddings (BERT/Sentence-BERT) for improved semantic similarity.
- Add data augmentation or paraphrase generation to expand training data.
- Save the best model and provide an inference script for fast predictions.

**Contact & attribution**
- Notebook author: Tariful Islam 
---
