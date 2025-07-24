# Kaggle Competition - [Spaceship Titanic]

This repository contains my work for the [Competition Name](https://www.kaggle.com/competitions/spaceship-titanic) on Kaggle.

---

## Competition Description
A short summary of the competition:
- Goal: Predict which passengers were transported to an alternate dimension.
- Evaluation metric: Accuracy.
- Data: Contains train.csv and test.csv with train.csv containing 14 columns and test.csv containing 13 columns (no target column). For more information on the data, check out the [data page](https://www.kaggle.com/competitions/spaceship-titanic/data) on the Kaggle page for the competition.

---

## Approach
- **Data Preprocessing:** Created new features like "GroupId" and "PassengerNumber" from "PassengerId", "Deck", "Num", and "Side" from "Cabin", and "TotalExpenses" from the ammenities columns. I also handled missing values using KNNImputer and the fillna() function provided by pandas. I also did extra feature engineering such as one-hot encoding for categorical features and also finding the correlations between the features and the target, to create new features that combine the best 4 boolean values. 
- **Models:** Tried out models like Random Forest, XGB Boosting, and Gradient Boosting and choose the best performing model after training with the removal of different combinations of features that needed to be tested since they had low correlation. 
- **Validation:** Used cross-validation to effectively train the models and then fitted the data to the best performing model. 

---

## Files
- `notebooks/` - Jupyter notebook that includes the data preprocessing and classification code.
- `data/` - Training and testing data for the classification.

---

## Usage
To reproduce results:
```bash
# Clone the repository
git clone https://github.com/cpicazo8304/Spaceship-Titanic-Classification.git
cd Spaceship-Titanic-Classification


# Install dependencies
pip install -r requirements.txt

# Run the notebook or script
jupyter notebook notebooks/spaceship-titanic-passenger-classification.ipynb
