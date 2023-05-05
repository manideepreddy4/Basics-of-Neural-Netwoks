# Basics-of-Neural-Netwoks

Variants of Activation Function 
Linear Function 
Equation : Linear function has the equation similar to as of a straight line i.e. y = x
No matter how many layers we have, if all are linear in nature, the final activation function of last layer is nothing but just a linear function of the input of first layer.
Range : -inf to +inf
Uses : Linear activation function is used at just one place i.e. output layer.
Issues : If we will differentiate linear function to bring non-linearity, result will no more depend on input “x” and function will become constant, it won’t introduce any ground-breaking behavior to our algorithm.
For example : Calculation of price of a house is a regression problem. House price may have any big/small value, so we can apply linear activation at output layer. Even in this case neural net must have any non-linear function at hidden layers. 

## Sigmoid Function 
![image](https://user-images.githubusercontent.com/126583779/236363101-2596ab43-594f-4e94-9c95-662011686ccd.png)
 

It is a function which is plotted as ‘S’ shaped graph.                                    
Equation : A = 1/(1 + e-x)                                               
Nature : Non-linear. Notice that X values lies between -2 to 2, Y values are very steep. This means, small changes in x would also bring about large changes in the value of Y.
Value Range : 0 to 1                                        
Uses : Usually used in output layer of a binary classification, where result is either 0 or 1, as value for sigmoid function lies between 0 and 1 only so, result can be predicted easily to be 1 if value is greater than 0.5 and 0 otherwise.

## Tanh Function 

![image](https://user-images.githubusercontent.com/126583779/236363549-d3a55e0c-e51e-4dcc-ba52-482f3b7e3426.png)
 

The activation that works almost always better than sigmoid function is Tanh function also known as Tangent Hyperbolic function. It’s actually mathematically shifted version of the sigmoid function. Both are similar and can be derived from each other.
Equation :-

 ![image](https://user-images.githubusercontent.com/126583779/236363562-895ad397-d375-4b3d-8afe-bf31b991b31f.png)


Value Range :- -1 to +1                                
Nature :- non-linear                                
Uses :- Usually used in hidden layers of a neural network as it’s values lies between -1 to 1 hence the mean for the hidden layer comes out be 0 or very close to it, hence helps in centering the data by bringing mean close to 0. This makes learning for the next layer much easier.
## RELU Function 

 ![image](https://user-images.githubusercontent.com/126583779/236363572-d2779d3b-4e71-4fe1-aa43-ac38dc99cedf.png)


It Stands for Rectified linear unit. It is the most widely used activation function. Chiefly implemented in hidden layers of Neural network.
Equation :- A(x) = max(0,x). It gives an output x if x is positive and 0 otherwise.                                  
Value Range :- [0, inf)                                                       
Nature :- non-linear, which means we can easily backpropagate the errors and have multiple layers of neurons being activated by the ReLU function.
Uses :- ReLu is less computationally expensive than tanh and sigmoid because it involves simpler mathematical operations. At a time only a few neurons are activated making the network sparse making it efficient and easy for computation.
In simple words, RELU learns much faster than sigmoid and Tanh function.     

## Leaky ReLU
It is an attempt to solve the dying ReLU problem                   
![image](https://user-images.githubusercontent.com/126583779/236363526-35b08100-d425-43a0-8a96-2d29d50b17f9.png)


Fig : ReLU v/s Leaky ReLU                    
Can you see the Leak? 😆                                                                                    

The leak helps to increase the range of the ReLU function. Usually, the value of a is 0.01 or so.                         

When a is not 0.01 then it is called Randomized ReLU.                                    

Therefore the range of the Leaky ReLU is (-infinity to infinity).                   

Both Leaky and Randomized ReLU functions are monotonic in nature. Also, their derivatives also monotonic in nature.

## Softmax Function

 ![image](https://user-images.githubusercontent.com/126583779/236363597-f019768f-7a95-40f3-be8a-fb7019aead9e.png)


The softmax function is also a type of sigmoid function but is handy when we are trying to handle multi- class classification problems.

Nature :- non-linear                                                      
Uses :- Usually used when trying to handle multiple classes. the softmax function was commonly found in the output layer of image classification problems.The softmax function would squeeze the outputs for each class between 0 and 1 and would also divide by the sum of the outputs. 
Output:- The softmax function is ideally used in the output layer of the classifier where we are actually trying to attain the probabilities to define the class of each input.

The basic rule of thumb is if you really don’t know what activation function to use, then simply use RELU as it is a general activation function in hidden layers and is used in most cases these days.

If your output is for binary classification then, sigmoid function is very natural choice for output layer.                              

If your output is for multi-class classification then, Softmax is very useful to predict the probabilities of each classes. 
