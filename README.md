# SURF-detection

In this project I use the SURF (Speeded-Up Robust features) to detect an object in the real time video capture and draw an bounding box for the detected object by applying Homography.

<img width="311" alt="image" src="https://github.com/tusharparimi/SURF-detection/assets/93556280/414a5bdc-7608-4373-9e54-3a42dcd0a366">

Real-time video-
https://youtu.be/RQYI0P72Q4Q?si=kSssbeXkQdsLU7UV

### Flow
- Extract SURF features(keypoints, descriptors) in template image (book) and in real time video capture frame.
- Find corresponding matches between the two sets of extracted features using FLANN(Fast Library for Approximate Nearest Neighbors)
- Compute the Homography matrix based on matched correspondenses (particularly used RANSAC regressor for Homography estimation)
- Find corresponding positions of corner points in template image to real time video capture frame by transformation with computed Homography matrix.
- Plot matches and bounding box using opencv draw functions.

### How-to-use
- Run the camera-app python file. 
- Click the 'd' button on your keyboard to start detecting the object in real time.
- You can change the template image(book.png) with your custom image but be careful complex templates needed some fine-tuning of SURF params. Also have the custom image in the same directory with the same name (book.png) or replace the path in line 408 of camera-app.py script.

### Note
- The SURF features detection was implemented on top of the [camera-app](https://github.com/tusharparimi/camera-app) project. So please use the comments in code to check the code for just SURF detection.
- Surf algorithm is not available in standard pip installation of opencv-contrib-python. Download and compile using CMake with flag OPENCV_ENABLE_NONFREE=ON. I installed this version in a virtual env.
Tutorial- https://pyimagesearch.com/2018/08/15/how-to-install-opencv-4-on-ubuntu/





