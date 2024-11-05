# Rice Seed Classification Model Using Supervised Machine Learning

## Overview
This project aims to develop a Rice Seed Classification Model using supervised machine learning techniques to accurately classify rice types based on their physical characteristics. By employing various algorithms, including decision trees, support vector machines, and ensemble methods, this system identifies patterns and relationships in the rice seed data to make reliable predictions on unseen samples. The successful implementation of this model promises to enhance the efficiency of the rice supply chain and improve product quality assessment.

## Dataset
The dataset contains various attributes that characterize each rice sample. These attributes include measurements related to size, shape, and other geometric properties, making them suitable for distinguishing between different rice types.

### Dataset Attributes
- **Area**: Surface area of the rice seed
- **MajorAxisLength**: Length of the major axis of the rice seed
- **Eccentricity**: Measure of the roundness of the rice seed
- **ConvexArea**: Area of the convex hull of the rice seed
- **EquivDiameter**: Diameter of a circle with the same area as the rice seed
- **Extent**: Ratio of the area to the bounding box area
- **Perimeter**: Perimeter length of the rice seed
- **Roundness**: Measure of how close the rice seed shape is to a perfect circle
- **AspectRatio**: Ratio of the major axis to the minor axis

## Exploratory Data Analysis (EDA) & Data Visualization

To understand the distribution of features and relationships between different attributes in the rice dataset, we conducted Exploratory Data Analysis (EDA) and visualized key patterns.

### EDA Steps
1. **Summary Statistics**: 
   - Calculated the mean, median, min, max, and standard deviation of each attribute to understand their range and central tendency.
   
2. **Correlation Matrix**:
   - Examined correlations between features such as Area, Perimeter, and MajorAxisLength to identify strongly correlated attributes.
   - Displayed the correlation matrix as a heatmap to visualize attribute relationships.

3. **Distribution Plots**:
   - Used histograms to check the distribution of attributes like Area and ConvexArea, identifying any skewness or outliers.
   
4. **Box Plots**:
   - Created box plots to visualize the spread and identify outliers in attributes such as Eccentricity and Roundness.

5. **Pair Plots**:
   - Generated pairwise scatter plots to explore relationships between pairs of attributes and identify clustering patterns.

### Visualizations
- **Histogram**: Displayed the distribution of Area, ConvexArea, and Perimeter attributes.
- **Heatmap**: Correlation heatmap to visualize the relationship between features.
- **Box Plot**: Box plots for MajorAxisLength and Eccentricity to identify outliers and data spread.
- **Pair Plot**: Pair plots to observe clustering patterns for different classes.

These visualizations and analyses help us gain insights into the data, which guide model selection and feature engineering decisions.

## Approach
1. **Data Preprocessing**:
   - Processed and cleaned the dataset, ensuring all attributes were in a suitable format.
   - Normalized feature values to optimize model performance.

2. **Feature Selection**:
   - Selected key attributes (e.g., Area, Perimeter, MajorAxisLength, etc.) relevant to distinguishing rice types.

3. **Model Training**:
   - Utilized various supervised machine learning models, including:
     - **Decision Trees**
     - **Support Vector Machines (SVM)**
     - **Random Forest**
     - **Logistic Regression**
     - **Gradient Boosting**
     - **AdaBoost**
     - **XGBoost**
   - Trained each model on labeled rice samples to classify the type of rice seed accurately.

4. **Hyperparameter Tuning**:
   - Used **GridSearchCV** to optimize the hyperparameters for models like SVM, achieving the best accuracy score.

## Model Performance
The performance of each model was evaluated based on classification accuracy:

| Model                            | Accuracy |
|----------------------------------|----------|
| Best SVM (GridSearchCV)          | 0.9904   |
| Support Vector Machine           | 0.9901   |
| Gradient Boosting                | 0.9901   |
| AdaBoost                         | 0.9896   |
| Decision Tree (max_depth=5)      | 0.9887   |
| Random Forest (n_estimators=10)  | 0.9887   |
| Logistic Regression              | 0.9881   |
| XGBoost                          | 0.9876   |
| Logistic Regression (C=0.1)      | 0.9851   |
| Logistic Regression (random=10)  | 0.9848   |
| Decision Tree                    | 0.9846   |
| Random Forest                    | 0.9846   |

### Conclusion
- The evaluation of various machine learning models for rice classification demonstrates strong performance across all models, with accuracies ranging between 98% and 99%.
- Consistent accuracy across different models and minimal differences between training and test accuracies indicate that the models are not overfitted.
- **SVM (GridSearchCV Hyperparameter)** stands out as the most effective model, achieving the highest accuracy of 0.9904, making it ideal for this classification task.

