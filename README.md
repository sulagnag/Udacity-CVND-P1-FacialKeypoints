# Udacity-CVND-P1-FacialKeypoints
Combine the knowledge of computer vision techniques and deep learning architectures to build a facial keypoint detection system that takes in any image with faces, and predicts the location of 68 distinguishing keypoints on each face

## Facial Keypoint Detection
<img src='images/key_pts_example.png' width=50% height=50%/>

Facial keypoints (also called facial landmarks) are the small magenta dots shown on each of the faces in the image above. In each training and test image, there is a single face and 68 keypoints, with coordinates (x, y), for that face. These keypoints mark important areas of the face: the eyes, corners of the mouth, the nose, etc. These keypoints are relevant for a variety of tasks, such as face filters, emotion recognition, pose recognition, and so on. Here they are, numbered, and you can see that specific ranges of points match different portions of the face.

<img src='images/landmarks_numbered.jpg' width=50% height=50%/>

## The Dataset
This facial keypoints dataset consists of 5770 color images. All of these images are separated into either a training or a test set of data.

3462 of these images are training images to use for creating a model to predict keypoints.
2308 are test images, which will be used to test the accuracy of the model.

## The model
I have used a CNN with the following layers
<li> Convolutional layers
<li> Maxpooling layers
<li> Fully-connected layers

To avoid overfitting, I have used dropout layers and batch normalisation.

## The feed forward behaviour
The network takes an image tensoe as input. The conv layers, with the relu activation function, followed by the max pooling layers, detect the features from the image. The last fully connected layers mark the 68 keypoints from the detected features.

## Backpropagation
While training, the network compares its output of 68 keypoints with the labels provided. Depending on the error, the network weights are updated.
Overtime, the network learns and the error(loss) reduces as seen in the graph
