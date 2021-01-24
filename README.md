# Weights-Initialization-in-Nueral-Networks
Weight Initialization Techniques in Neural Networks

•	Weight initialization: 
•	Building a basic neural network is bit confusing,  on top of it tuning it to get better results is much more tedious job, but the first step that comes into consideration was initialising parameters. If this part is done correctly then optimization can be achieved in minimum time or else converging to minima using Gradient Descent will be difficult.

Neural network: First let’s understand how neural network to understand how weights work. Within a neural network there's an input layer that takes the input signals and passes them to the next layer.

Next, the neural network contains a series of hidden layers which apply transformations to the input data. It is within the nodes of the hidden layers that the weights are applied. For example, a single node may take the input data and multiply it by an assigned weight value, then add a bias before passing the data to the next layer.
The final layer of the neural network is also known as the output layer. The output layer often tunes the inputs from the hidden layers to produces the desired numbers in a specified range.
Weight vs. Bias:
 Weights and bias are both learnable parameters inside the network. A teachable neural network will randomize both the weight and bias values before learning initially begins. As training continues, both parameters are adjusted toward the desired values and the correct output. Weights, on the other hand, can be thought of as the strength of the connection. Weight affects the amount of influence a change in the input will have upon the output. A low weight value will have no change on the input, and alternatively a larger weight value will more significantly change the output.

Bias: A low bias suggests that the network is making more assumptions about the form of the output, whereas a high bias value makes less assumption about the form of the output.

Activation functions:
Forward and backward propagation etc.

Random : Assigning random values to weights is better than just 0 assignment.  If weights are initialized high values or very low values and what is a reasonable initialization of weight values.
•	a) If weights are initialized with very high values the term np.dot(W,X)+b becomes significantly higher and if an activation function like sigmoid() is applied, the function maps its value near to 1 where the slope of gradient changes slowly and learning takes a lot of time.

•	b) If weights are initialized with low values it gets mapped to 0, where the case is the same as above.
•	This problem is often referred to as the vanishing gradient.

Xavier's / Glorot's
He's initialization: we just simply multiply random initialization with 
Lets take a dataset of size 15000 iterations, loss less , more accuracy
	Normal Distribution
	Uniform Distribution


•	Vanishing Gradient Problem / Exploding Gradient Problem
1.	Exploding Gradient
a.	Weights might be randomly initialized with values > 1
2.	Vanishing Gradient
a.	If the weights initialized are less than 1 then quickly the outputs of neurons in subsequent layers vanish to zero
•	Overcome this challenge by batch normalization
Overfitting: When train accuracy and test accuracy diverge that’s called overfitting 
Regularization Techniques
	 Early Stopping
	Error-change criterion: when error isn’t drooping over a window lets say 10 epochs
	Weight-change criterion: take max of all weights if that max weight is less than specific number then we stop running model. 
	If weight is more than specific number then we continue running model.
•	Drop Out: Randomly few neurons are ignored for every hidden layer. You define on how many neurons should be ignored as part of each and every training sample.
	Drop Connect: Drop connection itself.
	Weight Decay
	L1 regularization: A regression model that uses L1 regularization technique is called Lasso Regression
Lasso Regression (Least Absolute Shrinkage and Selection Operator) adds “absolute value of magnitude” of coefficient as penalty term to the loss function.
•	 
Cost function
Again, if lambda is zero then we will get back OLS whereas very large value will make coefficients zero hence it will under-fit.
L2 regularization: model which uses L2 is called Ridge Regression
Ridge regression adds “squared magnitude” of coefficient as penalty term to the loss function. Here the highlighted part represents L2 regularization element.
•	 
Cost function
Here, if lambda is zero then you can imagine we get back OLS. However, if lambda is very large then it will add too much weight and it will lead to under-fitting. Having said that it’s important how lambda is chosen. This technique works very well to avoid over-fitting issue.
•	Noise
	Data Noise : Adding noise to data
	Label Noise: Adding noise to output labels
	Gradient Noise: each gradient 
Data Manipulation Techniques:
	Data Transformation
	Batch Normalization
	Add batch normalization layer between Fully connected network (dense network) & Activation layer
	Shuffling Inputs
	Curriculum Learning
	Data Augmentation
o	Covariate Shift
o	Correlation between Inputs - Collinearity Problem

