# 🚢 Titanic Dataset - Exploratory Data Analysis (EDA)

## 📌 Project Overview
As part of my **AI & ML Internship**, I performed a full **Exploratory Data Analysis (EDA)** on the Titanic dataset.  
The main goal was to deeply understand the data using **statistics, visualizations**, and **pattern detection techniques**.

---

## 📚 What I Learned
- Descriptive Statistics (mean, median, standard deviation)
- Visualizing numeric and categorical data
- Identifying missing values, outliers, skewness
- Understanding feature relationships using Correlation
- Preparing data for machine learning models

---

## 🛠️ Tools and Libraries
- Python 🐍
- Pandas 📊
- Matplotlib 🎨
- Seaborn 🌊
- Plotly 📈 (optional for advanced visuals)

---

## 📂 Dataset
- **Dataset Name:** Titanic Passenger Data
- **Source:** [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)

---

## 📋 Data Information
After inspecting using `data.info()`, we found:

| Column       | Non-Null Count | Dtype    | Description                   |
|--------------|----------------|----------|-------------------------------|
| PassengerId  | 891             | int64    | Unique ID for each passenger  |
| Survived     | 891             | int64    | Survival (0 = No, 1 = Yes)    |
| Pclass       | 891             | int64    | Ticket class (1, 2, 3)        |
| Name         | 891             | object   | Passenger name                |
| Sex          | 891             | object   | Gender                        |
| Age          | 714             | float64  | Age in years                  |
| SibSp        | 891             | int64    | # of siblings/spouses aboard  |
| Parch        | 891             | int64    | # of parents/children aboard  |
| Ticket       | 891             | object   | Ticket number                 |
| Fare         | 891             | float64  | Passenger fare                |
| Cabin        | 204             | object   | Cabin number                  |
| Embarked     | 889             | object   | Port of Embarkation           |

---

## 📊 Plots and Visualizations

I created plots based on **data types**:

### Numeric Features (Age, Fare, SibSp, Parch, PassengerId, etc.)
- **Histograms**: To see distributions
- **Boxplots**: To detect outliers
- **Violin plots**: Optional for detailed distribution shape

Example:
```python
plt.figure(figsize=(10,6))
sns.histplot(data['Age'], kde=True, bins=30)
plt.title('Age Distribution')
plt.show()

sns.boxplot(x=data['Fare'])
plt.title('Fare Distribution with Outliers')
plt.show()
```

---

### Categorical Features (Sex, Pclass, Embarked)
- **Countplots**: For frequencies
- **Pie Charts** (Optional)

Example:
```python
sns.countplot(x='Sex', data=data)
plt.title('Sex Distribution')
plt.show()

sns.countplot(x='Pclass', data=data, hue='Survived')
plt.title('Passenger Class vs Survival')
plt.show()
```

---

### Correlation Heatmap (only for numeric columns)
Before plotting, I used:
```python
numeric_df = data.select_dtypes(include=['float64', 'int64'])
sns.heatmap(numeric_df.corr(), annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()
```
✅ This avoids the error you faced (`could not convert string to float`) because `Name`, `Ticket`, etc. are non-numeric.

---

## 🔥 Important Observations
- `Age` and `Cabin` have missing values.
- `Fare` feature has **outliers**.
- Strong positive correlation between `SibSp` and `Parch`.
- `Sex` and `Pclass` are highly related to survival.

---

# 📚 Quick Answers to Interview Questions:

### 1. What is the purpose of EDA?
➔ To understand the data, identify patterns, spot anomalies, and prepare for modeling.

### 2. How do boxplots help in understanding a dataset?
➔ Boxplots show median, quartiles, and detect outliers easily.

### 3. What is correlation and why is it useful?
➔ Correlation measures how features relate to each other. Useful for feature selection and detecting redundancy.

### 4. How do you detect skewness in data?
➔ By checking histograms or using `df.skew()` function.

### 5. What is multicollinearity?
➔ When two or more features are highly correlated, it can confuse the model.

### 6. What tools do you use for EDA?
➔ Pandas, Matplotlib, Seaborn, Plotly.

### 7. Can you explain a time when EDA helped you find a problem?
➔ Example: "While exploring Titanic data, I found missing values in 'Age' column and outliers in 'Fare', which needed cleaning."

### 8. What is the role of visualization in ML?
➔ Visualization helps understand the hidden patterns, informs feature engineering, and improves model performance.

---

## 🚀 Final Outcome
This EDA helped:
- Understand data distribution
- Handle missing values & outliers
- Prepare the dataset for further machine learning modeling.

✅ Task completed successfully for internship submission!

---

# 📬 Connect with Me
- **LinkedIn:** [Your LinkedIn Profile](https://www.linkedin.com/in/a-harshraj)

---

# 🔥 Thank you for checking out my project!
