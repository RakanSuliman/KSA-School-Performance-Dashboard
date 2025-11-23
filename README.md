# Education Performance Dashboard (Tarteeb)
### This project is part of CS316 course [Introduction To AI And Data Science] taught by Dr.Omar Alomeir

This repository contains two main components:

1. A **Streamlit dashboard** for exploring school performance and exam results.
2. A **Jupyter notebook** for cleaning, preparing, and analyzing the raw Tarteeb data.

---

## 📁 Repository Structure

- `PresentationDashboard.py`  
  Interactive Streamlit app to:
  - Filter schools by **year, region, city, authority, education type, exam type, specialization**, etc.
  - View **KPIs** such as average scores, ranks, and school counts.
  - Show **charts** (top schools by score, distributions, scatter plots).
  - Run simple **machine learning models**:
    - Regression to predict future scores.
    - Classification to predict top-performing schools.
    - Logistic model to detect **underperforming schools**.
    - PCA (unsupervised) to visualize schools by performance features.

- `Tarteeb.ipynb`  
  Data preparation and exploratory analysis notebook that:
  - Loads the raw dataset (e.g. `tarteeb_all_merged_cityfix.csv`).
  - Cleans missing values and inconsistent entries.
  - Creates useful columns (e.g. averages, ranks, size indices).
  - Filters data by exam type, specialization, and year.
  - Produces descriptive statistics and visualizations (distributions, correlations, maps, etc.).
  - Saves a **cleaned version** of the dataset for use in the dashboard.
  - Applying **K-Nearest Neighbors (KNN) imputation** to:
    - Fill in missing values (city, region, and area) based on similar schools  
    - Improve data quality before modeling and visualization
  - Saving a **cleaned and enhanced dataset** for use in the Streamlit dashboard.
---

## 📊 Data

The project works with a Tarteeb-like dataset containing:

- School information (name, region, city, authority, size).
- Exam details (year, exam type, specialization).
- Performance metrics:
  - Average scores (`avg`, `dept_avg`, `office_avg`, `area_avg`, etc.).
  - Ranks by country/area.
  - Student counts per school and year.

> ⚠️ Make sure the CSV files used in the notebook and dashboard are in the same folder as these scripts, or update the paths in the code.

---

## 🚀 Getting Started

### 1. Install dependencies

You can install the main libraries with:

```bash
pip install streamlit pandas numpy altair scikit-learn matplotlib seaborn plotly
```
## 🙏 Acknowledgements
I would like to thank my colleagues for their collaboration and support in this project:
* **Nawaf AlTamimi**
* **Mohammad Aldemaiji**
* **Saud Alnasser**

Their contributions were essential to the development and completion of this dashboard and analysis.
