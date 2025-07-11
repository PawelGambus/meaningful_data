Models are just programs. What makes them different is that a program executes a specific task. Model also does that but it can perform more than one task. It can be adjusted with weights to change what it's doing. It's a little bit like a parametrized program. Model is a more modern word to imply that it can actually do many different things.

Weights are referred to as model parameters. A weight is a subclass of a parameter.

A result of a model is something different than its performance. A result is simply an output. Performance is telling us how good that output is. 

An **Architecture** is a model without weights. An architecture just describes the structure of what is going to be trained. An architecture defines what activation function to use, and how many nodes and layers the model contains.

**Loss** is a measure of **performance**. Depends on *predictions* and correct *targets*.

**Predictions** are just the results of the model.

**Predictions** are calculated from *data*, and this *data* is provided without *labels*. Meaning: The model doesn't know up front what the predition (dependent variable value) should be.

**Label** is what the model tries to predict. Label is the correct value that we strive to predict with the model. Also called: **target**.

**valid_pct** stands for the fraction of data that will be used for validation, and not for training. Default is 0.2.
Validation set is used to measure the accuracy of the model.

**seed** is a parameter which determines the choice of the validation set. If we use the same seed, the same validation set will be selected for training.

Accuracy in fast ai is always calculated using the *validation set*.

Methods to avoid overfitting should be used only after confirming that overfitting actually occurs (e.g. by noticing that validation accuracy gets worse). Validation accuracy as opposed to training accuracy-refers to either validation set or training set. 

# Training
**cnn_learner** - a pretrained model based on ImageNer (http:/www.image-net.org) dataset to recognize a htousand different categories. 
cnn_learner will remove the last layer and add one or more layers of appropriate size for your dataset. This last part is a **head**.
Using pretrained models is a **commonly overseen method that is the most important to get more accurrate mmodels, more quickly, with less data and less time and money.**

Using a pretrained model for a diffferent task than it was originally trained for is called  **transfer learning**. In 2020 still a big problem cause not many pretrained models+a lot of things that could not be just transferred. 

**fit** vs **fine_tune**: fit (or train)is for new models, fine_tune for pretrained models (we don't want to throuw away the previously learned things). Technically fine_tuning is a transfer learning technique used on a pretrained model.

**epoch** one run through all the items of the training dataset

Contrary to popular belief (and mine also!), it is possible to inspect what is happening withing the neural network (there's a whole branch of research on that).

It might be a good idea to use CNN for different patterns recognition: You can transform your data into an image. And if a human is able to distingush the categories, so should a CNN be able to do a proper classification. Conclusion: be creative with how you represent your data!

**Loss** vs **metric**. Both show how good the model is. Loss is for SGD, a metric is for humans. 

Machine learning: a discipline in which we define a program not by writing it entirely ourselvs but by leaning from data. Deep learning-a subcategory of machine learning which uses neural networks
