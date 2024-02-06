# SURF-detection

In this project I use the SURF (Speeded-Up Robust features) to detect an object in the real time video capture and draw an bounding box for the detected object by applying Homography.

### Flow
- Extract SURF features(keypoints, descriptors) in template image (book) and in real time video capture frame.
- Find corresponding matches between the two sets of extracted features using FLANN(Fast Library for Approximate Nearest Neighbors)
- plots the matches
- Compute the Homography matrix based on matched correspondenses
