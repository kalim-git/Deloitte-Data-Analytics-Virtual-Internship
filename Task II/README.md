# Task 2: Gender Pay Equality Classification in Excel

Daikibo Industrials raised internal concerns about gender inequality in salary distribution. The Forensic Tech team processed employee compensation data and provided an **`Equality Table.xlsx`** that quantifies gender pay equality using a score between -100 and +100 for each job role across different factories.

## Background Information
Daikibo received internal complaints about gender pay inequality across different job roles and locations. The Forensic Tech Team developed an algorithm to compute an Equality Score for each job role, where:

- 0 indicates perfect equality.
- Negative values indicate gender pay disparity against women.
- Positive values indicate gender pay disparity against men.
- Scores range from -100 to +100.

## Objective

Objective is to Generate a new column **Equality Class** based on the values in the **Equality Score** column.

## Approach

1. Imported the <a href="https://github.com/kalim-git/Deloitte-Data-Analytics-Virtual-Internship/blob/main/Task%20II/Task%205%20Equality%20Table.xlsx">**`Equality Table.xlsx`**<a/> dataset, which contained:
  - `Factory`
  - `Job Role`
  - `Equality Score`

2. Created a new column, **"Equality Class"** based on the following rules:

  - **Fair**: Scores between -10 and +10
  - **Unfair**: Scores between -20 and -11 OR 11 and 20
  - **Highly Discriminative**: Scores below -20 or above +20

3. Catagorized the scores using an Excel formula:

   `=IF(ABS(C2) <= 10, "Fair", IF(ABS(C2) <= 20, "Unfair", "Highly Discriminative"))`

4. Saved and submitted the updated file named <a href="https://github.com/kalim-git/Deloitte-Data-Analytics-Virtual-Internship/blob/main/Task%20II/Task%205%20Equality%20Table%20-%20Updated.xlsx">**`Equality Table Updated.xlsx`**<a/> with the classifications applied to all job roles.
