# Hand Detection with MediaPipe

## To run the code, please either use "Visual Studio" or "Jupyter Notebook from Anaconda Navigator".

### For the project video, please check the "Project Video" file. Thank you.

<br>

## Code Explanation:

This code utilizes the MediaPipe library to detect and track hand landmarks in real-time using a webcam. Here's a breakdown of the key components and steps:

1. **Importing Libraries**: The code imports the necessary libraries, including OpenCV (cv2) for computer vision tasks and MediaPipe (mp) for hand detection and tracking.

2. **Initializing MediaPipe Hands Module**: The `mp_hands` module is initialized with specific parameters such as `model_complexity`, `min_detection_confidence`, and `min_tracking_confidence`. These parameters determine the accuracy and sensitivity of the hand detection and tracking process.

3. **Opening Webcam Stream**: The code initializes the webcam stream using OpenCV's `VideoCapture` function.

4. **Hand Detection and Tracking Loop**: Within a `while` loop, the code continuously reads frames from the webcam and processes them for hand detection and tracking using the MediaPipe Hands module.

5. **Processing Each Frame**: For each frame captured from the webcam, the following steps are performed:
   - The frame is converted from BGR to RGB format, and flipped horizontally to enable selfie-view display.
   - The MediaPipe Hands module processes the RGB frame to detect and track hand landmarks.
   - If hand landmarks are detected (`results.multi_hand_landmarks`), the landmarks are drawn on the frame using `mp_drawing.draw_landmarks`.
   - The annotated frame with hand landmarks is displayed in a window named "MediaPipe Hands".

6. **Exiting the Program**: The loop continues until the user presses the 'ESC' key (key code 27), at which point the webcam stream is released (`cap.release()`) and all OpenCV windows are closed (`cv2.destroyAllWindows()`).

This code provides a real-time visualization of hand landmarks detected by the MediaPipe Hands module using a webcam feed.

*** **Here**, keypoint means curvature point. 

*** **Video Capture(0)** -> if primary webcam / built-in webcam.
    **Video Capture(1)** -> if secondary webcam (not built-in webcam).

## Keypoints:
- Real-time hand detection and tracking using the MediaPipe library.
- Webcam stream is captured and processed frame by frame.
- Detected hand landmarks are annotated on each frame.
- The annotated frames are displayed in real-time.
- The program exits when the 'ESC' key is pressed.

