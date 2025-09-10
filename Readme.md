# Ningaflick 🥷🖱️

NingaFlick is a Python-based project that transforms your hand movements into a virtual mouse, allowing you to control your computer with gestures. Utilizing computer vision, it tracks your hand and translates the position of your index finger into mouse cursor movements, enabling a futuristic, contact-free interaction with your PC.

-----

### 🚀 Key Features

  * **Virtual Mouse Control:** Move your mouse cursor by simply moving your hand in front of the camera.
  * **Intuitive Gestures:** The system detects your index finger to control the cursor.
  * **Click Functionality:** You can initiate a **mouse-down event** by extending your pinky finger. This is useful for dragging and selecting items.
  * **Dynamic Calibration:** The tracking area is defined by a visible rectangle on the screen, automatically mapping your hand movements to the entire screen resolution.

-----

### ⚙️ Technologies Used

  * **Python:** The core programming language.
  * **OpenCV:** A powerful library for computer vision, used for capturing video and processing images.
  * **`cvzone`:** A helpful computer vision library built on top of OpenCV, simplifying hand detection and tracking.
  * **`mouse`:** A Python library for programmatically controlling the mouse.
  * **`pyautogui`:** Used to simulate mouse button actions like clicking.
  * **`numpy`:** For performing mathematical operations, specifically for mapping coordinates.

-----

### 💻 Getting Started

### Prerequisites

  * Python 3.6 or higher
  * A webcam

### Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```

2.  Install the necessary libraries:

    ```bash
    pip install opencv-python cvzone mouse pyautogui numpy
    ```

### Running the Application

1.  Ensure your webcam is connected and enabled.

2.  Run the main script from your terminal:

    ```bash
    python your_script_name.py
    ```

3.  A window will appear displaying the camera feed. Position your hand within the tracking rectangle to begin controlling the mouse. To exit the application, press the `q` key.

### How it Works

The script continuously captures video from your webcam. It detects your hand and identifies key landmarks, particularly the tip of your index finger. The coordinates of this landmark are then mapped from the camera's resolution to your screen's resolution. The `mouse.move()` function uses these mapped coordinates to move the cursor. When your pinky finger is detected as "up," the `pyautogui.mouseDown()` function is triggered, simulating a click.
