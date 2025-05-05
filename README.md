# Employee Data Analysis – Task 1

This project is part of a data analysis task where we explore a dataset containing employee information. The notebook performs several basic data exploration tasks using Python, Pandas, Matplotlib, and Seaborn.

## 📁 File Structure

- `Code.ipynb` — Jupyter notebook with all the analysis steps.
- `Employee 1000x.csv` — Dataset containing employee information.
- `README.md` — This file.

## ✅ Tasks Performed

1. **Load and Explore Dataset**
   - Read the dataset using `pandas`.
   - View column names, structure, and sample rows.

2. **Check for Missing Data**
   - Used `df.isnull().values.any()` to check for any missing values.

3. **Gender Distribution**
   - Calculated the percentage of male and female employees using:
     ```python
     df['gender'].value_counts(normalize=True) * 100
     ```

4. **Job Title Counts**
   - Counted how many employees hold each job title:
     ```python
     title_count = df['Job Title'].value_counts().reset_index()
     title_count.columns = ['Job Title', 'Count']
     ```

5. **Data Visualization**
   - Created a bar chart of job title counts using Seaborn:
     ```python
     sns.barplot(data=title_count, x='Job Title', y='Count', palette='viridis')
     ```
   - Rotated x-axis labels for better readability and customized chart size.

## 📊 Libraries Used

- `pandas`
- `matplotlib`
- `seaborn`

Install them with:

```bash
pip install pandas matplotlib seaborn
