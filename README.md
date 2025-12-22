# Technical Test — Tutoring Assignment (technical_test_solution.ipynb)
---

## Project summary
This repository contains a Jupyter Notebook that solves a Tutor-Student Assignment Problem --- Bipartite Matching with One Sided Preferences problem using the CPLEX optimization engine. The input dataset (`Interview small data.xlsx`) includes three sheets for new students, existing students, and tutor information. The notebook (.ipynb) loads the data, formulates an optimization model, solves it, and displays the assignment results.

This README explains how to set up the environment and run the notebook.

If you do not need to run the code, just click the .ipynb file to see the code and output directly on github.
---

## Files in this project

- `technical_test_solution.ipynb` — main Jupyter Notebook containing data imports, modeling, solution and results.
- `Interview small data.xlsx` — input dataset with three sheets, with columns:
  - **New Students** — studentId, tutoringNeed, tuitionCentre.
  - **Existing Students** — tutorId, studentId, tutoringNeed, tuitionCentre, active.
  - **Tutor Information** — tutoringSkills, preferredCentre1, preferredCentre2, maxOverallCapacity.
- `README.md` — (this document).
- `requirements.txt` — dependencies for the Python environment.
- `test_presentation.pptx` — ppt presentation summarizing the approach and results.
---

## Recommended setup (Windows example - without downloading IBM ILOG CPLEX Optimization Studio free edition)

1. Clone the repo and `cd` into it (or just download the files and skip this step). Note that you might want to change the working directory using cd in the command line to where you would like to save the file.

This step is optional (change to your own directory):
```bash
cd C:\Users\darryl\Downloads
```
Then clone the repo (put the full directory in cd if it doesn't work):
```bash
git clone https://github.com/darrylteo/Technical-Test---Tutor-Student-Matching-Problem
cd Technical-Test---Tutor-Student-Matching-Problem
```

2. (Optional) Create and activate a virtual environment (the directory is where the activate script is located... might be in .\bin or .\Scripts):

```bash
python -m venv .venv
.\.venv\Scripts\activate
```


3. Install dependencies. 22-12-2025 note: requirements installed this way does not work for newer versions of python!! I downloaded python 3.10.11 and made a 3.10 environment using the command
   ```bash
   py -3.10 -m venv .venv
   ```
Install dependencies with:

```bash
pip install -r requirements.txt
```

Or install the core packages manually (not recommended):

```bash
pip install pandas numpy openpyxl jupyter ipython docplex cplex
```
4. Open the notebook technical_test_solution.ipynb (i am using VSCode).

5. In the notebook (for VSCode), select the Python interpreter corresponding to your environment (e.g., `.venv/Scripts/python.exe` if you created one). This can be done with the command palette (Ctrl+Shift+P) and searching for "Python: Select Interpreter", and finding where you saved the environment.
