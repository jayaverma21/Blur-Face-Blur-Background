# Blur-Face-Blur-Background
This Python script provides real-time face and background blurring using OpenCV. Users can choose the service via a voice prompt implemented with pyttsx3.

# Features
+ Blur Faces: Detects faces in real-time and applies a Gaussian blur to them.
+ Blur Backgrounds: Detects faces in real-time and applies a Gaussian blur to everything except the faces.
+ Voice Prompts: Guides users to choose between the two services using voice prompts.

 # Requirements
+ Python 3.x
+ OpenCV (pip install opencv-python)
+ pyttsx3 (pip install pyttsx3)

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/jayaverma21/Blur-Face-Blur-Background.git
    cd Blur-Face-Blur-Background
    ```

2. Install the required packages:

    ```bash
    pip install opencv-python pyttsx3
    ```

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/yourusername/face-background-blur.git
    cd face-background-blur
    ```

2. Install the required packages:

    ```bash
    pip install opencv-python pyttsx3
    ```

## Usage

1. Run the script:

    ```bash
    python face_background_blur.py
    ```

2. You will be prompted to choose one of the following options:
    - Press `1` to blur the faces.
    - Press `2` to blur the background while keeping the faces visible.

3. The webcam feed will open in a new window, and the selected blurring option will be applied in real-time.

4. Press the 'Enter' key to exit the application.

## Code Overview

The main script performs the following steps:

1. Initializes the pyttsx3 engine for voice prompts and sets properties like speech rate, volume, and voice.
2. Prompts the user to choose a service using both text and speech.
3. Based on the user's choice, either blurs detected faces or blurs the background while keeping faces visible:
    - **Blurring Faces**: 
        - Uses a pre-trained Haar cascade classifier for face detection.
        - Applies Gaussian blur to detected faces and replaces the original faces with the blurred versions.
    - **Blurring Background**: 
        - Uses a pre-trained Haar cascade classifier for face detection.
        - Applies Gaussian blur to the entire frame.
        - Keeps detected faces visible by replacing blurred faces with the original, unblurred faces.

4. Displays the processed video feed and checks for the 'Enter' key to exit the application.
