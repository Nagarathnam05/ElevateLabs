# Task_1_README

Mobile Sales Data Analysis
This notebook performs comprehensive data preprocessing on a mobile sales dataset, preparing it for further analysis or machine learning model development. The steps cover various essential data cleaning and transformation techniques.

Notebook Overview:
Data Loading: The mobile_sales_data.csv dataset is loaded into a pandas DataFrame.
Handling Missing Values:
Numeric Columns: Missing values in numerical columns (Quantity, UnitPrice, CostPerUnit, DiscountRate, RAM, Storage) are imputed using the median of their respective columns.
Categorical Columns: Missing values in general categorical columns (Product, Region, Network) are imputed using the mode.
Binary Columns (Shipped, Delivered): Specific handling includes converting boolean/numeric representations to 'Yes'/'No' strings, and then imputing missing values with the mode of the column. For 'Delivered', missing values are further filled based on the 'Shipped' status.
Encoding Categorical Features:
Binary Encoding: The 'Shipped' and 'Delivered' columns are converted from 'Yes'/'No' strings to numerical (1/0) representations.
Descriptive Statistics: Basic statistical summaries are displayed to understand the dataset's distribution after initial cleaning.
Feature Scaling (Normalization and Standardization):
Numerical features (Quantity, UnitPrice, CostPerUnit, DiscountRate, RAM, Storage) are standardized using StandardScaler from sklearn.preprocessing to ensure they contribute equally to further analysis.
Outlier Detection and Removal:
Box plots are generated for numerical columns to visualize potential outliers.
Outliers are detected and removed using the Interquartile Range (IQR) method (1.5 * IQR rule) for each numerical column. The DataFrame is updated to reflect the removal of rows containing outliers.

Resources:
This notebook utilizes popular Python libraries for data manipulation, numerical operations, machine learning preprocessing, and visualization:

pandas: For data loading, manipulation, and analysis (pd).
numpy: For numerical operations (np).
sklearn.preprocessing: Specifically StandardScaler for feature scaling.
matplotlib.pyplot: For creating static, interactive, and animated visualizations (plt).
seaborn: For making statistical graphics based on matplotlib (sns).
