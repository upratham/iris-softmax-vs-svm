# Iris Classification with Softmax Regression & SVM

A clean, reproducible implementation for classifying Iris species using **Softmax Regression (multinomial LogisticRegression)** and **Support Vector Machines (SVC)**.  
This repository is based on the notebook `75da026b-dfc8-4d70-b0ed-12b6f062213d.ipynb` by *Prathamesh Uravane (UID 122016187)* and packages the work so it can be easily cloned, set up, and re‑run.

---

## Highlights
- Trains and evaluates two classic models: **LogisticRegression** (multinomial) and **SVM (RBF kernel)**.
- Reports **test accuracy** and **confusion matrix**.
- Uses the dataset file **`Data_Iris.csv`** expected at the repo root.
- Minimal dependencies; quick to run on CPU.

---

## Repo Structure
```
.
├── iris_softmax_vs_svm.ipynb   # Jupyter Notebook with full workflow
├── Data_Iris.csv                                    # CSV dataset (add this file)
└── README.md
```

> **Note:** The notebook expects a column named `species_name` as the target label.  
> The current notebook factorizes **all** columns (including numeric ones) for simplicity. If your CSV already has numeric features, you may remove that step and only encode the label column.

---

## Dataset
- File: **`Data_Iris.csv`**
- Format: CSV with feature columns (e.g., sepal/petal measurements) and a categorical label column `species_name`.
- Place the file at the repository root (same folder as the notebook) or update the path inside the notebook.

If you don't have the file, you can export the classic Iris dataset to this schema or adapt the notebook’s loading code to `sklearn.datasets.load_iris()`.

---

## Environment & Dependencies
- Python ≥ 3.9
- Packages:
  - `pandas`
  - `matplotlib`
  - `scikit-learn`

### Quick Setup
```bash
# (recommended) create a virtual environment
python -m venv .venv
# activate it (Windows)
.venv\Scripts\activate
# activate it (macOS/Linux)
source .venv/bin/activate

# install dependencies
pip install pandas matplotlib scikit-learn jupyter
```

---

## How to Run
1. **Add the dataset** file **`Data_Iris.csv`** to the repo root.
2. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
3. Open `75da026b-dfc8-4d70-b0ed-12b6f062213d.ipynb` and run all cells.
4. The notebook prints:
   - Test accuracy for each model
   - Confusion matrices

> Optional: A commented `StandardScaler` section is included. You can enable it to improve performance for SVM-based models (scaling is generally recommended).

---

## Reproducibility
- The train/test split uses `random_state=42` for consistency.
- Logistic Regression uses `solver='lbfgs'` and `max_iter=1000` (suitable for multinomial classification).
- SVM uses the **RBF** kernel with default hyperparameters; feel free to tune `C` and `gamma`.

---

## Suggested Repository Names
Pick one of these (or mix your own):
- `iris-softmax-vs-svm`
- `iris-ml-classifiers`
- `iris-logreg-svm-comparison`
- `iris-species-classification`
- `hw5-iris-classification`

**My top pick:** `iris-softmax-vs-svm` — short, descriptive, and searchable.

---

## License
This template is provided under the **MIT License** by default. Update as needed.

---

## Acknowledgements
- Original notebook author: *Prathamesh Uravane (UID 122016187)*.
- The Iris dataset was originally introduced by R.A. Fisher (1936).

