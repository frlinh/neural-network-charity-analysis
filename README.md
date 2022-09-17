# Neural Network Charity Analysis

## Overview of the Analysis
The purpose of this analysis is to use deep-learning neural networks to analyze and classify the success of charitable donations.
 
1) Preprocess the data for a neural network model  
2) Compile, train, and evaluate the model
3) Optimize the model for higher accuracy

## Resources
- Data Source: charity_data.csv
- Software: Google Colab, sklearn, tensorflow

## Neural Network Model

### Data Preprocessing
- Dropped the non-beneficial ID columns ```EIN``` and ```NAME```
- Visualized the value counts of ```APPLICATION_TYPE```

![count_app_type](https://github.com/frlinh/neural-network-charity-analysis/blob/839577d40e5b897ed5a0a6dc4ce77382b6439ddb/charity.fig.png)
- Generated a categorical variable list containing ```APPLICATION_TYPE```, ```AFFILIATION```, ```CLASSIFICATION```, ```USE_CASE```, ```ORGANIZATION```, ```INCOME_AMT```, and ```SPECIAL_CONSIDERATIONS```
- Used OneHotEncoder to fit and transform the variable list and added the encoded variable names to the dataframe
- Split preprocessed data into features and target arrays

![split](https://github.com/frlinh/neural-network-charity-analysis/blob/92ecc0703d6980c57c714bbea9a83da5635789f2/Resources/splitTrain.png)
- Assign ```IS_SUCCESSFUL``` as the x-variable

### Compiling, Training, and Evaluating the Model
- Defined the number of input features and hidden modes for each layer
![sequential](https://github.com/frlinh/neural-network-charity-analysis/blob/839577d40e5b897ed5a0a6dc4ce77382b6439ddb/sequentialModel.png)
- Compiled, trained, and evaluate the model

The initial Neural Network Model accuracy was 73%.

![nnModel](https://github.com/frlinh/neural-network-charity-analysis/blob/839577d40e5b897ed5a0a6dc4ce77382b6439ddb/nnModel.png)

### Optimize the Neural Network Model
Optimized the neural network model accuracy by adding more data to train the model.
The following steps were applied:
- Increased the application count from 500 to 750

![appCount](https://github.com/frlinh/neural-network-charity-analysis/blob/18957a009dd653c0b6811353cce18fbad7fb4927/Resources/appCount.png)
- Increased the classification count from 1000 to 1500

![classCount](https://github.com/frlinh/neural-network-charity-analysis/blob/18957a009dd653c0b6811353cce18fbad7fb4927/Resources/classCount.png)
- Added test_size=128 to the test statement

![splitOpt](https://github.com/frlinh/neural-network-charity-analysis/blob/92ecc0703d6980c57c714bbea9a83da5635789f2/Resources/splitTrainOpt.png)
- Changed the node hidden layer values

![sequentialModelOpt](https://github.com/frlinh/neural-network-charity-analysis/blob/92ecc0703d6980c57c714bbea9a83da5635789f2/Resources/sequentialModelOpt.png)

The optimized Neural Network Model accuracy improved to 76.6%.

![nnModelOpt](https://github.com/frlinh/neural-network-charity-analysis/blob/92ecc0703d6980c57c714bbea9a83da5635789f2/Resources/nnModelOpt.png)
