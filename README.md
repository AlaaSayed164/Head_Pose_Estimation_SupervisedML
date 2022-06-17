## Head_Pose_Estimation_SupervisedML
* [General info](#general-info)
* [Output Example](#Output-Examples)

## General info
In this project we will draw the 3 position axis (pitch,yaw,roll) by predicting the 3 angels of each position by training 3 models to predict each angel.


![Axis-rotations-pitch-yaw-and-roll-and-translation-specified-by-a-translation-vector-t](https://user-images.githubusercontent.com/101005712/174391309-c0380eb5-164a-47ab-b8c7-9b5df4e57aa9.png)



* step1: we download  AFLW2000 dataset that contain 2000 image and 2000 matlab file.
* step2: we used MediaPipe library to generate the landmark points of the face of each image in dataset.
* Due to issues where some pictures weren't loaded properly, only 1711 samples were collected with 940 features (468 for X and 468 for Y).
* step3: we used mat file extract the 3 angels and it well be our labels
* step4: we split our data using train-text split, then used SVM model  
* step5: in testing we used the MediaPipe Library to generate the landmarks as we did in the training phase and using the trained models to predict the 3 labels and using them to draw the axis.

## Output Example
Here we have input video 


https://user-images.githubusercontent.com/101012562/174390867-48226f2a-e1d8-45ed-b2c9-e37aa58954e7.mp4

