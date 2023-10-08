# Heart-Attack-Analysis-Prediction-using-data-analysis-data-visualization-
1- Background:
2- The dataset is designed for the classification of heart attacks, a critical medical condition.
3- It is used for analytical and machine learning tasks related to predicting the likelihood of a heart attack based on various medical attributes.
4- Dataset Size:
5- The dataset contains 304 rows (samples) and 14 columns (features).
6- Features:
7- The dataset includes several features (attributes) that provide information about patients and their health conditions. These features can be used to predict the likelihood of a heart attack. Some of the key features include:
8- age: The age of the patient.
9- sex: The gender of the patient (0 = female, 1 = male).
10- cp: Chest pain type (1 = typical angina, 2 = atypical angina, 3 = non-anginal pain, 4 = asymptomatic).
11- trestbps: Resting blood pressure (in mm Hg).
12- chol: Serum cholesterol level (in mg/dl).
13- fbs: Fasting blood sugar (> 120 mg/dl) (1 = true, 0 = false).
14- restecg: Resting electrocardiographic results (0 = normal, 1 = having ST-T wave abnormality, 2 = probable or definite left ventricular hypertrophy).
15- thalach: Maximum heart rate achieved.
16- exang: Exercise-induced angina (1 = yes, 0 = no).
17- oldpeak: ST depression induced by exercise relative to rest.
18- slope: Slope of the peak exercise ST segment.
19- ca: Number of major vessels colored by fluoroscopy.
20- thal: Thalassemia (a type of blood disorder) results (3 = normal, 6 = fixed defect, 7 = reversible defect).
21- Target Variable:
22- The target variable in this dataset is often output or target, which indicates the presence (1) or absence (0) of a heart attack
Importing Libraries:
The code starts by importing necessary libraries, including pandas, numpy, matplotlib.pyplot, seaborn, and plotly.express. These libraries are used for data manipulation, analysis, and visualization.
Data Loading:
The dataset is loaded from a CSV file named 'heart.csv' using pd.read_csv(). The loaded data is stored in a DataFrame named df.
Data Exploration:
df.info() is used to display information about the dataset, including data types and the number of non-null values in each column.
df.isnull().sum() checks for missing values in each column and shows the count of missing values (which is zero in this case).
df.duplicated().sum() checks for duplicated rows, and since there's one duplicated row, it is removed using df.drop_duplicates().
Data Visualization:
Several data visualizations are created to explore the dataset:
A histogram showing the distribution of ages.
Boxplots and count plots to visualize relationships between variables, such as cholesterol levels by gender and the distribution of chest pain types.
Pie charts to display the distribution of heart disease, chest pain types, fasting blood sugar levels, exercise-induced angina, and more.
Histograms of numerical features.
Outlier Removal:
A custom function Remove_outliers is defined to remove outliers using the Interquartile Range (IQR) method. Outliers are replaced with NaN values.
Numerical Feature Boxplots:
A custom function boxplot_drawer is defined to draw boxplots for numerical features. These boxplots visualize the distribution and presence of outliers in these features.
Correlation Matrix:
A correlation matrix is computed using df.corr(). The matrix is then visualized as a heatmap using Seaborn's sns.heatmap(). This helps visualize the relationships between different features in the dataset.
