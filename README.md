# deep-learning-challenge

## Report on the Neural Network Model

### Deep Learning Charity Funding Outcome Predictor Project using hyper-tuned Neural Networks.

### Overview:

I've created a tool for the nonprofit foundation Alphabet Soup that can help it select applicants for funding with the best chance of success in their ventures. Using my knowledge of machine learning and neural networks, I have used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. We were set a target of 75% accuracy for our model. From Alphabet Soup’s business team, I received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as: * EIN and NAME—Identification columns * APPLICATION_TYPE—Alphabet Soup application type * AFFILIATION—Affiliated sector of industry * CLASSIFICATION—Government organization classification * USE_CASE—Use case for funding * ORGANIZATION—Organization type * STATUS—Active status * INCOME_AMT—Income classification * SPECIAL_CONSIDERATIONS—Special consideration for application * ASK_AMT—Funding amount requested * IS_SUCCESSFUL—Was the money used effectively.

### Steps Taken:

* Dataset was checked for null and duplicated values

* EIN and NAME—Identification columns removed from the input data because they are neither targets nor features

* Created cutoff point to bin "rare" categorical variables together in a new value, Other for both CLASSIFICATION and APPLICATION_TYPE 

* Converted categorical data to numeric with pd.get_dummies, split the preprocessed data into features and target arrays, then lastly split into training and tesing datasets 

Target Variable for the model: * IS_SUCCESSFUL Feature Variables for the model: * APPLICATION_TYPE * AFFILIATION * CLASSIFICATION * USE_CASE * ORGANIZATION * STATUS * INCOME_AMT * SPECIAL_CONSIDERATIONS * ASK_AMT

#### 2: Compiling, Training, and Evaluating the Model
I build the first model with the following parameters with low computation time in mind: * With an hidden layer activation function of relu as this our go to for first model.

#### Summary:
The final automatically optimized neural network trained model from the keras tuner method achieved 80% prediction accuracy with a 0.45 loss, using a sigmoid activation function with input node of 76; 5 hidden layers at a 16, 21, 26, 11, 21, neurons split and 50 training epochs. This shows the importance of the shape of your datasets before you preprocess it.