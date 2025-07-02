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
