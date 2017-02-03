# Neural Networks made Easy
### How to add Neural Nets to your Data Science Toolbox
In many ways neural nets represent the future of machine learning because they can make more "intelligent" decisions than traditional learning algorithms. However the sophistication of these tools tend to make them seem too complicated and unaccessable by even season data scientists. This post will hopefully change your mind and show you that even deep neural nets can be implemented in a matter of minutes.

### What is a neural net and what are those pictures?
A neural net is a machine that takes some input and provides some output. Every neural net has an input layer and output layer, which can be separated by several "hidden" layers. These layers are called hidden because you can not directly observe what is going into or out of them. Some sophisticated neural nets will have several hidden layers which make them fall under the realm of deep learning.

<img src="../nn_diagram.png" width="400px">

### What is a neural net doing?

This is a common question and the answer is understandable by anyone who knows how to do some basic linear algebra. Just like any other machine learning algorithm neural networks take an input vector of features `x` and provide some kind of output. Each step that goes in between the input layer and the output layer is a matrix multiplication

