# UCI Adult - Analyzing Income Factors
**EPITA – MSc Artificial Intelligence Systems (AIS)**  
**Spark & Python for Big Data AIS S2 F25**

**Students:**
- TRUONG Kim Tan
- LE Linh Long
- Farouk RAHAL
---

## 1. Data Preprocessing
- Handle missing values by creating `Unknown` category for each categorical column
- Remove redundancy of `education` and `education_num` by removing `education` column
- Cleaning categorical columns by removing leading and trailing whitespaces
---

## 2. Feature Engineering
- Transform `income` column to binary values (0 and 1).
- Creating new features by:
    - Grouping `native_country` variable into `US` and `Others`
    - Creating `age_category` column based on `age`
    - Substracting `capital_loss` from `capital_gain` to create `net_capital`
---

## 3. Unsupervised Learning
-  Create a Pipeline for Unsupervised Learning, including:
    - Extracting numerical features
    - Using VectorAssembler to combine numerical features
    - Using StandardScaler to scale numerical features before putting it to PCA
    - Using PCA to reduce dimensionality to 2D for visualization
---

## 4. Data Visualization
- Group data by education level, calculate the percentage of individuals earning >$50K, convert to an ordered Pandas categorical, and render a gradient-filled bar chart with percentage labels using plotnine
- Extract age and label columns to Pandas, converted labels to strings for discrete treatment, and generate a boxplot comparing age distributions across income classes with custom color mapping
- Aggregate counts by occupation and label, merged totals to compute high-income percentages, sorted occupations by percentage, apply an ordered categorical for proper ranking, and display a horizontal bar chart with coordinate flipping
---

## 5. Modeling and Prediction
- Split the dataset in 80/20 ratio
- Creating a Pipeline for Supervised Learning, including:
    - Applying One Hot Encoder for categorical features
    - Using VectorAssembler to combine all features
    - Scale the data
- Training Logistic Regression with hyperparameter tuning and cross-validation
- Training Random Forest with hyperparameter tuning, cross-validation and feature importance extraction
- Comparing the performance of 2 models