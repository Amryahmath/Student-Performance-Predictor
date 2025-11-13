# Student-Performance-Predictor

A simple project that demonstrates using classical machine learning models to predict student performance (pass/fail) from a small tabular dataset. The project includes an interactive Jupyter notebook that is ready to run in Google Colab or locally.

Key points:

- Models: Decision Tree, Random Forest, and SVM (comparison and evaluation)
- Environment: Notebook uses pandas, scikit-learn, matplotlib/seaborn for EDA, training and plotting
- Goal: show preprocessing, model training, evaluation (accuracy, confusion matrix), and simple feature importance

## Files in this repository

- `Student_Performance_Predictor.ipynb` — Main notebook with data loading, EDA, preprocessing, model training, evaluation, and visualizations.
- `student_performance_dataset (1).csv` — Dataset used by the notebook. Typical columns include Attendance, Study Hours, Internal Marks, and a Pass/Fail target.

If you move or rename the CSV, update the path used by the notebook.

## Run in Google Colab (recommended)

Colab already includes common ML packages and is the easiest way to run the notebook without installing anything locally.

1. Open this notebook in Colab (replace `main` if you use another branch):

```
https://colab.research.google.com/github/Amryahmath/Student-Performance-Predictor/blob/main/Student_Performance_Predictor.ipynb
```

2. Make the dataset available to the runtime. Options:

- Upload file to the session (one-off):

	- In Colab's left pane choose Files → Upload and upload `student_performance_dataset (1).csv`.
	- Read with pandas:

		```python
		import pandas as pd
		df = pd.read_csv('student_performance_dataset (1).csv')
		```

- Mount Google Drive (persistent across sessions):

	```python
	from google.colab import drive
	drive.mount('/content/drive')
	df = pd.read_csv('/content/drive/MyDrive/path/to/student_performance_dataset (1).csv')
	```

- Load directly from GitHub (if file is public in the repo). Note the filename has spaces — URL-encode them as `%20`:

	```python
	df = pd.read_csv('https://raw.githubusercontent.com/Amryahmath/Student-Performance-Predictor/main/student_performance_dataset%20(1).csv')
	```

Tip: renaming the CSV to remove spaces (e.g., `student_performance_dataset.csv`) makes raw URL access simpler.

## Run locally (Windows PowerShell)

If you prefer to run locally, create a virtual environment and install dependencies:

```powershell
python -m venv .venv; .\.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install notebook pandas numpy scikit-learn matplotlib seaborn
jupyter notebook Student_Performance_Predictor.ipynb
```

Open the notebook in Jupyter, then run cells top-to-bottom. The notebook reads the CSV from the repository root by default.

## What the notebook does

- Loads and inspects the dataset
- Cleans / preprocesses features (simple imputation/encoding if needed)
- Explores feature distributions and correlations
- Trains Decision Tree, Random Forest, and SVM classifiers
- Evaluates models with accuracy and confusion matrices
- Shows feature importance for tree-based models

## Suggestions / next steps

- Add `requirements.txt` for reproducible installs (I can create this for you).
- Rename the dataset to remove spaces and update the notebook (recommended).
- Add cross-validation and hyperparameter tuning (GridSearchCV) to improve model selection.
- Serialize the best model with `joblib` and provide a small prediction script.

If you'd like any of the above, tell me which and I will implement it.

## License

This project is provided for educational purposes.

---

