# deep-learning-challenge

NN Report:

Overview:  The purpose of this analysis is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
Results:
The target variable is “IS_SUCCESSFUL”
The features are:  Application Type, Affiliation, Classification, Use Case, Organziation, Status, Income Amount, Ask Amount, & Special Considerations.

Variables that are neither Targets or Features: EIN and Name

Neurons, layers, and activation functions and why:  I started the model with 2 hidden ReLU layers with 8 and 6 neurons respectively and an output Sigmoid layer with one neuron.  I chose these parameters because I was told ReLU are the 2 most common activation functions, and I arbitrarily chose 8 and 6 neurons because that’s generally the number we used in our activities in class. For the output layer, the Sigmoid function is bound to 1 neuron by default.

I was unable to achieve the target performance of 75%, however I was very close at 73%.

On my first attempt at optimization, I added a hidden tanh layer with 2 neurons which resulted in no improvement of the model, with performance remaining at 73%.

On my second attempt at optimization, I kept the same parameters as in part f.), but I reduced the epochs to 25.  Again, no improvement.

On my third attempt, I added another hidden ReLU hidden layer with 8 neurons and again, no improvement from 75%.  

Summary:  The keras model was fairly close at hitting the 75% target with 73% performance, however it didn’t seem to matter whether adding additional layers or neurons resulted in any improvement in the model.  I would attempt to use a Random Forest classifier to improve the performance since RF is known to be robust against outliers.  I believe there is probably too much influence from outliers in this dataset, so RF may be the way to go here.
