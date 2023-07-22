# Mediapipe Pose Detection and Exercise Counter

This repository contains Python code that uses the Mediapipe library along with OpenCV to perform real-time pose detection and count repetitions of a specific exercise (knee bend). The code captures video from the default camera, processes the frames, detects poses using the Mediapipe Pose model, calculates the angle of the left elbow joint, and counts the number of knee bends based on the detected angles.

## Requirements

Before running the code, ensure you have the following requirements met:

- Python 3.x
- OpenCV (`cv2`) library
- Mediapipe (`mediapipe`) library
- NumPy (`numpy`) library

You can install these libraries using pip:

```
pip install opencv-python mediapipe numpy
```


## How to Use

1. Import Required Libraries

```python
import cv2
import mediapipe as mp
import numpy as np
```
2. Video Feed
The code starts by capturing video from the default camera and displaying it in a window using OpenCV. To stop the video feed, press the 'q' key.

3. Make Detections
In this section, pose detection is performed on the captured video feed using Mediapipe's Pose model. The code extracts pose landmarks (joints) from the detected poses and renders them on the video frames with lines connecting the joints.

4. Determining Joints
This section enhances the previous section by printing the coordinates of the detected pose landmarks, specifically the left shoulder, left elbow, and left wrist joints.

5. Calculate Angles
The code defines a function to calculate the angle between three points (a, b, c) in 2D space. It then calculates and prints the angle formed by the left shoulder, left elbow, and left wrist joints.

6. Knee Bend Counter
The final section introduces a knee bend counter. It uses the calculated angle between the hip, knee, and ankle to determine the stage of the exercise (up or down) and counts the repetitions based on the transitions. The counter's current value and the exercise stage (up or down) are displayed on the video feed.

7. Please note that the code snippets provided here are only an overview of the functionalities. To see the complete code and execute it, please refer to the source code provided in the original files.

### Acknowledgments
The pose detection functionality is made possible by the Mediapipe library developed by Google Research. The library provides pre-trained machine learning models for various tasks, including pose estimation.







