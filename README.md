# Hand Gesture Mouse Control with MediaPipe

This project uses the [MediaPipe](https://mediapipe.dev/) library for hand tracking to control your mouse with hand gestures via a webcam. The script detects various gestures and translates them into mouse actions such as left-click, right-click, double-click, and moving the mouse cursor.

## Features

- **Move mouse**: Move your hand to control the cursor position.
- **Left-click**: Perform a gesture to simulate a left mouse click.
- **Right-click**: Perform a gesture to simulate a right mouse click.
- **Double-click**: Perform a gesture to simulate a double mouse click.

## Prerequisites

Before running the project, ensure you have the following dependencies installed:

- Python 3.x
- OpenCV (`cv2`)
- MediaPipe (`mediapipe`)
- PyAutoGUI (`pyautogui`)
- NumPy (`numpy`)
- pynput (`pynput`)

You can install the required packages using the following command:

```bash
pip install opencv-python mediapipe pyautogui numpy pynput
```

## Getting Started

### 1. Clone the Repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/mzhu296/hand-gesture-mouse-control.git
cd hand-gesture-mouse-control
```

### 2. Run the Script

After cloning the repository and installing the required dependencies, you can run the script:

```bash
python hand_gesture_control.py
```

Make sure your webcam is connected and working, as the program will capture hand movements through the webcam.

### 3. Available Gestures

- **Move mouse**: Move your index finger around the screen to control the mouse cursor.
- **Left-click**: Make a gesture with your thumb and index finger close together.
- **Right-click**: Bent index finger, then moving them away from each other.
- **Double-click**: Bring your thumb and index finger close together while keeping the middle finger folded.

### 4. Exit the Program

To exit the program, press `q` on your keyboard.

YouTube Demo

Watch the project in action by clicking on the link below:
https://www.youtube.com/watch?v=nN0gGC3r_9M

## Code Structure

- `main()`: The main loop that captures frames from the webcam and processes them for hand tracking and gesture detection.
- `detect_gesture()`: Detects specific hand gestures and triggers mouse actions.
- `is_left_click()`, `is_right_click()`, `is_double_click()`: Functions that detect gestures for left-click, right-click, and double-click based on hand landmark positions and distances.
- `move_mouse()`: Moves the mouse pointer to the position of the detected index finger.

## Troubleshooting

- **Webcam Not Detected**: Make sure your webcam is properly connected and not being used by another application.
- **Gestures Not Detected**: Ensure your hand is visible in the webcam feed and try increasing the `min_detection_confidence` or `min_tracking_confidence` parameters in the `hands` object if gestures aren't being detected consistently.
- **Slow Performance**: If you experience lag, try closing unnecessary applications, as real-time video processing can be resource-intensive.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
