# What is my project about?

## Abstract
Modern medicine relies heavily on the analysis of white blood cells to provide diagnosis for different types of disease. Most of the methods employed nowadays require large and expensive machinery and are therefore unavailable in large parts of the world. This paper suggests a machine learning based approach to classify leukocytes using only a phone, a cheap microscope, and a 3D printed phone-holder. On validation the model reached an accuracy of 85%. The accuracy under real life conditions has not yet been evaluated.

## Question
The question of this project was to create a lightweight and portable solution to classify white blood cells in stained blood smears. 

## Methods
To do this a convolutional neural network was trained and ported to an android app. To use the app with a microscope, a 3D-printable phone holder was used. The model was created using TensorFlow lite and Keras. For the evaluation of the model a small portion of the data was held back during training. To make the hyperparameter search easier the framework Talos was used. 
To increase accuracy and reliability multiple different networks with varying architecture were combined. The prediction is given by majority vote. This combined network was not yet ported to android.

## Results
A real-life applicable app based on the image classification example provided by TensorFlow was created. The app contains a pretrained model. The model reaches 85% accuracy on validation. The accuracy under real life conditions was not yet evaluated but is estimated to be significantly lower. The app allows the user to zoom in and out to adjust to different hardware magnifications.

## Discussion
The main difficulties for this project were small datasets and low phone camera resolution. The small dataset lead to a model which overfit very quickly and had to be stopped very soon to keep its generalizability. The low resolution was a problem as the network had to work with fewer datapoints and more distortion when compared to the training images. A focus now is to improve the accuracy under those suboptimal conditions. One way to do this would be more preprocessing and data
A possible and very reasonable addition to the project would be to move from image classification to object recognition or segmentation. This would allow us to more easily automate the whole process of creating a blood count, because as of now a person still has to focus the cells manually. This new architecture could be combined with a motorized microscopy table to make a fully automatic blood classifier.

## Conclusion
In the end I managed to build a neural network that can accurately classify leukocytes during validation. The accuracy under real life conditions remains to be evaluated. Because the phone adaptor is already done, and only minor additions must be made to the app I now only have to focus on optimizing the network. If I manage to do this, this could be a great start for machine learning assisted biology education and remote medicine.

# This website is incomplete and still "work in progress"
