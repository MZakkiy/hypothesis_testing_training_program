# Analysis of the Impact of Training on Employee Performance

## 📋 Project Overview

This project conducts a statistical analysis to determine if attending a training program has a significant effect on employee performance scores. By applying a hypothesis test, the project aims to provide a data-driven answer to a crucial business question: "Is there a measurable return on investment for employee training?"

---

## 📊 Dataset

The analysis uses the **Employee Training and Performance Dataset**, which contains information about employees, including whether they attended training and their corresponding performance scores. The dataset includes the following columns:

* `EmployeeID`
* `Age`
* `Department`
* `Education`
* `ExperienceYears`
* `TrainingAttended` ('Yes' or 'No')
* `PerformanceScore`

---

## 🔬 Methodology

The core of this project is an **independent samples t-test** to compare the mean performance scores of two groups: employees who attended training and those who did not.

The analysis followed these key steps:
1.  **Hypothesis Formulation**:
    * **Null Hypothesis ($H_0$):** There is no significant difference in the mean performance scores between the two groups.
    * **Alternative Hypothesis ($H_1$):** There is a significant difference in the mean performance scores.
2.  **Data Preparation**: The dataset was divided into two samples based on the `TrainingAttended` column.
3.  **Assumption Checks**:
    * **Normality**: The Shapiro-Wilk test was performed on both groups.
    * **Homogeneity of Variances**: Levene's test was used to check if the variances of the two groups were equal.
4.  **Statistical Testing**: An independent samples t-test was conducted using SciPy to calculate the t-statistic and the p-value.

---

## 📈 Key Findings & Conclusion

### Findings

* The t-test yielded a **t-statistic of 9.188** and an extremely low **p-value of 2.86 x 10⁻¹⁹**.
* Since the p-value is significantly less than the standard alpha level of 0.05, the **null hypothesis was rejected**.
* The positive t-statistic indicates that the mean performance score for employees who **attended training is significantly higher** than for those who did not.

### Conclusion

The results provide strong statistical evidence that **attending training is associated with a significant increase in employee performance scores**. This analysis supports the business case for investing in employee development programs.

---

## 💻 How to Run

To replicate this analysis, you can run the `Hypothesis_Testing_Training_Program.ipynb` notebook in an environment like Google Colab or a local Jupyter setup.

1.  Clone this repository:
    ```bash
    git clone [https://github.com/MZakkiy/hypothesis_testing_training_program.git](https://github.com/MZakkiy/hypothesis_testing_training_program.git)
    ```
2.  Install the required libraries:
    ```bash
    pip install pandas scipy matplotlib seaborn
    ```
3.  Open and run the Jupyter Notebook.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas:** For data manipulation and analysis.
* **SciPy:** For conducting the statistical tests (Shapiro-Wilk, Levene, and t-test).
* **Matplotlib & Seaborn:** For data visualization.
* **Jupyter Notebook / Google Colab:** As the development environment.
