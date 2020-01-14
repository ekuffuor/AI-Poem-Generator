# AI-Poem-Generator

In this project, I am build and train a Recurrent Neural Network. Since this process requires a massive amount of computing power, in order not to be constrained by my personal computer, I initially run the model with Amazon’s computing resources via Amazon Web Service’s Elastic Cloud Compute platform. I started by setting up an Elastic Cloud Computing (EC2) instance. I then selected the Deep Learning Amazon Machine Image (AMI). This allowed me to create a virtual machine within the Amazon Elastic Compute Cloud. With this selection, I was saved the rigorous step of installing various deep learning packages for my project. It also afforded me the option to launch multiple instances from a single AMI with the same configuration if the need arose. Once the instance was up and running, I linked it to my Jupyter notebook. After I few runs, I noticed it was very expensive to keep my instance running and therefore switched to a more affordable cloud computing service called Floydhub which provided the same functionality as AWS.  



I coded this project in using Python in my Jupyter notebook. Some of the libraries I imported include TensorFlow which is an open-source software library and machine learning framework developed by Google for dataflow programming across a range of tasks, and machine learning applications such as neural networks. Also, Numpy, which will add support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on arrays.






The dataset implemented in this project consist of a collection of poems and sonnets by Shakespeare. There was no particular process in the selection of these literary works however, I made sure to select works that did not have any copyright restriction in terms of its use in academic and research projects. The list included all the sonnets by Shakespeare along with other pieces of his work in poetry, plays and short stories.     
Recurrent Neural Network (RNN)
Artificial Neural Networks in general are capable of modeling and processing nonlinear relationships between inputs and outputs in parallel. In this project, I trained my RNN on my input dataset in order to improve the model and cause it to be able to generate original literature. 
I used a batch to iteratively train the model to account for the size of my dataset. In terms of layering, I added further hidden layer after every training to improve quality of the output. Thus, I built the RNN with 3 hidden layers, 3 of which used tanh activation functions while the final layer used a SoftMax classifier to feed into a cross-entropy loss function using Adam optimizer. I trained the model for 3000 epochs on the training dataset, which means the RNN will run through the batches of data three thousand times. The batch size was set to 250 whereas the number of RNNs was set to 512. The data sequence length parameter was set at 30, meaning that was the max sequence the recurrent neural network can generate and utilize. I set the learning rate to 0.001 to allow the RNN learn slowly and efficiently as a larger number would have caused the model to be haphazard. With more time and resources, this learning rate can be tuned to suit the experimenter's preferences depending on the type of outcome they seek as well as the kind of model they have constructed. The other parameter may also shape the choice of the learning rate based and affect how these points interact with each other.



The result from this was promising. The RNN model was able to produce outputs based on the input data that was fed into it. The model was able to produce literature texts that are coherent enough to read and understand. I made some interesting observations about my results; the choice of words and phrasing of sentences matched the medieval-style writing of Shakespeare, on whose corpus this model was trained on. The three generated poems included in this repository show the level of sophistication of this current model. With Further training, this model will be the next Pulitzer Prize winner.
