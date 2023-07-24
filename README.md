# deep-learning-challenge
Dataviz bootcamp

*Note: the TA helped with code on how to export to HDF5 file and where to find the file after saving it. The code she provided was nn_model.save(AlphabetSoupCharity.h5), which I adpoted it into my code. https://stackoverflow.com/questions/47418299/python-combining-low-frequency-factors-category-counts was also used to help with binning*

## Step 1: Preprocess the Data

Start by uploading the starter file to Google Colab

Read in the charity_data.csv to a Pandas DataFrame

Drop the EIN and NAME columns.

Determine the number of unique values for each column.

For columns that have more than 10 unique values, determine the number of data points for each unique value.

Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, and then check if the binning was successful.

Use pd.get_dummies() to encode categorical variables.

Split the preprocessed data into a features array, X, and a target array, y. Use these arrays and the train_test_split function to split the data into training and testing datasets.

Scale the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform function.

## Step 2: Compile, Train, and Evaluate the Model

Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.
Create the first hidden layer and choose an appropriate activation function.

If necessary, add a second hidden layer with an appropriate activation function.

Create an output layer with an appropriate activation function.

Check the structure of the model.

Compile and train the model.

Create a callback that saves the model's weights every five epochs.

Evaluate the model using the test data to determine the loss and accuracy.

Save and export your results to an HDF5 file. Name the file AlphabetSoupCharity.h5.

## Step 3: Optimize the Model

Using your knowledge of TensorFlow, optimize your model to achieve a target predictive accuracy higher than 75%.

Adjust the input data to ensure that no variables or outliers are causing confusion in the model, such as:

  Dropping more or fewer columns.
  
  Creating more bins for rare occurrences in columns.
  
  Increasing or decreasing the number of values for each bin.
  
  Add more neurons to a hidden layer.
  
  Add more hidden layers.
  
  Use different activation functions for the hidden layers.
  
  Add or reduce the number of epochs to the training regimen.

## Step 4: Write a Report on the Neural Network Model

For this part of the assignment, you’ll write a report on the performance of the deep learning model you created for Alphabet Soup.
