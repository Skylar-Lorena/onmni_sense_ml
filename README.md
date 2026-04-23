
# OmniSense: E-Commerce Sentiment & Product Analysis

**OmniSense** is a cross-platform NLP engine designed to analyze consumer sentiment and product performance across Amazon (Global) and regional tech marketplaces. This repository contains the end-to-end pipeline from data cleaning to model interpretability.

## Quickstart: Project Setup

To ensure the environment is consistent across the team, please follow these steps:

### 1. Clone & Environment Setup

```
# Clone the repository
git clone `github.com/Skylar-Lorena/onmni_sense_ml`
cd omnisense

# Create a virtual environment
python -m venv venv

# Download Language Models:
python -m spacy download en_core_web_sm

# Activate environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Download the NLP model for SpaCy
python -m spacy download en_core_web_sm

```

### 2. Directory Structure

Maintain this structure when adding new scripts or assets:

```
omnisense/
├── data/
│   ├── raw/                # Immutable original datasets
│   └── processed/          # Sanitized data (amazon_cleaned.csv, mendeley_cleaned.csv)
├── models/                 # Serialized model assets (XGBoost, TF-IDF, LabelEncoder)
├── notebooks/
│   ├── 01_eda.ipynb        # Data auditing and price normalization
│   ├── 02_baseline.ipynb   # SpaCy Pipeline & Naive Bayes Baseline
│   ├── 03_modeling.ipynb   # SMOTE Balancing & XGBoost Implementation
│   └── OmniSense_Master_Notebook.ipynb # FINAL: Executive Report & SHAP Insights
├── .gitignore              # Excludes venv, checkpoints, & large data files
├── README.md               # Project documentation
└── requirements.txt        # Pinned dependencies (XGBoost, SHAP, Imblearn)
```
----------

##  Data Dictionary


| Dataset    | File                   | Currency | Primary Use                                       |
| :--------- | :--------------------- | :------- | :------------------------------------------------ |
| **Amazon**   | `amazon_cleaned.csv`   | INR (₹)  | Pricing benchmarks and rating distributions.     |
| **Mendeley** | `mendeley_cleaned.csv` | BDT (Tk) | Raw text reviews for Sentiment Training.         |

##  Project Roadmap

- **Exploratory Data Analysis:** Data auditing, price normalization, and class distribution mapping.

- **Preprocessing & Baseline:** Text cleaning (Lemmatization/Stop-words) and initial Naive Bayes testing.

- **OmniSense Engine:** Implementation of SMOTE to handle class imbalance and XGBoost for high-accuracy classification.

- **Interpretability & ROI:** Utilizing SHAP to identify "Red Flag" keywords (e.g., battery, delivery, condition) for strategic business intervention.
    

----------

##  Contribution Guidelines

-   **Branching:** Do not push directly to `main`. Create a `feature/` or `dev/` branch for your task.
    
-   **Commits:** Use descriptive commit messages (e.g., `feat: add vader sentiment labels`).

-   **Dependencies:** If you add a library, update requirements.txt immediately.
    
-   **Notebooks:** Ensure all cells are run and outputs are visible before committing notebooks.
    

----------

## License

MIT

## Contributors

-   Lorenah -M, Ainsley -G, Angela -M, Dennis -K.

    

## Acknowledgments

Special thanks to the Mendeley and Amazon Open Data communities for providing the foundational datasets for this research.