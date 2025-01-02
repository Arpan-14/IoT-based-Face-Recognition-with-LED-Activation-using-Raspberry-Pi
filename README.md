# IoT-Based Face Recognition with LED Activation using Raspberry Pi

This project demonstrates the use of facial recognition on a Raspberry Pi with IoT capabilities. It captures and stores facial images in a dataset, recognizes faces, and activates an LED light when a recognized face is detected.

## Instructions

### 1. Set up the Raspberry Pi
- Connect the Raspberry Pi to a monitor, keyboard, and mouse.
- Ensure the Raspberry Pi is running the required operating system (e.g., Raspberry Pi OS).
- Connect the Raspberry Pi to the internet and set up SSH (optional for remote access).

### 2. Connect Additional Resources
- Connect an **LED light** to the Raspberry Pi via the GPIO pins using a **breadboard**. This LED will activate based on face recognition.
- Set up a **boot loader** for the Raspberry Pi if required for your setup.

### 3. Run `headshot.py` to Capture Images
- After setting up the hardware, run the script `headshot.py` on the Raspberry Pi to capture images for your face recognition dataset.
- The script will store these captured images in the dataset folder for future use.

    ```bash
    python headshot.py
    ```

- Follow the on-screen instructions to capture your face images. These will be saved in the `dataset/` folder.

### 4. Run `facial_req.py` to Recognize Faces
- After capturing the images, run the `facial_req.py` script to begin recognizing faces.
- The script will use the images stored in the dataset to identify faces. It will also provide a confidence level for the recognition.

    ```bash
    python facial_req.py
    ```

- If a face is recognized, the LED light will activate to indicate a successful match.

### 5. IoT Integration
- The Raspberry Pi will be integrated with IoT, enabling remote monitoring and triggering of actions based on the facial recognition results.
- The LED light will turn on when the face is recognized, signaling a match.

---

## Requirements
- Raspberry Pi with Raspbian OS (or another suitable OS)
- Python 3.x
- OpenCV (for face recognition)
- Raspberry Pi GPIO library (for LED control)
- Breadboard and jumper wires for connecting the LED

---

## Troubleshooting
- **No image captured:** Ensure your camera is connected properly and configured in the Raspberry Pi's settings.
- **Low confidence in recognition:** Ensure you have enough varied images in the dataset for the algorithm to recognize your face accurately.
- **LED not lighting up:** Double-check the wiring of the LED and ensure it's properly connected to the GPIO pins.

---
