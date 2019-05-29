# Hand-Written-Digit-Recognition
Machine Learning Classification detecting hand written digits
CSE474 Project 3: Classification


Vickykumar Patel
Department of Computer Science
University at Buffalo
vickykum@buffalo.edu
		
Overview
This project is to implement machine learning methods for the task of classification. First implementing an ensemble of four classifiers for a given task. Using SVM, Random Forest, Neural Networks, and Logistic Regression from scratch. Then the results of the individual classifiers are combined to make a final decision.

1	Logistic Regression
Tried two different parts and compared the accuracy one from public and other from scratch.
1.1	Using Public Libraries
Public library sklearn was used to create the classifier and the data size about 50,000 was fed to the model and trained on it. Further, after the fitting is over we obtain the scores and get the accuracies. There is a direct relation we get from the accuracy so did not observed on the loss and got data from accuracy.
 
It reduced when un-know data from USPS was giving to it as it was large and wasn’t covered in while fitting the model. 
Changes in lambda parameters increasing it.
 

1.2 	Applying Logistic Regression from scratch
Here, first thing was to get our normal way of phi error matrix then do the sigmoid function, get the cross entropy error and keep doing this while getting probabilities from softmax function that helps us deciding which one has best chance to be predicted. Then this how we get the values an apply testing, validation, and USPS data to get final accuracies.
Increasing the value of alpha kept on reducing the accuracy as the skipping of graph was getting more linear and did not get proper predictions as expected. Other way, lamda value was kept constant to 0.01 for most of the time reducing it gt more accuracy compare to 0.01 but then as we kept greater than 0.01 like values, 0.05, 0.09, 0.1, it increased accuracy and then got less again so bet was to keep it around 0.09 – 0.01 range the value.
  

2	Neural Networks
Public library sklearn was used to create the classifier and the data size about 50,000 was fed to the model and trained on it. Further, after the fitting is over we obtain the scores and get the accuracies. There is a direct relation we get from the accuracy so did not observed on the loss and got data from accuracy. For DNN and CNN different changed hidden layers and more the layers better the accuracy become max we achieved was about 60% that covered the DNN module they were simultaneously updated so it has same code for both. Changing hyper parameters that is filters for CNN we c=got maximum 40% accuracy. CNN was faster so that was the final code that was submitted and here is the final accuracy we got.
Accuracy in Testing data: 92.6%
Accuracy in Validation data: 90.3%
 
That was our model that also got better while increasing epocs in it.

3	SVM Packages
Public library sklearn was used to create the classifier and the data size about 50,000 was fed to the model and trained on it. Further, after the fitting is over we obtain the scores and get the accuracies. There is a direct relation we get from the accuracy so did not observed on the loss and got data from accuracy.

3.1	Using Linear Kernel
This model was the one with fastest runtime everything was aligned and even the testing and validating accuracy’s were great. Here is the one we achieved at the end.
 
 
 
3.2	Using Radial Basis Function and gamma = 1
Similarly, we changed the kernel settings and observed the runtime got slower in this particular case but the accuracy in the validation and testing data were found good around for the testing and validation but not differed in USPS data. Here are the following results that were last obtained. This model crashed the computer a couple of time as it was taking longer than 3hrs time in fitting and had more data to train. Reducing the data here are the accuracies we got.
Accuracy in Testing data: 92.6%
Accuracy in Validation data: 93.3%
Accuracy in USPS data: 33.9%

3.3	Using Radial Basis Function with default setting
Again same thing just kept gamma to auto setting. This also took lot of time therefore reduction in reading data was applied that way we were atleast able to get the accuracies.
Accuracy in Testing data: 74.8%
Accuracy in Validation data: 76.7%
Accuracy in USPS data: 29.3%


4	Random Forest Packages
Public library sklearn was used to create the classifier and the data size about 50,000 was fed to the model and trained on it. Further, after the fitting is over we obtain the scores and get the accuracies. There is a direct relation we get from the accuracy so did not observed on the loss and got data from accuracy. 

4.1	Keeping 500 Trees Estimators
 
 
.
4.2	Keeping Default Estimators
In the below results we kept default estimators and tested the accuracy of the model.
 
 

5	Ensemble Classifier (Majority Voting)
We took all the classifiers and then applied majority voting method the most guessed number was chosen and then that was kept as actual predicted value out of all these above models Logistic, SVM, RFC, and Neural networks. This did help reducing the actual error overall though it did have overall accuracy lesser than some of the classifiers but the average helped out getting best choices in Testing and Validating data.
5.1 Here Logistic model is same, Neural is DNN based, SVN has linear kernel, and RFC had 500 estimators.
 
In the above results the classifiers were kept to their slowest running time models so that parallel calculations can be done easily. In this part it was more important to observe the average accuracy get better when all the classifiers accuracy is taken in count
5.2 Here Logistic model is same, Neural is DNN based, SVN has linear kernel, and RFC had 500 estimators.
 
These section 5.1 and 5.2 were the best average accuracy we could have achieved with the previous models. Testing and validation were the smaller data’s so the accuracy were precisely maintained as the belonged to a particular cluster that was used to design the models. On the other hand, USPS data was new so even the combined model did not get the correct output as we expected. Still maintaining overall accuracy works so this should be applied whenever we get weird data.



