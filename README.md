# Melanoma detection with CNN
Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

## Approaches
We have tried three different model approaches and evaluate the results of each of them to find the best one

### 1st Approach
We built a simple model having `2 32 features convolution -> max pooling -> 2 64 features convolution -> max pooling -> Flatten -> FC (512) -> Softmax`

This model was overfitting with a train accuracy of 0.93 and validation accuracy of 0.50. We trained it for 20 epochs

### 2nd Approach
In the second model we added a dropout layer and also a data augmentation layer. We built a simple model having `Augmentation layer -> 2 32 features convolution -> max pooling -> Dropout -> 2 64 features convolution -> max pooling -> dropout -> Flatten -> FC (512) -> Softmax`

This model was not overfitting but the train and test accuracy was quite low below 0.50. The model was again trained for 20 epochs

### 3rd Approach
Before building a model we found out that there a huge class imbalance problem so we added extra 500 images in each classes using Augmentor library

Once we had enough data we built a fairly dense model having `2 32 features convolution -> max pooling -> Dropout -> 2 64 features convolution -> max pooling -> dropout -> 2 128 features convolution -> max pooling -> dropout -> Flatten -> FC (512) -> Softmax`

With this model it was not overfitting and also the train and validation accuracy was quite high at **0.85**


## Conclusions
> We went ahead with the third model which is having accuracy of 0.85

## Contact
Created by [@jawad360](https://github.com/jawad360) - feel free to contact me!
