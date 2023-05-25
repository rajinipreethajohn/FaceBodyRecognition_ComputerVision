# Real-Time Body Language Detection
This code demonstrates the real-time detection of body language using the Mediapipe library. It utilizes the Holistic solution from Mediapipe to detect and track various landmarks on the face, hands, and body.

[![alt text](/images/FB.png)](https://github.com/rajinipreethajohn/FaceBodyRecognition_ComputerVision/blob/main/video/CV_FB.mov)

## Prerequisites
Before running the code, make sure you have the following libraries installed:

Mediapipe (mediapipe)
OpenCV (cv2)
NumPy (numpy)
Pandas (pandas)
Scikit-learn (sklearn)

### You can install these libraries using pip:

pip install mediapipe opencv-python numpy pandas scikit-learn

### Usage
1. Import the required libraries: mediapipe, cv2, pickle, np, pd, StandardScaler, and the classifiers (LogisticRegression, RidgeClassifier, RandomForestClassifier, GradientBoostingClassifier) from sklearn.
2. Load the pre-trained model using pickle.load() from a .pkl file.
3. Initialize the video capture using cv2.VideoCapture().
4. Initialize the Holistic model from mp_holistic.Holistic() with the desired parameters.
5. Read frames from the video capture in a loop.
6. Preprocess the frame by converting it to RGB and making it writeable.
7. Process the frame using the Holistic model and obtain the landmarks for face, hands, and body.
8. Recolor the frame back to BGR for rendering.
9. Draw the landmarks on the frame using mp_drawing.draw_landmarks() for face, right hand, left hand, and pose.
10. Extract the coordinates of the landmarks and create a feature row.
11. Create a pandas DataFrame X from the feature row.
12. Predict the body language class and the probabilities using the pre-trained model.
13. Display the body language class and probabilities on the frame using cv2.putText() and cv2.rectangle().
14. Show the resulting frame with the annotations using cv2.imshow().
15. Exit the loop when the 'q' key is pressed.
16. Release the video capture and destroy all OpenCV windows.


### Acknowledgments
1. The Mediapipe library provides various solutions for different computer vision tasks, including holistic detection of body landmarks.
2. OpenCV is a popular computer vision library used for image and video processing.
3. NumPy provides efficient array operations and mathematical functions.
4. Pandas is a powerful library for data manipulation and analysis.
5. Scikit-learn provides machine learning algorithms and tools for model training and evaluation.
