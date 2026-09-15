# 📊 Exploratory Data Analysis — Student Performance Factors

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the **Student Performance Factors** dataset.

The main purpose of this project is to explore the dataset, identify patterns and trends, analyze relationships between different factors, and understand which factors are associated with students' exam performance.

Python libraries such as **Pandas, NumPy, Matplotlib, and Seaborn** are used for data analysis and visualization.

---

## 🎯 Objectives

The objectives of this project are to:

* Understand the structure of the dataset.
* Perform statistical analysis of numerical variables.
* Identify missing and duplicate values.
* Explore categorical and numerical features.
* Visualize the distribution of important variables.
* Analyze relationships between different student performance factors.
* Identify correlations between numerical variables.
* Determine factors associated with `Exam_Score`.
* Present meaningful insights from the data.

---

## 📂 Dataset

**Dataset Name:** `StudentPerformanceFactors.csv`

The dataset contains **6,607 records and 20 features** related to student academic performance.

### Features

* `Hours_Studied`
* `Attendance`
* `Parental_Involvement`
* `Access_to_Resources`
* `Extracurricular_Activities`
* `Sleep_Hours`
* `Previous_Scores`
* `Motivation_Level`
* `Internet_Access`
* `Tutoring_Sessions`
* `Family_Income`
* `Teacher_Quality`
* `School_Type`
* `Peer_Influence`
* `Physical_Activity`
* `Learning_Disabilities`
* `Parental_Education_Level`
* `Distance_from_Home`
* `Gender`
* `Exam_Score`

The main variable of interest in this analysis is **`Exam_Score`**.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook / VS Code

---

## 🔍 EDA Process

The project follows a structured Exploratory Data Analysis workflow.

### 1. Data Loading

The dataset is loaded using Pandas.

```python
df = pd.read_csv("StudentPerformanceFactors.csv")
```

### 2. Data Understanding

The dataset is examined using functions such as:

```python
df.head()
df.tail()
df.shape
df.columns
df.info()
df.describe()
df.dtypes
df.nunique()
```

These functions help understand the size, structure, data types, and statistical properties of the dataset.

### 3. Data Cleaning

The dataset is checked for:

* Missing values
* Duplicate records
* Incorrect data types
* Unique categorical values

Example:

```python
df.isnull().sum()
df.duplicated().sum()
```

### 4. Univariate Analysis

Individual variables are analyzed to understand their distributions.

Examples include:

* Exam Score
* Hours Studied
* Attendance
* Gender

Histograms, count plots, and boxplots are used for visualization.

### 5. Bivariate Analysis

Relationships between two variables are explored.

Examples include:

* Hours Studied vs Exam Score
* Attendance vs Exam Score
* Previous Scores vs Exam Score
* Sleep Hours vs Exam Score
* Gender vs Exam Score
* Teacher Quality vs Exam Score
* Parental Involvement vs Exam Score

### 6. Correlation Analysis

A correlation matrix is created for numerical variables.

```python
numeric_df = df.select_dtypes(include=np.number)

correlation = numeric_df.corr()
```

A heatmap is used to visualize the correlations.

```python
sns.heatmap(
    correlation,
    annot=True,
    cmap="coolwarm",
    fmt=".2f"
)
```

The correlations with `Exam_Score` are also examined to identify important numerical relationships.

### 7. Group Analysis

Average exam scores are compared across different categories such as:

* Gender
* Motivation Level
* Parental Involvement
* Teacher Quality
* Family Income

---

## 📈 Visualizations

The project includes several visualizations, including:

* Histograms
* Boxplots
* Count plots
* Scatter plots
* Correlation heatmap
* Pairplot

These visualizations make it easier to identify patterns, relationships, distributions, and potential outliers in the dataset.

---

## 💡 Key Insights

The analysis focuses on understanding how different academic, personal, family, and environmental factors are associated with student performance.

Important factors explored include:

* Study hours
* Attendance
* Previous academic scores
* Sleep hours
* Tutoring sessions
* Motivation level
* Parental involvement
* Teacher quality
* Access to resources
* Family income
* Internet access
* Peer influence
* Physical activity

Correlation analysis is used to identify which numerical variables have stronger relationships with exam scores.

> **Note:** Correlation indicates an association between variables and does not necessarily imply causation.

---

## 📝 Conclusion

This project demonstrates the use of **Exploratory Data Analysis** to understand student performance data.

Through data cleaning, statistical summaries, visualizations, correlation analysis, and group-based comparisons, the project explores patterns and relationships between different factors and students' exam scores.

The analysis provides a clearer understanding of the dataset and demonstrates how EDA can transform raw data into meaningful and interpretable information.

---

## 📁 Project Structure

```text
Student-Performance-EDA/
│
├── StudentPerformanceFactors.csv
├── Student_Performance_EDA.ipynb
└── README.md
```

---

## ▶️ How to Run the Project

1. Download or clone the project.
2. Open the project folder in **VS Code** or **Jupyter Notebook**.
3. Make sure `StudentPerformanceFactors.csv` is in the same folder as the notebook.
4. Install the required Python libraries.
5. Run the notebook cells sequentially.

Install the required libraries using:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

### Project

**Exploratory Data Analysis (EDA) — Student Performance Factors**

---

⭐ This project was created to develop practical skills in **data cleaning, statistical analysis, data visualization, correlation analysis, and interpretation of real-world datasets**.
