# Model-comprehension

The motivation for creating this notebook was to demonstrate how a simple model that preforms well on a certain task can have an complete lack of understanding when it comes to approaching a task that slightly deviates from the original one. 

### Method
The model was trained on the mnnist dataset and preformed well on both the training and testing data (as was expected since this is a very basic dataset). Then the goal was to see how the probability distribution from the softmax output function changd when we introduced similair images (same shape and color space), but not quite the same as in the mnist dataset (not images of clothes)

### Result
The highest probability in the probability distribution (the label that the model is the most confident on) decreased significantly after introduing the new images (from close to 100% on the mnist images to around 60% on the new images). However this was still a suprisingly high probability seeing as the images were not images of digits. This shows that the model has a very poor understanding of its input data. It would be more intuitive to expect a model that has trained on purely digit images to have a even (and low) probability-distribution for all the possible labels.
