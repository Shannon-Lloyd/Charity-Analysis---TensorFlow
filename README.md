

# Alphabet Soup Charity Analysis

## Overview:
 The purpose of this analysis is to develop a tool to predict the best chances of success of applicants looking for funding. Use the provided CSV file containing data on more than 34,000 organizations that have previously received funding to develop a  neural network model using TensorFlow to predict the applicants success.
## Results:
1.	<b> Data Preprocessing </b>
-	<b> What variable(s) are the target(s) for your model? </b> The target for our model is if the campaign is successful. The column for this is in the data received is 'IS_SUCCESSFUL'.
 
-	<b> What variable(s) are the features for your model? </b> The features are the remaining variables provided in the data with the exception of ‘EIN’ and ‘NAME’ which we dropped as non-beneficial.


-	<b> What variable(s) should be removed from the input data because they are neither targets nor features? </b> ‘EIN’ and ‘NAME’ which were removed  because they are non-beneficial.
-	
2.	<b> Compiling, Training, and Evaluating the Model </b>
<b>How many neurons, layers, and activation functions did you select for your neural network model, and why? </b> For all of the following I used activation ‘relu’ for all layers except the output layer which was ‘sigmoid’. I used 100 epochs for training. 
-	
1.	I chose 4 layers to see if more layers provided the best results. The first 2 layers were 20 neurons, the third layer was 7 neurons, and the output layer was one neuron since we were only looking for one value. Loss = .5559  Accuracy = .7271
2.	I used the implied 3 layers with 30 neurons in the first layer, 7 neurons in the second layer, and 1 neuron in the output layer as a basic model to compare the other models against. Loss = .5533  Accuracy = .7328
3.	I used 3 layers again but increased the neurons in layer one to 80 while keeping the other layers the same.  Loss = .5557 Accuracy = .7263
4.	I used three layers again but this time I used 7 neurons on the first layer and 30 neurons on the second layer with the single neuron in the output layer. Loss = .5541 Accuracy = .7278

-	<b> Were you able to achieve the target model performance? </b>  No, the closest I came to the desired results was with my basic second model which had a loss of .5533 and an accuracy of .7328.


-	<b> What steps did you take in your attempts to increase model performance? </b> I tried more layers, more neurons in the initial layer, and more neurons in a deeper layer.
## Summary:  
The 4 models I ran did not provide the desired 75% accuracy for predicting the success of the non-profits applying for funding. I would recommend running keras-tuner to see if the auto tuner can find a better model. 


