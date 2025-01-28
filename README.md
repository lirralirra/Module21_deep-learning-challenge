# Module21_deep-learning-challenge

## Neural Network Model Report: Alphabet Soup

Overview of the Analysis

The purpose of this analysis was to build a deep learning model to predict whether applicants for funding by Alphabet Soup 
are likely to be successful. Using a dataset of historical funding data, the model aimed to identify key patterns and 
predict outcomes based on applicant characteristics. This can help streamline decision-making and allocate 
resources more effectively.

## Results

Data Preprocessing

### Target Variable:

The target variable for the model is the IS_SUCCESSFUL column, which indicates whether a funding application was successful (1) or not (0).

### Features:

The feature variables include the remaining columns after preprocessing, such as:

APPLICATION_TYPE

AFFILIATION

CLASSIFICATION

USE_CASE

ORGANIZATION

INCOME_AMT

ASK_AMT

categorical variables converted into dummy variables via one-hot encoding.

### Removed Variables:

Variables that were removed because they are neither features nor targets:

EIN and NAME—Identification columns

### Compiling, Training, and Evaluating the Model

Neurons, Layers, and Activation Functions:

The neural network model consisted of:

Input Layer: Matching the number of input features after one-hot encoding (~40 features).

Hidden Layers:

Layer 1: 80 neurons with ReLU activation to handle complex relationships.

Layer 2: 40 neurons with ReLU activation to further refine patterns.

Output Layer: 1 neuron with a sigmoid activation function for binary classification.

Rationale: ReLU was selected for the hidden layers due to its efficiency in avoiding vanishing gradients, 
and sigmoid was used in the output layer as it is appropriate for binary classification problems.
Model Performance:

The target model accuracy was set at 75%.

The achieved accuracy was approximately 72%, falling slightly short of the goal.


### Steps to Improve Performance:

Adjusted the number of neurons and layers to balance complexity and overfitting.

Tested different batch sizes (e.g., 32, 64) and epochs (e.g., 50, 100, 200).

Applied dropout regularization to reduce overfitting.

Normalized input data to improve convergence.

Explored additional feature engineering by grouping certain categories.
