# Fashion_Clothing
To practice multi-class classification, we're going to build a neural network to classify image of different items of clothing  we are taking tensorflow built-in dataset which is fashion clothing dataset which classify image on basis of clothes, uses 10 classes  Datasets has more than 60k image

Here's how data looks like
![image](https://user-images.githubusercontent.com/98272246/213528805-619dbc74-c957-4892-912e-d34a652f1019.png)

TO know more about dataset check out the link -  https://github.com/zalandoresearch/fashion-mnist 

Here we have 10 classes, where we used the multi-class classification model for predicting the fashion clothing
Here is the sample image
![image](https://user-images.githubusercontent.com/98272246/213529559-111c47b9-98db-47a9-a750-f3130e7ae58e.png)

-> Here first we have created a small list so we can index onto our training labels so they're human readable
<h1> Building a multi-class classification model</h1>

For our multi-class classification model, we can use a similar architecture to our binary classifiers, however, we're going to have a tweak few things:

-> Input shape = 28 x 28 shape of one image e.g train_data[0].shape
-> Output shape = 10 (one per class of clothing) e.g len(class_names)

We'll also change the activation parameter of our output layer to be "softmax" instead of 'sigmoid'. As we'll see the "softmax" activation function outputs a series of values between 0 & 1 (the same shape as output shape, which together add up to ~1. The index with the highest value is predicted by the model to be the most likely class.

-> Loss function = tf.keras.losses.CategoricalCrosstentropy()
       * If your labels are one_hot encoded, use `CategoricalCrossentropy`,(e.g. they looked something like [0, 0, 1, 0,...0]


       * If your labels are integer form , use `SpareCategoricalCrossentropy`

-> Output layer activation = Softmax (not sigmoid)
We'll also use the validation_data parameter when calling the fit() function. This will give us an idea of how the model performs on the test set during training.
  
 You can see more about in given notebook
 
 Further on :-
 <h3> For each layer in output its previous layers works as its input as one layer affects the working and flow of another layer </h3> 
 ![image](https://user-images.githubusercontent.com/98272246/213531115-e0e80a24-abf8-420b-a006-e671af9df6d1.png)


 
