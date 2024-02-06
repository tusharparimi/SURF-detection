# SURF-detection

In this project I use the SURF (Speeded-Up Robust features) to detect an object in the real time video capture and draw an bounding box for the detected object by applying Homography.

<img width="311" alt="image" src="https://github.com/tusharparimi/SURF-detection/assets/93556280/414a5bdc-7608-4373-9e54-3a42dcd0a366">

Real-time video-
https://youtu.be/RQYI0P72Q4Q?si=kSssbeXkQdsLU7UV

### Flow
- Extract SURF features(keypoints, descriptors) in template image (book) and in real time video capture frame.
- Find corresponding matches between the two sets of extracted features using FLANN(Fast Library for Approximate Nearest Neighbors)
- Compute the Homography matrix based on matched correspondenses (particularly used RANSAC regressor for Homography)
- Find corresponding positions of corner points in template image to real time video capture frame by transformation with computed Homography matrix.
- Plot matches and bounding box using opencv draw functions.

### Note
The SURF detection features was implemented on top of the [camera-app](https://github.com/tusharparimi/camera-app) project. So please use the comments in code to check the code for just SURF detection.



