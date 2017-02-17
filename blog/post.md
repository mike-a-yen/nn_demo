# Neural Networks made Easy
Follow along in the [interactive notebook](../mnist_demo.ipynb).

## How to add Neural Nets to your Data Science Toolbox
In many ways neural nets represent the future of machine learning because they can make more "intelligent" decisions than traditional learning algorithms. However the sophistication of these tools tend to make them seem too complicated and inaccessable by even seasoned data scientists. This post will hopefully change your mind and show you that even deep neural nets can be implemented in a matter of minutes.

## What is a neural net and what are those pictures?
A neural net is a machine that takes some input and provides some output. Every neural net has an input layer and output layer, which can be separated by several "hidden" layers. These layers are called hidden because you can not directly observe what is going into or out of them. Some sophisticated neural nets will have several hidden layers which make them fall under the realm of deep learning. For a neural network to be considered "deep" it only needs 2 hidden layers. This picture shows a shallow neural net with a single hidden layer, so this arcitecture would not qualify as a deep learner.

<img src="../nn_diagram.png" width="500px">

These figures are used to illustrate the neural network's architecture which is ultimately responsible for the network's behavior and thus an important thing to think about when constructing your own neural network. There are some loose heuristics for choosing a good architecture, but this is a skill that gets better with experience. Once a good architecture is identified it is illustrated via one of these figures so others can get a better understanding of your network. 

## What is a neural net doing?
The answer can be explained in a mathematically intensive way or a hand-wavy way. For the purpose of this discussion we will choose the later. Just like any other machine learning algorithm neural networks take an input vector of features `x` and provide some kind of output `y`. 

The magic behind neural nets is the way they move data between layers. Data is transfered by combining all of the outputs of the left layer in many different ways and sending each of these different combinations to one of the input nodes of the right layer. While training, your neural net will figure out how to combine the inputs to produce the best outputs. This combining operation is facilitated by matrix multiplication and is the foundation for all neural networks. 

By repetitively making combinations of combinations of the inputs a neural network can figure out the higher level structures in the data. This principle is what makes neural networks so powerful. 

## How can I use a neural net?
There are many popular neural network libraries built for python, however the two that I will focus on here are `Tensorflow` and `keras`. 

<img src="../nn_libs.png" width="400px">

`Tensorflow` is highly customizable and allows the user to get into the nitty gritty of the network's behavior. For example, you can change the way data is transferred between layers, which can be useful for neural net experts. This customizability comes at the cost of development time. I usually find myself recycling many of the same basic steps in all of my neural nets, so this much detail is not something I tend to need.

This is where `keras` comes in. The `keras` library is built on top of `Tensorflow` and is using `Tensorflow`'s mechanics under the hood, but provides a very simple API that allows you to gloss over many of the standard steps while building a neural network. This allows you to focus on refining the course grain details of your network while leaving many of the finer grain details to `keras`. The benefit here is that you can build a complex architecture in less than 10 lines of code without having to be explicit about many of the common steps.

As an additional bonus `keras` neural networks can be easily integrated with `scikit learn` and further treated like any other `scikit learn` machine learning algorithm. This is one of my favorite things about `keras`.

## MNIST Example
<img src="../mnist_ex.png" width="300px">

Included in this post is an [`ipython notebook`](../mnist_demo.ipynb) with three neural networks using two different architectures aimed towards classifying hand written digits. The first two neural nets have the same architecture but are implemented first in `Tensorflow` and then in `keras`. These networks have the same behavior and very similar performance, but the `keras` network is developed in half the amount of code. 

The third network is an illustration of what can be developed in `keras` trading line for line with `Tensorflow`. In about 10 lines of code I built a convolutional neural network that approaches state of the art performance for `MNIST`.

## Limitations

While neural nets can do some really cool things they do have their limitations. The largest I have noticed has been the vast amounts of data needed to train a decent model. Even small neural nets can have hundreds of thousands of weights to tune which is an impossible task to do properly with only a few thousand data points. 

Another important limitation is interpretability. Once you have a lot of data and you have trained a good neural net there will be no way for you to figure out what your model is actually doing. This may be an important thing to consider, especially because other machine learning models have much better interpretability.

## What to do now?
At this point I have given you a 10,000 ft view of how neural nets work and a quick introduction to how you can use them. Hopefully I have convinced you that neural networks can solve some really complicated problems while being easily accessible and fast to develop and test. Until recently I considered neural networks out of reach, but now with `keras` I use them just like any other machine learning model. With that being said, due to their limitations, neural nets are not the first thing I try when starting a new problem.

If you haven't already, I would recommend working through the [interactive notebook](../mnist_demo.ipynb) to test out `tensorflow`, `keras` and to get a feel for both APIs.

## What has been skipped?
A lot. I have tried to convey that using neural nets can be simple, and in some cases they can be. However if you want to really understand neural networks and their behavior, you will need to get very deep into the math behind the algorithm. There are many different free online course, books, websites, etc. that do a great job of explaining the technical details.

## Resources:
[Tensorflow's Getting Started](https://www.tensorflow.org/get_started/get_started) is a great place to learn some more of the basic mechanics behind neural nets.

#### Authors: 
Michael Yen

#### Special Thanks to:
Paul Paczuski
