# Python for Social Research Workshop at Indian Statistical Institute, Kolkata on September 24, 2026

**A hands-on, beginner-friendly workshop on descriptive and inferential statistics in Python for anthropologists and sociologists.**

This repository contains all the materials for the workshop:

- A synthetic household survey dataset (200 households)
- A complete Jupyter notebook with all analysis code
- Beamer slide decks for every module
- A Python brush-up reference deck for participants new to coding

No prior programming experience is required.

---

## 📁 Repository Contents

```
python-social-research-workshop/
├── README.md
├── village_survey.csv
├── Demo.ipynb
├── intro.pdf
├── Mod1.pdf
├── Mod2.pdf
├── Mod3.pdf
├── Mod4.pdf
└── end.pdf
```

Each folder is described below.

### 📂 `data/`

- **`village_survey.csv`** — A synthetic survey of 200 households with 10 variables. Designed to mirror realistic Indian household survey distributions (informed by NFHS-5, IHDS, and NEEMSIS patterns).

### 📂 `notebooks/`

- **`Demo.ipynb`** — The master notebook used during the workshop. Every code block from the slides is pre-filled, with expected outputs annotated. Participants can run the whole notebook from start to finish.

### 📂 `slides/`

Beamer slide decks for the full workshop, compiled to PDF:

| File | Contents | Duration |
|---|---|---|
| `intro.pdf` | Welcome, roadmap, dataset overview, setup | 30 min |
| `Mod1.pdf` | Descriptive statistics in simple steps | 40 min |
| `Mod2.pdf` | Parametric inferential tests | 45 min |
| `Mod3.pdf` | Non-parametric tests for skewed/ordinal data | 35 min |
| `Mod4.pdf` | Visual analysis and presentation | 30 min |
| `end.pdf` | Ethics, reproducibility, and next steps | 10 min |

---

## 🎯 What You Will Learn

By the end of the workshop, participants will be able to:

- Load a survey dataset into Python and inspect its structure
- Compute descriptive statistics (mean, median, standard deviation)
- Filter rows and compare groups with simple code
- Run parametric tests (t-test, ANOVA, correlation, regression)
- Run non-parametric tests (Mann–Whitney, Wilcoxon, Kruskal–Wallis, chi-square, Spearman)
- Make four kinds of publication-ready charts
- Save results and figures reproducibly

---

## 🛠️ Requirements

### Software

- **Python 3.9 or higher** — [Download here](https://www.python.org/downloads/)
- **Jupyter Notebook** or **JupyterLab** — installed automatically with Anaconda
- Recommended: [Anaconda Distribution](https://www.anaconda.com/products/distribution) for a one-step setup

### Python packages

If you are using Anaconda, all these are installed by default. Otherwise, install them with:

```bash
pip install pandas numpy scipy matplotlib seaborn statsmodels
```

A full list of versions used in the workshop can be found in `requirements.txt`.

### Alternative: Google Colab

If you cannot install anything locally, use **Google Colab**:

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Upload `workshop_notebook.ipynb`
3. Upload `village_survey.csv` to the Colab session
4. Run the cells — Colab has all the required packages pre-installed

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/python-social-research-workshop.git
cd python-social-research-workshop
```

Or download the repository as a ZIP and extract it.

### 2. Launch Jupyter

From the repository folder, run:

```bash
jupyter notebook
```

Then open `notebooks/workshop_notebook.ipynb`.

### 3. Run the first cell

Run the first cell to confirm everything is installed:

```python
import pandas as pd
import numpy as np
import scipy.stats as stats
import matplotlib.pyplot as plt
import seaborn as sns

print("All libraries loaded successfully.")
```

If you see "All libraries loaded successfully", you are ready to begin.

---

## 📊 The Dataset

The workshop uses a **synthetic dataset** — no real households are represented. Its patterns, however, are designed to mirror real survey data from India.

### Variables

| Variable | Type | Description |
|---|---|---|
| `household_id` | Identifier | Unique household code (HH1000–HH1199) |
| `region_type` | Categorical | Rural or Urban |
| `gender` | Categorical | Gender of household head |
| `age` | Numeric | Age of household head in years |
| `education_years` | Numeric | Years of formal education |
| `household_size` | Numeric | Number of household members |
| `income` | Numeric | Monthly household income (INR) |
| `land_ownership` | Categorical | Yes or No |
| `shg_membership` | Categorical | Self-Help Group membership: Yes or No |
| `wellbeing_score` | Numeric | Self-reported wellbeing (0–100) |

Some values are deliberately missing in `income` and `wellbeing_score` to mirror real survey attrition.

### Reproducing the dataset

The dataset is generated from a script with a fixed random seed, so the exact CSV can be reproduced at any time:

```bash
python data/generate_dataset.py
```

---

## 📖 Recommended Reading

### Books

- McKinney, W. *Python for Data Analysis* — the standard reference
- Downey, A. *Think Stats* — free online, gentle introduction
- Healy, K. *Data Visualization: A Practical Introduction*
- D'Ignazio, C. & Klein, L. *Data Feminism* — ethics of data practice

### Online

- [pandas documentation](https://pandas.pydata.org/docs/)
- [seaborn gallery](https://seaborn.pydata.org/examples.html)
- [scipy.stats reference](https://docs.scipy.org/doc/scipy/reference/stats.html)
- [statsmodels documentation](https://www.statsmodels.org/)

---

## 🔁 Reproducibility

Every analysis in this workshop is fully reproducible. To re-run any figure or table:

1. Open `notebooks/workshop_notebook.ipynb`
2. Restart the kernel: **Kernel → Restart & Run All**
3. All outputs will regenerate exactly as shown in the slides

If you are using the notebook in your own research, replace `village_survey.csv` with your own data file and adjust the column names accordingly.

---

## 📚 Citation

If you use these materials in teaching or research, please cite:

```bibtex
@misc{python_social_research_workshop,
  title  = {Python for Social Research Workshop},
  author = {Workshop Facilitator},
  year   = {2026},
  url    = {https://github.com/YOUR_USERNAME/python-social-research-workshop}
}
```

---

## 🤝 Contributing

Suggestions, corrections, and improvements are welcome. Please open an issue or submit a pull request.

When contributing:

- Keep the language plain and beginner-friendly
- Avoid jargon without explanation
- Test all code blocks before submitting
- Use synthetic or anonymised data only

---

## 📄 License

This project is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to share and adapt the materials, provided you give appropriate credit.

---

## ✉️ Contact

For questions about the workshop, please open an issue in this repository, or write to the workshop facilitator at **[your email]**.

---

**Reproducible social science is a form of respect — for our colleagues, our readers, and the communities we study.**
