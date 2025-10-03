# Credit Card Unsupervised Fraud Detection

## Overview

This repository provides an end-to-end workflow for detecting fraudulent credit card transactions using unsupervised machine learning techniques. The project leverages both Isolation Forest and Autoencoder models to identify anomalies in highly imbalanced datasets.

## Dataset

- **Source:** [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Transactions:** 284,807
- **Fraudulent:** 492
- **Features:** 30 anonymized features (V1–V28), `Time`, and `Amount`

## Workflow

1. **Data Preprocessing**
   - Remove unusable columns (`Time`)
   - Handle duplicates and missing values
   - Scale `Amount` feature using `StandardScaler`
2. **Exploratory Data Analysis**
   - Histograms, boxplots, scatterplots, and correlation heatmaps
   - PCA for dimensionality reduction and visualization
3. **Modeling**
   - **Isolation Forest:** Detects anomalies based on contamination rate
   - **Autoencoder:** Learns compressed representation, flags outliers by reconstruction error
4. **Evaluation**
   - Metrics: Precision, Recall, F1-Score, ROC-AUC, PR-AUC
   - Visualize predictions in PCA space

## Results

- Isolation Forest and Autoencoder both provide useful anomaly detection.
- ROC-AUC and PR-AUC are used to evaluate performance, especially for rare fraud cases.
- Combining models and tuning thresholds can maximize recall, prioritizing detection of rare fraud.

## Usage

1. **Clone the repository**
   ```sh
   git clone https://github.com/MhmdSafa7/creditcard-unsupervised-fraud.git
   cd creditcard-unsupervised-fraud
   ```

2. **Set up Python environment**
   ```sh
   python -m venv creditvenv
   source creditvenv/Scripts/activate  # Windows
   # or
   source creditvenv/bin/activate      # Linux/Mac
   pip install -r requirements.txt
   ```

3. **Download the dataset**
   - Place `creditcard.csv` in the `data/` directory.

4. **Run the notebook**
   - Open [notebook/main.ipynb](notebook/main.ipynb) in VS Code or JupyterLab.
   - Execute cells step by step to reproduce results.

## Contributing

- Fork the repository and create feature branches (`feature/your-feature`)
- Use clear commit messages and pull requests
- Follow PEP8 and add docstrings/comments for clarity
- Run `black` and `flake8` before pushing

## Version Control Best Practices

- Commit often with descriptive messages
- Use `.gitignore` to exclude environment and data files
- Tag releases for major milestones
- Review code via pull requests



## Contact

For questions or collaboration, open an issue or contact [mhmdhsafa7@gmail.com].