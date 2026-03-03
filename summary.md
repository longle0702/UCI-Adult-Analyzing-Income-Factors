# Summary of our approach:

## 1. Data Preprocessing
- Handle missing values by creating `Unknown` category for each categorical column.
- Remove redundancy of `education` and `education_num` by removing `education` column.
- Cleaning categorical columns by removing leading and trailing whitespaces.

## 2. Feature Engineering
- Transform `income` column to binary values (0 and 1).
- Creating new features by:
    - Grouping `native_country` variable into `US` and `Others`.
    - Creating `age_category` column based on `age`.
    - Substracting `capital_loss` from `capital_gain` to create `net_capital`.

## 3. Unsupervised Learning
-  Create a Pipeline for Unsupervised Learning, including:
    - Extracting numerical features
    - Using VectorAssembler to combine numerical features
    - Using StandardScaler to scale numerical features before putting it to PCA
    - Using PCA to reduce dimensionality to 2D for visualization

## 4. Data Visualization

## 5. Modeling and Prediction