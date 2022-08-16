# TASK 4 - Under The Hood!

## About the Task
I have implemented a single neural network. It is a multi-class classification neural network with a single hidden layer. I have used only NumPy, Pandas and Matplotlib libraries to implement this algorithm.

## Data
The training data is present in the file `Surgical-deepnet.csv`.

This dataset was taken from Kaggle. To know more [click here](https://www.causeweb.org/tshs/datasets/Surgery%20Timing%20Data%20Dictionary.pdf).

## Approach
First I have uploaded the data using Pandas DataFrame and created the training data. Then I made a class to setup the network.

To initialize the network you can give input of learning rate, the number of nodes in the hidden layer (more the depth of the hidden layer, more the accuracy - but the running time of the code also increases!) and the number of iterations you want to carry out.

The dimensions for the various matrices are stored in a list `d a jims`. The weights and biases for each layer of the network(input layer, hidden layer and output layer) is stored in a dictoniory `param`. The dictionary `ch` stores the cached parameters which are later used in the back propagation step. The forwards function takes are initializing my data `tanh` and `sigmoid`. I used the Cross Entropy Loss Fucntion to calculate the loss at each iteration and update the parameters automaticlly.

<!-- Here is some maths behind the algorithm - 

For one example $x^{(i)}$:
$$z^{[1] (i)} =  W^{[1]} x^{(i)} + b^{[1]}\tag{1}$$ 
$$a^{[1] (i)} = \tanh(z^{[1] (i)})\tag{2}$$
$$z^{[2] (i)} = W^{[2]} a^{[1] (i)} + b^{[2]}\tag{3}$$
$$\hat{y}^{\(i\)} = a^{\[2\]\(i\)} = \sigma(z^{\[2\]\(i\)})\tag{4}$$
$$y^{\(i\)}_{prediction} = \begin{cases} 1 & \mbox{if} a^{\[2\]\(i\)} > 0.5 \\ 0 & \mbox{otherwise} \end{cases}\tag{5}$$

Given the predictions on all the examples, you can also compute the cost $J$ as follows: 
$$J = - \frac{1}{m} \sum\limits_{i = 0}^{m} \large\left(\small y^{\(i\)}\log\left(a^{\[2\] \(i\)}\right) + (1-y^{\(i\)})\log\left(1- a^{\[2\] \(i\)}\right)  \large  \right) \small \tag{6}$$ -->

I tried running the code for many values of learning rate, number of iterations and the depth of the hidden layer.

I found the best result for `learning rate = 0.02`, `number of iterations = 5000` and `number of nodes in hidden layer = 30`
