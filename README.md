🚗 Vehicle Detection and Traffic Analytics System

Creator / Developer: Shubham Mehrotra

A real-time vehicle detection, tracking, and traffic analytics system built using Python and computer vision techniques. The system processes traffic videos or live webcam feeds to detect vehicles, track them with unique IDs, estimate speed, flag over-speeding, and generate analytics.

📌 Project Overview

This project uses YOLOv8 for vehicle detection and SORT for tracking to provide real-time traffic insights such as:

Vehicle detection (car, bus, truck, bike)

Unique ID-based tracking

Speed estimation

Over-speeding detection

Vehicle counting (no double counting)

Data logging and visualization

It is designed to be modular, scalable, and suitable for research or smart traffic applications.

🛠️ Tech Stack

Python 3.9+

OpenCV

NumPy

YOLOv8 (Ultralytics)

SORT (Simple Online and Realtime Tracking)

Pandas

Matplotlib

✨ Features

Load traffic video or live webcam feed

Detect vehicles: car, bus, truck, bike

Track vehicles using SORT (unique IDs)

Accurate vehicle counting

Speed estimation using frame-based motion

Over-speeding flagging

Real-time bounding boxes with:

Vehicle ID

Class label

Estimated speed

Log analytics to CSV

Generate bar graph of vehicle counts

Handles multiple vehicles and partial occlusion

📐 Speed Calculation Logic

Vehicle speed is estimated by tracking the movement of a vehicle’s centroid between consecutive frames.

Formula:

Speed (km/h) = (distance_pixels × pixel_to_meter × FPS) × 3.6

Assumptions:

Pixel-to-meter conversion is predefined

FPS is obtained from the video source

Speed is an approximation, not radar-accurate

▶️ How to Run
1️⃣ Prerequisites

Python 3.9 or higher

Install required dependencies:

pip install opencv-python numpy ultralytics pandas matplotlib

2️⃣ Run the Application
▶️ Using a video file:
python main.py --source path/to/video.mp4

▶️ Using webcam:
python main.py --source 0
