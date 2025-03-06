# Titanic Survival Prediction Using Machine Learning

This project uses machine learning to predict passenger survival on the Titanic based on various features such as age, sex, class, and embarkation point. The dataset used is the Titanic dataset provided by Kaggle.

## Dataset
The dataset used for this project is `train.csv`, which contains information about passengers, including:
- `PassengerId`: Unique identifier for each passenger.
- `Survived`: Survival status (0 = No, 1 = Yes).
- `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd).
- `Name`: Passenger's name.
- `Sex`: Gender of the passenger.
- `Age`: Age of the passenger.
- `SibSp`: Number of siblings/spouses aboard.
- `Parch`: Number of parents/children aboard.
- `Ticket`: Ticket number.
- `Fare`: Passenger fare.
- `Cabin`: Cabin number.
- `Embarked`: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

## Dependencies
This project requires the following Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`


## Data Preprocessing
1. Load the dataset using `pandas`.
2. Handle missing values:
   - Drop the `Cabin` column due to excessive missing values.
   - Fill missing `Age` values with the mean age.
   - Fill missing `Embarked` values with the most common value (mode).
3. Convert categorical variables into numerical values:
   - `Sex`: Male = 0, Female = 1.
   - `Embarked`: S = 0, C = 1, Q = 2.
4. Drop unnecessary columns (`PassengerId`, `Name`, `Ticket`, `Cabin`).

## Exploratory Data Analysis (EDA)
- Countplots for `Sex`, `Pclass`, and `Survived` using `seaborn`.
- Value counts for categorical variables.

## Model Training
- The dataset is split into training and testing sets (80%-20%).
- A **Logistic Regression** model is trained using `scikit-learn`.
- The accuracy of the model is evaluated on both training and testing data.

## Results
The accuracy scores for training and test data are printed to assess model performance.

## Usage
Run the script in a Jupyter Notebook or a Python environment like Google Colab. Ensure that the `train.csv` dataset is available in the working directory.



