# Customer Segmentation Clustering

Unsupervised machine learning project for segmenting retail customers based on demographic and spending behavior. The analysis compares K-Means, Hierarchical Clustering, and Gaussian Mixture Models, then profiles the best-performing customer segments for business interpretation.

## Project Overview

This notebook walks through an end-to-end clustering workflow:

- Exploratory data analysis of customer demographics and spending patterns
- Feature engineering using a spending-to-income ratio
- Feature scaling with `StandardScaler`
- Cluster selection using the elbow method and silhouette score
- Model comparison across K-Means, Agglomerative Clustering, and Gaussian Mixture Models
- Customer segment profiling by age, income, spending score, and gender distribution
- Business recommendations for which customer groups need more attention

## Repository Structure

```text
.
|-- customer-segmentation-clustering.ipynb
|-- requirements.txt
|-- .gitignore
`-- README.md
```

## Methods Used

### Exploratory Data Analysis

The notebook checks:

- Dataset structure and data types
- Summary statistics
- Missing values
- Age, income, and spending distributions
- Relationships between income, age, spending, and gender

### Feature Engineering

A `Spending_Income_Ratio` feature is created to capture how much a customer spends relative to their income.

### Clustering Models

The following unsupervised learning models are compared:

- K-Means Clustering
- Agglomerative Hierarchical Clustering
- Gaussian Mixture Model

Model quality is evaluated using:

- Silhouette Score
- Davies-Bouldin Score
- Calinski-Harabasz Score

## Key Result

The analysis identifies 6 customer segments using K-Means as the final model. The notebook then profiles each cluster and recommends focusing attention on high-income, high-spending customers because they are likely to be valuable targets for retention, loyalty programs, and premium campaigns.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/customer-segmentation-clustering.git
cd customer-segmentation-clustering
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

```bash
# Windows
.venv\Scripts\activate

# macOS/Linux
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the notebook

```bash
jupyter notebook customer-segmentation-clustering.ipynb
```

Run the notebook cells from top to bottom.

## Reproducibility Notes

- Random seeds are set for supported clustering models.
- Numerical features are standardized before clustering.
- The notebook was developed with Python 3.13.
- If results differ slightly across machines, check installed package versions and rerun all cells from a clean kernel.

## Future Improvements

- Move data loading into a reusable script or pipeline
- Add automated notebook execution checks
- Export final cluster profiles to CSV
- Add model artifact saving for repeatable downstream use
- Add interactive visualizations for exploring segments
