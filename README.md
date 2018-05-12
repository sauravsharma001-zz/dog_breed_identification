# **Dog Breed Identification**


## Introduction
This is a competition hosted on Kaggle, which was completed as my final project for Machine Learning course.
The main purpose of this project is to recognize the breed of a Dog using different machine learning techniques.
The scope of project was reduced to identifying just 6 breeds instead of 120 breeds, namely boston bull, chihuahua,
doberman, golden retriever, irish wolfhound and redbone.

## Approach
Every dog have some features which are innate to a breed. Using those features we can train a machine to correctly predict a dog's breed.

The first step was to extract various features from the training image by using the SIFT algorithm. 
After extracting the features, we use the K-means clustering algorithm to group together similar kind of features 
which provide an approximate estimate as to what the image is. Using the result from K-means clustering, bag of 
features is created which contains the frequency of features belonging to different cluster for a given image.
Using bag of features, different classifiers were trained  (in our case KNN, SVM and AdaBoost).


## Result 
The program was tested for 6 different values of k. However, the most optimum result for each classifier was obtained 
by using different values of the clusters. i.e. for k= 10, 20, 30, 40, 50, 60. 
Below is a table for results obtained using different values for k.

|  k   |   KNN   |   SVM   |  AdaBoost  |
|:----:|:-------:|:-------:|:----------:|
|  10  |  44.27  |  31.14  |  30.93     |
|  20  |  47.24  |  40.25  |  40.46     |
|  30  |  50.21  |  38.93  |  39.83     |
|  40  |  48.51  |  44.06  |  45.33     |
|  50  |  49.36  |  42.16  |  44.06     |
|  60  |  49.36  |  43.85  |  43.00     |

## Reference
Competition Page: https://www.kaggle.com/c/dog-breed-identification/data <br/>
Stanford Dog Data Set: http://vision.stanford.edu/aditya86/ImageNetDogs/
