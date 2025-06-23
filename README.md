# data-cleaning-and-preprocessing

This project focuses on cleaning and preprocessing a real-world marketing dataset, as part of a data analytics pipeline. The dataset used is the **Marketing Campaign Data** sourced from Kaggle.

## Dataset Source

- **File:** `marketing_campaign.csv`
- **Source:** [Kaggle - Marketing Campaign Data](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign)

---

## Objective

To clean and prepare a raw dataset (with nulls, duplicates, inconsistent formats, etc.) using **Python (Pandas)**. The goal is to produce a cleaned version of the dataset, suitable for further analysis and modeling.

---

##  Tools Used

- Python 3.x
- Pandas
- Jupyter Notebook / VSCode
- Matplotlib / Seaborn (optional for visualization)

---

##  Steps Performed

1. **Load and Inspect Data**
   - Read the dataset using `pd.read_csv()` with appropriate separator.
   - Checked for null values, duplicates, and data types.

2. **Handle Missing Values**
   - Dropped rows with missing values in the `Income` column.

3. **Remove Duplicates**
   - Removed any duplicate rows.

4. **Clean Column Names**
   - Converted column names to lowercase.
   - Replaced spaces with underscores for consistency.

5. **Fix Date Format**
   - Converted `Dt_Customer` to `datetime` format (`YYYY-MM-DD`).

6. **Standardize Categorical Values**
   - Cleaned up `Education` and `Marital_Status` columns by:
     - Removing typos, inconsistencies, and mixed cases.
     - Grouping uncommon entries under standard labels.

7. **Remove Redundant Columns**
   - Dropped constant columns like `Z_CostContact`, `Z_Revenue`.

8. **Filter Outliers**
   - Removed customers with unrealistic ages (<18 or >100).

---

##  Output

- **Cleaned File:** `marketing_campaign_cleaned_final.csv`
- **Rows Remaining:** ~2,000 (after cleaning)
- **Ready for:** Analysis, visualization, or machine learning

---

##  Summary of Key Fixes

| Issue                      | Solution                              |
|---------------------------|----------------------------------------|
| Null values in `Income`   | Dropped rows                          |
| Duplicate rows            | Removed                               |
| Column name inconsistencies | Cleaned and standardized             |
| Date format issues        | Converted to `YYYY-MM-DD`             |
| Categorical inconsistencies | Mapped to consistent values         |
| Constant columns          | Removed                               |
| Age outliers              | Filtered to 18–100 years              |

---

## How to Run

```bash
pip install pandas
python clean_marketing_data.py
