## Advanced Lane Finding

![Lanes Image](./output_images/final_result_test3.jpg)

The goals / steps of this project are the following:

* Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.
* Apply a distortion correction to raw images.
* Use color transforms, gradients, etc., to create a thresholded binary image.
* Apply a perspective transform to rectify binary image ("birds-eye view").
* Detect lane pixels and fit to find the lane boundary.
* Determine the curvature of the lane and vehicle position with respect to center.
* Warp the detected lane boundaries back onto the original image.
* Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.

The source is present in a newly created file named "Advanced_LaneFindingPipeline.ipynb". The files contains the aforementioned steps and explains various building blocks,analysis,experiements done to achive project goals. The test images present in "test_images" were used to analyse and check intermediate results to fine tune the results. All the intermediate results, the final outputs for all test images and project output video are present in the "output_images" folder.

## Camera Calibration
The camera was calibrated using 9x6 chessboard images. Using objectpoints and image points , matrix and distortion coefficient were calculated. The code for this section can be found in file "Advanced_LaneFindingPipeline.ipynb" in 1st section "Camera Calibration using 9x6 chessboard images - Finding Object points and Image points" from line# 1 through #40 arrives at objectpoint (3-D points) and imagepoints(2-D points) using chessboard image corners. All the calibration images were used to create a list of imagepoints which are furher used to calibrate camera and un-distort image. 

The other section "Camera Calibration using 9x6 chessboard images - Camera Calibration and undistort test chessboard image" from line# 1 through #25 has code using which matrix and distortion coeffient is calculated. Using these coefficinets,a sample chessboard image is undistorted. 

<img src="./camera_cal/test.jpg" width="400" alt="Image1" />  <img src="./camera_cal/test_undist.jpg" width="400" alt="Image1" />

## Pipeline (Test Images)

### Example of a distortion-corrected image

The section "Camera Calibration using 9x6 chessboard images - Camera Calibration and undistort test real world image" and from code line#1 to 19 corrects the distorted image using imagepoints and objectpoints.

<img src="output_images/test2.jpg" width="400" alt="Image1" />  <img src="output_images/test2_undist.jpg" width="400" alt="Image1" />


To help the reviewer examine your work, please save examples of the output from each stage of your pipeline in the folder called `output_images`, and include a description in your writeup for the project of what each image shows.    The video called `project_video.mp4` is the video your pipeline should work well on.  

The `challenge_video.mp4` video is an extra (and optional) challenge for you if you want to test your pipeline under somewhat trickier conditions.  The `harder_challenge.mp4` video is another optional challenge and is brutal!

If you're feeling ambitious (again, totally optional though), don't stop there!  We encourage you to go out and take video of your own, calibrate your camera and show us how you would implement this project from scratch!

## How to write a README
A well written README file can enhance your project and portfolio.  Develop your abilities to create professional README files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).

