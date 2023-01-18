The model code begins by importing the necessary packages, including the Sequential model and various
layer types from Keras.

Then, you can load the MNIST dataset.

Next, the model is defined using the Sequential model, which allows you to define a linear stack of layers
in the model. The model begins with two convolutional layers, which are responsible for learning features
from the input data. The first convolutional layer has 32 filters and a kernel size of 3x3, and uses the ReLU activation function. The second convolutional layer has 64 filters and a kernel size of 3x3, and also uses the ReLU activation function.

The convolutional layers are followed by a max pooling layer, which down samples the spatial dimensions
of the data by taking the maximum value over a window of the input. This helps to reduce the number of
parameters in the model and control overfitting.

The model also includes a dropout layer, which randomly sets a fraction of the input units to zero during
training in order to prevent overfitting.

After the convolutional and pooling layers, the data is flattened into a single vector and passed through
a fully-connected layer with 128 units and the ReLU activation function. The output of this layer is then
passed through a second dropout layer and a final dense layer with 10 units and the softmax activation
function, which is used for classification.

Finally, the model is compiled using the categorical cross-entropy loss function and the Adam
optimization algorithm, and is fit to the training data using the fit() function. The model is trained for 10 epochs, and the performance is evaluated on the test data after each epoch.

To test a trained model in Keras, we use the evaluate() function, which returns the loss value and any
metrics that you specified when you compiled the model.
