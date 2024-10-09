Live Number Detection Using Hand Gestures
This project implements a live hand gesture recognition system to detect numbers (0-9) using MediaPipe for hand tracking and a Torch LSTM (Long Short-Term Memory) model for gesture classification. The application runs in real-time and captures gestures from one hand using a webcam.

Table of Contents
Overview
Features
Installation
Usage
Model Training
Results
Contributing
License
Overview
This project aims to detect numbers drawn by hand gestures using live video input. MediaPipe is used for hand landmark detection, and a pre-trained LSTM model classifies the temporal sequence of hand landmarks into specific number gestures.

Technologies Used:

MediaPipe: For hand landmark detection.
PyTorch: For building and training the LSTM model.
OpenCV: For capturing video feed from the webcam.
Features
Real-time hand gesture recognition for numbers (1-3).
Uses LSTM to process temporal sequences of hand movements.
Easy to extend to detect more complex gestures or numbers.
Visualizes hand landmarks and the recognized number on the screen.

Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/hand-gesture-number-detection.git
cd hand-gesture-number-detection
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
The requirements.txt file includes:

mediapipe
torch
torchvision
opencv-python
numpy
Usage
Run the live gesture detection:

Model Training
Data Collection:
You can collect your own dataset by saving hand landmarks during live detection. Use mediapipe to extract and store the landmarks as a sequence of 21 points for each hand frame. Multiple frames of data will be used to form the sequence for LSTM training.

Preprocessing:
Normalize the hand landmarks and sequence them for feeding into the LSTM model. Each sequence represents a full gesture of a number.

Training:
The LSTM model can be trained on sequences of hand landmarks using the following script:

Model Architecture:
The LSTM model takes a sequence of hand landmarks as input and outputs a classification of the hand gesture as one of the numbers (1-3).

Results
The system should achieve real-time performance with reasonable accuracy depending on the quality and quantity of the training data. You can visualize the detected numbers in real-time using OpenCV’s window.

Contributing
Contributions are welcome! Feel free to open issues or submit pull requests with improvements or additional features.

License
This project is licensed under the MIT License - see the LICENSE file for details.
