# Titanic-Classification
Make a system which tells whether the person will be save  from sinking. What factors were most likely lead to success- socio-economic status, age, gender and more.

The provided Python script is used to perform binary classification on the Titanic dataset to predict whether passengers survived or did not survive the Titanic disaster. Here's a general description of the script's main steps:

1. Data Loading and Preprocessing:
   - The script imports the required libraries, including pandas, LabelEncoder, train_test_split, DecisionTreeClassifier, tree, and matplotlib.
   - It reads the Titanic dataset from a specified URL.
   - The script checks for missing values in the dataset and handles them by dropping the 'Cabin' column (which has many missing values) and removing rows with missing values in other columns.
   - The 'Sex' column is encoded from categorical values ('male' and 'female') to numerical values (0 and 1) using LabelEncoder.

2. Feature Selection and Target Variable:
   - The script selects specific features ('Pclass', 'Sex', 'Age', 'SibSp', 'Parch', 'Fare') as input variables (X) for the classification model.
   - The target variable ('Survived') is defined as the variable to predict (y), indicating whether a passenger survived (1) or did not survive (0).

3. Train-Test Split:
   - The data is split into a training set (80%) and a testing set (20%) using the `train_test_split` function. This allows for model training and subsequent evaluation.

4. Decision Tree Model Training:
   - A Decision Tree classifier is created with a maximum depth of 3, limiting the tree's complexity.
   - The Decision Tree classifier is trained on the training dataset using the `fit` method.

5. Tree Visualization:
   - The script visualizes the trained Decision Tree using `tree.plot_tree`. The resulting plot displays the structure of the decision tree, including decision nodes and leaf nodes, along with the associated decision rules and class predictions.

6. Model Evaluation:
   - The accuracy of the trained Decision Tree classifier is calculated and printed using the `score` method on the testing set. This accuracy score indicates how well the model performs in predicting whether passengers survived or not.

In summary, this script demonstrates a basic implementation of a Decision Tree classifier for binary classification using the Titanic dataset. It preprocesses the data, trains the model, visualizes the decision tree, and evaluates its performance in predicting passenger survival outcomes.
