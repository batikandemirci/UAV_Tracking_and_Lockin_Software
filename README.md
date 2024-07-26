## UAV Tracking and Locking Software

### Description
This project involves developing a software application that uses computer vision techniques to track and lock onto unmanned aerial vehicles (UAVs). The software leverages a YOLOv5 model for object detection, a Kalman filter for state estimation, and a centroid tracking algorithm for maintaining object identities across frames. The software is capable of detecting and tracking UAVs in video feeds, and it provides a visual indication of successful locking after a specified duration.

![track_gif](https://github.com/user-attachments/assets/e37c7c90-7607-429b-b9c2-5410727fc225)

### Features
- **YOLOv5 Object Detection**: Utilizes a custom-trained YOLOv5 model for detecting UAVs in video frames.
- **Kalman Filter**: Implements a Kalman filter to predict and correct the state of detected UAVs, enhancing the tracking accuracy.
- **Centroid Tracking**: Uses a centroid tracking algorithm to manage and track multiple detected objects across video frames.
- **Locking Mechanism**: Includes a timer-based locking mechanism that indicates successful locking onto a UAV after it remains within a designated region for a specified time.
- **Real-time FPS Display**: Shows the real-time frame rate of the video processing.
- **Recording**: Records the processed video with tracking annotations.

### Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/UAV-Tracking-and-Locking.git
    ```
2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Usage
1. Place the trained YOLOv5 model weights file (`weight.pt`) in the project directory.
2. Replace the input video file (`x.mp4`) with your desired video file.
3. Run the script:
    ```bash
    python uav_tracking.py
    ```

### Code Structure
- **Kalman Filter Initialization**: Initializes the Kalman filter with appropriate matrices for measurement, transition, process noise, and measurement noise.
- **Centroid Tracker Class**: Manages object registration, deregistration, and updates using centroid positions.
- **Main Loop**: Reads frames from the video, performs object detection, updates the tracker, and handles the locking mechanism.

### Future Work
- Enhance the locking mechanism with more sophisticated criteria.
- Improve the Kalman filter tuning for better prediction accuracy.
- Extend the software to handle multiple UAVs more efficiently.

### Contributions
Feel free to fork the repository and submit pull requests. All contributions are welcome!



