## Deep Learning

[Deep Learning (Keras)](https://machinelearningmastery.com/start-here/#deeplearning)

[Better Deep Learning Performance](https://machinelearningmastery.com/start-here/#better)

[How To Improve Deep Learning Performance](https://machinelearningmastery.com/improve-deep-learning-performance/)

[How to Choose Loss Functions When Training Deep Learning Neural Networks](https://machinelearningmastery.com/how-to-choose-loss-functions-when-training-deep-learning-neural-networks/)

[Understand the Impact of Learning Rate on Neural Network Performance](https://machinelearningmastery.com/understand-the-dynamics-of-learning-rate-on-deep-learning-neural-networks/)


## Challenge of Training Deep Learning Neural Networks

[A Gentle Introduction to the Challenge of Training Deep Learning Neural Network Models](https://machinelearningmastery.com/a-gentle-introduction-to-the-challenge-of-training-deep-learning-neural-network-models/)

### Neural Networks Learn a Mapping Function

Deep learning neural networks learn a _mapping function_. 

Developing a model requires historical data from the domain that is used as training data which is comprised of observations or examples from the domain with input elements that describe the conditions and an output element that captures what the observation means.

- A problem where the output is a quantity would be described generally as a regression predictive modeling problem. 

- A problem where the output is a label would be described generally as a classification predictive modeling problem.

A neural network model uses the examples to learn how to map specific sets of input variables to the output variable. 

The NN must learn the mapping in such a way that this mapping works well for the training dataset but also works well on new examples not seen by the model during training which is called _generalization_. 


We can describe the relationship between the input variables and the output variables as a complex mathematical function. 

For a given model problem, we must believe that a true mapping function exists to best map input variables to output variables and that a neural network model can do a reasonable job at approximating the true unknown underlying mapping function.

Thus, we can describe the broader problem that neural networks solve as _function approximation_. 

A NN learns to approximate an unknown underlying mapping function given a training dataset by learning weights and the model parameters, given a specific network structure that we design.

However, finding the parameters for neural networks in general is hard.

In fact, training a neural network is the most challenging part of using the technique.

The use of nonlinear activation functions in the neural network means that the optimization problem that we must solve in order to find model parameters is not convex.

Solving this optimization is challenging, not least because the error surface contains many local optima, flat spots, and cliffs.


### Navigating the Non-Convex Error Surface

A NN model has a specific set of weights can be evaluated on the training dataset and the average error over all training datasets can be thought of as the error of the model. 

A change to the model weights will result in a change to the model error. Therefore, we seek a set of weights that result in a model with a small error.

The process involves repeating the steps of evaluating the model and updating the model parameters in order to step down the error surface which is repeated until a set of parameters is found that is good enough or the search process gets stuck.

Thus, the process is a search or an optimization and we refer to optimization algorithms that operate in this way as gradient optimization algorithms sonce they naively follow along the error gradient. In practice, this is more art than science.

The algorithm that is most commonly used to navigate the error surface is called stochastic gradient descent (SGD).

Other global optimization algorithms designed for non-convex optimization problems could be used, such as a genetic algorithm but stochastic gradient descent is more efficient since it uses the gradient information specifically to update the model weights via an algorithm called _backpropagation_.

Backpropagation refers to a technique from calculus to calculate the derivative (e.g. the slope or the gradient) of the model error for specific model parameters which allows the model weights to be updated to move down the gradient.

### Components of the Learning Algorithm

Training a deep learning neural network model using stochastic gradient descent with backpropagation involves choosing a number of components and hyperparameters:

- Loss Function: The function used to estimate the performance of a model with a specific set of weights on examples from the training dataset.

- Weight Initialization: The procedure by which the initial small random values are assigned to model weights at the beginning of the training process.

- Batch Size: The number of examples used to estimate the error gradient before updating the model parameters.

- Learning Rate: The amount that each model parameter is updated per cycle of the learning algorithm.

- Epochs. The number of complete passes through the training dataset before the training process is terminated.


### Decrease Neural Network Size and Maintain Accuracy

[Decrease Neural Network Size and Maintain Accuracy](https://towardsdatascience.com/decrease-neural-network-size-and-maintain-accuracy-knowledge-distillation-6efb43952f9d)

Some neural networks are too big to use. There is a way to make them smaller but keep their accuracy.

1. Pruning
2. Knowledge distillation


