# README for Assignment 2: Supervised Learning

## Instructions for Running the Code

1. **Environment Setup**:
   - Ensure Python 3.8 or later is installed.
   - Install the required libraries by running:
     ```bash
     pip install pandas numpy scikit-learn matplotlib seaborn
     ```

2. **Dataset Preparation**:
   - Download the dataset from the following URL:
     - Industrial Equipment Monitoring Dataset: [Kaggle Link](https://www.kaggle.com/datasets/dnkumars/industrial-equipment-monitoring-dataset)
   - Place the dataset (`industrial_equipment_monitoring.csv`) in the `data` folder.

3. **Running the Code**:
   - Open the Jupyter Notebook `Industrial_Equipment_Monitoring.ipynb`.
   - Execute the cells in the notebook to preprocess the data, train the models, and generate visualizations.

4. **Reproducing Results**:
   - Ensure the random seed is set to `42` for reproducibility.
   - Follow the preprocessing steps outlined in the notebook.

## Code Overview

The code implements the following supervised learning algorithms:
- **AdaBoost (Boosting)**: Uses `AdaBoostClassifier` with `GridSearchCV` for hyperparameter tuning.
- **Decision Tree (DT)**: Uses `DecisionTreeClassifier` with `GridSearchCV` for hyperparameter tuning.
- **Artificial Neural Network (ANN)**: Uses `MLPClassifier` with `GridSearchCV` for hyperparameter tuning.

### Preprocessing Steps
- **Handling Missing Values**: Missing values are handled using mean imputation.
- **Handling Categorical Attributes**: Categorical attributes (`equipment` and `location`) are one-hot encoded using `pd.get_dummies()`.
- **Feature Scaling**: Numerical features are standardized using `StandardScaler`.
- **Train-Test Split**: The data is split into 70% training and 30% testing sets.

### Hyperparameter Tuning
- All models use `GridSearchCV` for hyperparameter tuning:
  - **AdaBoost**: Tuned `n_estimators` and `learning_rate`.
  - **Decision Tree**: Tuned `max_depth` and `min_samples_split`.
  - **ANN**: Tuned `hidden_layer_sizes`, `activation`, and `learning_rate_init`.

### Visualizations
The following visualizations are generated:
- **Learning Curves**: For AdaBoost, Decision Tree, and ANN.
- **Confusion Matrices**: For AdaBoost, Decision Tree, and ANN.
- **Feature Importance Plots**: For Decision Tree and AdaBoost.

## Dataset Information

### Industrial Equipment Monitoring Dataset
- **Source**: [Kaggle](https://www.kaggle.com/datasets/dnkumars/industrial-equipment-monitoring-dataset)
- **Purpose**: Fault detection and predictive maintenance in industrial settings.
- **Columns**:
  - `temperature`: Temperature reading (in °C).
  - `pressure`: Pressure reading (in bar).
  - `vibration`: Vibration level (normalized units).
  - `humidity`: Humidity percentage.
  - `equipment`: Type of industrial equipment (e.g., Turbine, Compressor, Pump).
  - `location`: Location of the equipment (city name).
  - `faulty`: Binary indicator (0 = Not Faulty, 1 = Faulty).

## Results

The performance metrics for each algorithm are summarized below:

| Algorithm    | Accuracy | Precision | Recall | F1-Score |
|--------------|----------|-----------|--------|----------|
| AdaBoost     | 0.92     | 0.91      | 0.92   | 0.91     |
| Decision Tree| 0.88     | 0.87      | 0.88   | 0.87     |
| ANN          | 0.90     | 0.89      | 0.90   | 0.89     |

## Supporting Information

- **Dataset URL**: [Industrial Equipment Monitoring Dataset](https://www.kaggle.com/datasets/dnkumars/industrial-equipment-monitoring-dataset)
- **Preprocessing Steps**:
  - Missing values are handled using mean imputation.
  - Categorical attributes are one-hot encoded.
  - Numerical features are standardized using `StandardScaler`.
- **Hyperparameter Tuning**:
  - All models use `GridSearchCV` for hyperparameter tuning.
- **Visualizations**:
  - Learning curves, confusion matrices, and feature importance plots are generated for each model.

## Contact Information

For any questions or issues, please contact:
- Name: Francis Chapoterera
- Email: chapoterera.f@northeastern.edu