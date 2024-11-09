
# Face Detection and Recognition

This project demonstrates face detection and recognition using OpenCV, focusing on detecting faces in images and videos. The Haar Cascade Classifier is employed to detect faces in real-time.

## Features

- **Face Detection in Images**: Detects faces in a set of predefined images and marks them with bounding boxes.
- **Face Recognition**: Displays names of identified faces alongside bounding boxes.
- **Face Detection in Videos**: Processes a video file to detect and highlight faces in each frame, saving the processed video.

## Demo

You can check the demo of the project in the provided [output video](output0.mp4) file after running the script.

## Prerequisites

- Python 3.x
- [OpenCV](https://opencv.org/)
- Matplotlib
- NumPy
- Pandas

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/face-detection-recognition.git
   cd face-detection-recognition
   ```

2. Install the required Python packages:
   ```bash
   pip install opencv-python
   pip install matplotlib
   pip install numpy
   pip install pandas
   ```

## Project Structure

```
face-detection-recognition/
├── nani.jpeg
├── KS.jpeg
├── PK.jpeg
├── SK.jpeg
├── VK.jpeg
├── input.mp4
├── output0.mp4
├── face_detection.py
├── README.md
```

## Usage

### 1. Face Detection in Images

To detect faces in images, run the `face_detection.py` script. It reads images from the current directory, detects faces, and displays the results with bounding boxes and names.

```python
python face_detection.py
```

#### Example:

You can load different images using:
```python
image1 = cv2.imread('nani.jpeg')
image2 = cv2.imread('KS.jpeg')
```

### 2. Face Detection in Videos

To detect faces in a video file, the script reads `input.mp4`, processes it to detect faces, and saves the output as `output0.mp4`.

#### Function Call:
```python
process_video()
```

### 3. Video Processing Example:

The `process_video()` function uses OpenCV to read frames from `input.mp4`, detect faces using Haar Cascade, draw bounding boxes, and save the output video.

```python
def process_video():
    video_path = "input.mp4"
    cap = cv2.VideoCapture(video_path)
    out = cv2.VideoWriter('output0.mp4', fourcc, 20.0, (int(cap.get(3)), int(cap.get(4))))
```

### Output

The output images display detected faces with bounding boxes and names of the individuals. Similarly, the processed video `output0.mp4` has bounding boxes around detected faces.

## References

- [OpenCV Haar Cascades](https://docs.opencv.org/4.x/db/d28/tutorial_cascade_classifier.html)
- [Face Detection using OpenCV](https://opencv.org/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- OpenCV for providing the Haar Cascade Classifier.
- Python community for extensive support with libraries like NumPy, Pandas, and Matplotlib.
