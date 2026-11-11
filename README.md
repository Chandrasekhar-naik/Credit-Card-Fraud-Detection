# Credit Card Fraud Detection

This project explores credit-card transaction fraud detection with an
unsupervised autoencoder. It includes notebooks for exploratory data analysis,
preprocessing, model training, and threshold selection, along with the saved
model artifacts.

## Project structure

```text
app/                  Placeholder for an application entry point
data/                 Local dataset (download separately; not tracked)
models/               Trained autoencoder, scaler, and decision threshold
notebooks/
  01_eda.ipynb         Exploratory data analysis
  02_preprocessing.ipynb
  03_autoencoder.ipynb Training, evaluation, and threshold tuning
requirements.txt       Python dependencies
```

## Dataset

The dataset is not included in this repository because the CSV is larger than
GitHub's 100 MB per-file limit. Download the **Credit Card Fraud Detection**
dataset from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
and place `creditcard.csv` in the `data/` directory:

```text
data/creditcard.csv
```

The notebooks expect the CSV to contain the `Class` target column and the
transaction features used by the Kaggle dataset.

## Setup

Use Python 3.10 or later and install the dependencies:

```bash
python -m venv .venv
```

Activate the virtual environment, then run:

```bash
python -m pip install -r requirements.txt
```

## Run the notebooks

From the project root, start Jupyter:

```bash
jupyter notebook
```

Run the notebooks in order:

1. `notebooks/01_eda.ipynb`
2. `notebooks/02_preprocessing.ipynb`
3. `notebooks/03_autoencoder.ipynb`

The autoencoder notebook trains and evaluates the model, tunes a reconstruction
error threshold using validation data, and saves artifacts under `models/`.
The checked-in model artifacts are provided for reference; rerun the notebook
to regenerate them for your environment and dataset.
