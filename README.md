#  Color Detection in Real-Time

This project detects a specific color (🟡 yellow) in real-time using a webcam feed. It utilizes OpenCV to process the video frames, convert them to HSV color space, and then applies a mask to detect the color. When the color is detected, a bounding box is drawn around the area where the color appears.

## ✨ Features
-  Detects yellow color in real-time from webcam feed.
-  Draws a green rectangle around the detected color area.

<img width="500" alt="Screenshot 2024-08-11 153521" src="https://github.com/user-attachments/assets/86373f76-7b17-443f-b702-7fd564e62d1e"> <br>
<br>

<img width="600" alt="Screenshot 2024-08-11 153414" src="https://github.com/user-attachments/assets/18532a8e-01f4-4f89-a341-3ec0d5440d1a">

## 📋 Prerequisites

Before running the code, make sure you have Python installed on your system. You will also need to install the required Python packages listed in the `requirements.txt` file.

## 💻 Installation

. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```

## 🚀 Usage

1. **Run the script**:
    ```bash
    python main.py
    ```
   
   The script will start capturing video from your webcam. The live feed will be displayed in a window, and a green rectangle will appear around any detected yellow objects.

2. **Exit the script**:
   - Press the `q` key to exit the video window and terminate the script.

## 📂 Project Structure

- **`main.py`**: The main script that captures video, processes frames, and detects the specified color.
- **`util.py`**: Contains the utility function `get_limits` that calculates the lower and upper HSV bounds for the specified color.
- **`requirements.txt`**: Lists all the dependencies required to run the project.

## ⚙️ How It Works

1. **Color Conversion**:
   - The video feed is captured using OpenCV and converted from BGR to HSV color space.

2. **Masking**:
   - The `get_limits` function in `util.py` computes the lower and upper limits for the color in HSV space.
   - A mask is created by filtering out the pixels within the specified HSV range.

3. **Bounding Box**:
   - The `getbbox` method from the Pillow library is used to find the bounding box of the detected color in the mask.
   - If the color is detected, a green rectangle is drawn around the detected region in the video feed.

## 📦 Dependencies

- `opencv-python==4.6.0.66`
- `numpy==1.23.4`
- `Pillow==9.2.0`

These dependencies are listed in the `requirements.txt` file.













