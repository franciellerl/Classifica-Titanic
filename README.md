[![English](https://img.shields.io/badge/lang-EN-blue)](README.md)
[![Português](https://img.shields.io/badge/lang-PT--BR-white)](README.br.md)

# Titanic Classification

Data Science pipeline applied to exploratory data analysis and passenger survival classification on the Titanic dataset. This project was developed to apply data preprocessing techniques, exploratory analysis, and supervised learning using Decision Trees to predict passenger survival based on socioeconomic and demographic characteristics.

The dataset used is derived from the classic Titanic dataset, widely adopted in Machine Learning studies for binary classification problems.

### Project Structure

```text
Titanic-Classification/
├── analise_e_classificacao_titanic.ipynb
├── train.csv
├── validation.csv
└── result.csv
```

# Stages

**Stage 1 - Exploratory Data Analysis:**

Initial analysis of the dataset to understand passenger characteristics and identify patterns relevant to the classification task.

What was performed:

* Missing value analysis;
* Passenger age distribution;
* Survival analysis by passenger class;
* Exploration of available variables;
* Identification of potential relationships between features and survival.

**Stage 2 - Data Preprocessing:**

Preparation of the dataset for Machine Learning model training.

What was performed:

* Selection of the most relevant features;
* Removal of variables with low predictive potential;
* Conversion of categorical attributes into numerical values using Label Encoding;
* Missing value treatment;
* Standardization of training and validation datasets.

Features used:

* Passenger Class (`Pclass`);
* Sex (`Sex`);
* Age (`Age`);
* Number of Siblings/Spouses (`SibSp`);
* Number of Parents/Children (`Parch`);
* Fare (`Fare`);
* Port of Embarkation (`Embarked`).

**Stage 3 - Model Training:**

Development of a supervised learning model for passenger survival classification.

What was performed:

* Train-test split;
* Training using a Decision Tree Classifier;
* Model parameter tuning;
* Performance evaluation on unseen data.

**Stage 4 - Evaluation and Prediction:**

Assessment of predictive performance and classification of unseen records.

What was performed:

* Training accuracy calculation;
* Test accuracy calculation;
* Generation of predictions for the validation dataset;
* Export of results to a CSV file.

**Stage 5 - Model Interpretation:**

Visualization of the decision structure learned by the algorithm.

What was performed:

* Graphical representation of the Decision Tree;
* Export of learned decision rules;
* Interpretation of the criteria used to predict survival.

# Examples

* Age Distribution:

```python
sns.histplot(trainData["Age"], bins=20, kde=True)
```

* Survival by Passenger Class:

```python
sns.countplot(x="Pclass", hue="Survived", data=trainData)
```

* Generated Decision Tree:

```python
plot_tree(model, feature_names=features, filled=True)
```

# Tools Used

* `pandas`: data manipulation and preprocessing;
* `matplotlib`: data visualization;
* `seaborn`: exploratory analysis and statistical graphics;
* `scikit-learn`: model training and evaluation;
* `Jupyter Notebook`: development and documentation of the analytical workflow.

# Applied Data Science Concepts

* Exploratory Data Analysis (EDA);
* Missing Data Treatment;
* Feature Engineering;
* Categorical Variable Encoding;
* Supervised Learning;
* Binary Classification;
* Decision Trees;
* Model Evaluation using Accuracy.
