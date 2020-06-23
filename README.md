# SFND 2D Feature Tracking

<img src="images/keypoints.png" width="820" height="248" />

The idea of the camera course is to build a collision detection system - that's the overall goal for the Final Project. As a preparation for this, you will now build the feature tracking part and test various detector / descriptor combinations to see which ones perform best. This mid-term project consists of four parts:

* First, you will focus on loading images, setting up data structures and putting everything into a ring buffer to optimize memory load. 
* Then, you will integrate several keypoint detectors such as HARRIS, FAST, BRISK and SIFT and compare them with regard to number of keypoints and speed. 
* In the next part, you will then focus on descriptor extraction and matching using brute force and also the FLANN approach we discussed in the previous lesson. 
* In the last part, once the code framework is complete, you will test the various algorithms in different combinations and compare them with regard to some performance measures. 


#### Results and explanation
The time it takes for keypoint detection and descriptor extraction for each detector/descriptor combination are logged in the excel file `Camera_Assignment_Result.xlsx`. First, I collected the number of keypoints for each detector and each image and the time it takes. Then the time it takes for matching keypoints. Finally, the time for descriptor extraction. 

The used criteria for picking the detctor/descriptor combination is the total mean processing time per image. The total mean time is the sum of keypoints detection time per image, keypoints matching time per image and descriptor extraction time per image.

From the data collected we can see that the top 3 detector/descriptor combinations based on total processing time per image criteria are :

1) FAST + ORB
2) ORB + BRIEF
3) FAST + BRIEF

