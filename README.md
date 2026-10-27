# Titanic Survival Analysis

A complete, runnable Python project that explores passenger survival patterns in the Titanic training dataset. It includes the dataset CSV, analysis script, generated charts, and a findings report.

## Quick start (Windows PowerShell)

Python 3.10+ is required. From this folder run:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python src\titanic_analysis.py
```

If PowerShell blocks activation, use the environment directly:

```powershell
.venv\Scripts\python.exe -m pip install -r requirements.txt
.venv\Scripts\python.exe src\titanic_analysis.py
```

The dataset is included in `data/titanic.csv`. If you delete it, the program downloads a fresh copy when run. Use `python src\titanic_analysis.py --refresh` to replace it.

## Generated files

- `figures/survival_overview.png` — survival proportions by sex, passenger class, and age band.
- `figures/age_distribution.png` — age distributions split by survival outcome.
- `reports/findings.md` — computed summary statistics, interpretation, limitations, and source.

## Project structure

```text
data/titanic.csv             Input data
figures/                     Generated charts
reports/findings.md          Generated written results
src/titanic_analysis.py      Analysis and chart code
requirements.txt             Python packages
```

## Data source and assumptions

The CSV is Titanic passenger training data mirrored by Data Science Dojo at [the source CSV](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv). The analysis was written for this project. Please review the source repository's terms before redistributing the data, and cite the source when presenting results.

- `Survived` is treated as binary: 1 means survived and 0 means did not survive.
- Results are descriptive proportions in this dataset, not causal claims or predictions.
- Missing ages are excluded from age-based charts and reported as a limitation; no age imputation is done.
- Age bands are 0–12, 13–18, 19–35, 36–60, and 61–100 years.
- Fare remains in the dataset's original units.

## GitHub

The project can be published in a repository named `titanic-survival-analysis`. Include the code, README, requirements, CSV, charts, and report so visitors can inspect the complete run. After creating an empty GitHub repository, connect and push with:

```powershell

