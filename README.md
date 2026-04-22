
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
│   ├── raw/                                        # Immutable original datasets
│   │   ├── All Electronics.csv
│   │   └── all_data.csv
│   └── processed/                                  # Sanitized data for modeling
│       ├── amazon_cleaned.csv
│       └── mendeley_cleaned.csv
├── notebooks/
│   ├── 01_exploratory_data_analysis.ipynb          # Completed: Visuals & Cleaning Logic
│   ├── 02_preprocessing_and_baseline.ipynb         # Skeleton: SpaCy Pipeline & Baseline
│   ├── 03_advanced_modeling_and_interpretability.ipynb  # Skeleton: XGBoost & SHAP
│   └── 04_final_evaluation_and_conclusions.ipynb   # Skeleton: Final Stakeholder Report
├── .gitignore                                      # Excludes venv, checkpoints, & data/
├── README.md                                       # Setup instructions & Data Dictionary
└── requirements.txt                                # Project dependencies
```
----------

##  Data Dictionary


| Dataset    | File                   | Currency | Primary Use                                       |
| :--------- | :--------------------- | :------- | :------------------------------------------------ |
| **Amazon**   | `amazon_cleaned.csv`   | INR (₹)  | Pricing benchmarks and rating distributions.     |
| **Mendeley** | `mendeley_cleaned.csv` | BDT (Tk) | Raw text reviews for Sentiment Training.         |

##  Project Roadmap

1.  **[01_Exploratory_Data_Analysis:** Data auditing, price normalization, and distribution plots.
    
2.  **[02_Preprocessing_and_Baseline:** Text cleaning (Lemmatization/Stop-words) and initial Naive Bayes model.
    
3.  **[03_Advanced_Modeling:** XGBoost/Transformer models and **SHAP** interpretability.
    
4.  **[04_Final_Evaluation:** Cross-platform comparison and business insights.
    

----------

##  Contribution Guidelines

-   **Branching:** Do not push directly to `main`. Create a `feature/` or `dev/` branch for your task.
    
-   **Commits:** Use descriptive commit messages (e.g., `feat: add vader sentiment labels`).
    
-   **Notebooks:** Ensure all cells are run and outputs are visible before committing notebooks.
    

----------

## License

MIT

## Contributors

-   Lorenah -M, Ainsley -G, Angela -M, Dennis -K.

    

## Acknowledgments

TBU
