# Vehicle_Detection_System
 Vehicle Detection System in Python using OpenCV. Detects and counts vehicles in a video stream, with background subtraction and contour analysis. Technologies: Python, OpenCV, NumPy.

 Vehicle_detection_system project output(here is how it turned out):
 https://github.com/KeerthiK2005/Vehicle_Detection_System/assets/128359412/07b8ce42-6e40-446b-a9b4-6793c2f5d1cd

**Need for vehicle detection:**
It covers the latest need for intelligent traffic management systems like
1. Traffic Management and Planning
2. Parking Management System
3. Traffic Control

**Outsketch:**
1. Detector
2. Tracker
3. Counter

**Project Description:**

This project is a Vehicle Detection System that uses computer vision techniques to detect, track and count vehicles in a given video stream. The system analyzes each frame of the video to identify and count vehicles that pass a predefined line on the screen. The code is written in Python and utilizes the OpenCV library for computer vision and image processing.

**Project Structure:**

The project consists of a single Python script containing the code for the Vehicle Detection System. The script is designed to process a video feed, apply background subtraction, and identify vehicles in each frame. It includes the following main components:

1. **Importing Libraries:** The project starts by importing the necessary libraries. OpenCV (cv2) is used for video capture and image processing, while NumPy (np) is used for numerical operations.

2. **Video Capture:** The code initializes a webcam (or reads a video file) to capture frames for analysis.

3. **Parameters:** Various parameters are defined to control the system, such as the minimum width and height of rectangles that will be considered as vehicles. A count line position is also set to determine where vehicles will be counted.

4. **Background Subtraction:** The code uses the MOG (Mixture of Gaussians) background subtractor algorithm provided by OpenCV to extract foreground objects, which are likely vehicles, from the video feed.

5. **Frame Processing:** Each frame is processed in the following steps:
   - Convert the frame to grayscale.
   - Apply Gaussian blur to reduce noise.
   - Apply background subtraction to identify moving objects.
   - Dilate the resulting image to connect vehicle components.
   - Use morphological operations to further clean and improve object detection.

6. **Contour Detection:** The code finds contours in the processed image and iterates over them to identify potential vehicle candidates. It filters out rectangles that do not meet the minimum size criteria and draws bounding boxes around the detected vehicles. It also keeps track of vehicle counts.

7. **Vehicle Counting:** The system counts vehicles as they cross a designated line on the screen. When a vehicle is detected crossing this line, the counter is incremented, and the system displays the count on the screen.

8. **Display Output:** The original video frame is displayed with bounding boxes around detected vehicles and the vehicle count. The system waits for a key press to exit.

9. **Cleanup:** The video capture and OpenCV windows are released and closed when the script is terminated.

**Technologies, Libraries, and Languages Used:**

- **Python:** The primary programming language for this project.(used version 3.12.0)
- **OpenCV (cv2):** Used for video capture, image processing, contour detection, and visualization.
- **NumPy (np):** Utilized for numerical operations and array handling.

**Sequence of Project Building:**

1. Import necessary libraries, including OpenCV and NumPy.
2. Initialize the video capture from a webcam or video file.
3. Define parameters for object detection, including minimum rectangle sizes and count line position.
4. Apply background subtraction to identify moving objects.
5. Process each frame, including converting to grayscale and applying morphological operations.
6. Detect contours in the processed image.
7. Filter and count vehicles based on size criteria.
8. Display the original video frame with bounding boxes around detected vehicles and the vehicle count.
9. Continuously loop through frames until the user exits.
10. Release the video capture and close OpenCV windows upon exit.

This project can be further extended and customized for specific applications, such as traffic monitoring, parking lot management, or security systems. Additionally, it can serve as a foundation for more advanced computer vision projects involving object detection and tracking.
