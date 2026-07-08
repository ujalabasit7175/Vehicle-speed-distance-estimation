# Vehicle Speed & Distance Estimation using YOLOv8

## Overview

This project detects, tracks, and estimates the speed and distance between vehicles in traffic videos using Computer Vision techniques.

The project combines:

- YOLOv8 for vehicle detection
- ByteTrack for multi-object tracking
- Perspective Transformation for Bird's-Eye View conversion
- OpenCV for visualization
- Supervision library for tracking utilities

---

## Features

- ✅ Vehicle Detection
- ✅ Multi-Object Tracking
- ✅ Speed Estimation (km/h)
- ✅ Vehicle-to-Vehicle Distance Estimation (meters)
- ✅ Region of Interest (ROI) Filtering
- ✅ Perspective Transformation (Bird's-Eye View)

---

## Technologies Used

- Python
- OpenCV
- Ultralytics YOLOv8
- Supervision
- NumPy
- ByteTrack

---

## Project Workflow

```text
Input Video
      │
      ▼
YOLOv8 Detection
      │
      ▼
ByteTrack Tracking
      │
      ▼
ROI Filtering
      │
      ▼
Perspective Transformation
      │
      ▼
Speed Estimation
      │
      ▼
Distance Estimation
      │
      ▼
Annotated Output Video
```

---

## Installation

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Usage

1. Add your own traffic video.
2. Update the video path:

```python
SOURCE_VIDEO_PATH = "your_video.mp4"
```

3. Update the ROI coordinates according to your video:

```python
SOURCE = np.array([
    ...
])
```

4. Update the real-world road dimensions:

```python
ROAD_WIDTH = ...
ROAD_LENGTH = ...
```

5. Run the notebook.

---

## Output

The notebook generates an annotated output video containing:

- Vehicle Bounding Boxes
- Vehicle Speed (km/h)
- Distance Between Nearby Vehicles (meters)

---

## Notes

- ROI coordinates must be adjusted for your own video.
- Road width and road length should be measured according to the real-world road for accurate speed and distance estimation.
- Results may vary depending on camera angle and calibration accuracy.
