# 🚢 Titanic Survival — Exploratory Data Analysis

## 🎯 Project Objective
This project explores the Titanic passenger dataset to understand which factors — gender, passenger class, age, and fare — were associated with a passenger's chances of survival. The workflow covers data cleaning, dtype optimization, and univariate/bivariate visual analysis using `pandas`, `matplotlib`, and `seaborn`.

## 📋 Dataset Overview
The dataset contains passenger-level records from the RMS Titanic (1912), commonly used as a beginner-friendly benchmark dataset for classification and EDA practice.

**Columns:**

| Column        | Description                                              |
|---------------|------------------------------------------------------------|
| `PassengerId` | Unique ID for each passenger                              |
| `Survived`    | Survival status (0 = No, 1 = Yes) — **target variable**    |
| `Pclass`      | Ticket / passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)        |
| `Name`        | Passenger's full name                                     |
| `Sex`         | Gender of the passenger                                   |
| `Age`         | Age in years                                               |
| `SibSp`       | Number of siblings/spouses aboard                          |
| `Parch`       | Number of parents/children aboard                          |
| `Ticket`      | Ticket number                                              |
| `Fare`        | Passenger fare                                             |
| `Cabin`       | Cabin number (many missing values)                          |
| `Embarked`    | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |
                            

## 🛠️ Tools Used
- Python
- pandas
- NumPy
- matplotlib
- seaborn
- Jupyter Notebook

## 🧹 Data Cleaning
- Dropped the `Cabin` column due to a high percentage of missing values.
- Filled missing `Age` values with the median age grouped by `Pclass` and `Sex`.
- Filled missing `Embarked` values with the mode (`S`).
- Optimized dtypes: converted `Survived`, `Pclass`, `Sex`, and `Embarked` to `category`, and `Age` to `int` for memory efficiency.

## 📊 Analysis

### 1. Distribution of Age and Fare
Shows the distribution of passenger ages and ticket fares, highlighting common age groups and fare ranges.

![Age and Fare Distribution](images/graph1.png)

### 2. Count Distribution of Categorical Columns
Displays the frequency of each category for gender, passenger class, embarkation port, and survival status.

![Categorical Columns Count](images/graph2.png)

### 3. Survival vs Categorical Features
Compares survivor and non-survivor counts across gender, passenger class, and embarkation port.

![Survival by Categorical Features](images/graph3.png)

### 4. Age and Fare vs Survival
Compares age and fare distributions between survivors and non-survivors to identify potential survival patterns.

![Age and Fare vs Survival](images/graph4.png)

### 5. Correlation Heatmap
Visualizes relationships between numerical variables using correlation coefficients.

![Correlation Heatmap](images/grap5.png)

### 6. Age Distribution by Survival
Shows the age distribution of survivors and non-survivors to identify age-related survival trends.

![Age Distribution by Survival](images/grap6.png)

### 7. Pairplot for Numerical Features
Explores relationships among numerical features and their association with survival status.

![Pairplot](images/graph7.png)

### 8. Outlier Detection for Age and Fare
Identifies unusual age and fare values that differ significantly from the rest of the dataset.

![Outlier Detection](images/graph8.png)

### 9. Survival Rate by Gender and Passenger Class
Shows the percentage of survivors across genders and passenger classes, highlighting differences in survival rates.

![Survival Rate by Gender and Class](images/graph9.png)

## ✅ Key Takeaways
- **Gender**: Women had a substantially higher survival rate than men, consistent with the "women and children first" evacuation policy.
- **Passenger Class**: 1st class passengers survived at a much higher rate than 2nd and 3rd class, reflecting cabin location and access to lifeboats.
- **Fare**: Higher fares (correlated with class) were associated with better survival odds.
- **Age**: Younger passengers, especially children, had somewhat better survival odds than older adults.
- **Embarked**: Port of embarkation shows some association with survival, likely acting as a proxy for class/fare rather than a direct cause.
