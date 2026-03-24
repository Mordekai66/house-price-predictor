# House Price Predictor

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?style=flat-square&logo=scikitlearn)
![Gradio](https://img.shields.io/badge/Gradio-UI-yellow?style=flat-square&logo=gradio)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Views](https://visitor-badge.laobi.icu/badge?page_id=Mordekai66.house-price-predictor)

Regression pipeline that predicts house sale prices from structural and location features. Trains and compares Linear Regression, Decision Tree, and Random Forest regressors, tunes hyperparameters via GridSearchCV, and exposes a Gradio interface for real-time price estimation.

---

## Features

- Preprocessing: median imputation for numeric columns, mode imputation for categorical, `LabelEncoder`, `StandardScaler`
- Model comparison: Linear Regression vs. Decision Tree vs. Random Forest (MSE, MAE, R²)
- Hyperparameter tuning via `GridSearchCV` with 5-fold cross-validation
- Visualizations: price distribution, size–price scatter, location box plot, actual vs. predicted scatter
- Interactive Gradio UI for live price prediction

---

## Dataset

File: `House_Prices.csv`

| Feature | Type |
|---|---|
| Location | Categorical — Rural, Suburban, Urban |
| Size (sqft) | Numeric |
| Bedrooms | Numeric |
| Bathrooms | Numeric |
| Year Built | Numeric |
| Condition | Numeric |
| **Price** | **Target — continuous** |

---

## Setup

```bash
pip install -r requirements.txt
```

Place `House_Prices.csv` in the same directory as the notebook, then run all cells.

---

## Gradio Interface

After running the final cell, a local web UI launches. Select a location from the dropdown, enter numeric values, and the Random Forest model returns the predicted house price.

---

## Project Structure

```
.
├── House_Prices.ipynb
├── House_Prices.csv
├── LICENSE
├── .gitignore
└── README.md
```

---

## License

MIT — see [LICENSE](LICENSE) for full terms.