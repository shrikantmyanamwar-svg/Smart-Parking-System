# Smart Parking System

## 1. Project Overview

The Smart Parking System is a computer vision-based application designed to
identify available and occupied parking spaces from a parking-lot video.

The application processes video frames, analyses predefined parking-space
regions, and displays the estimated occupancy status on a dashboard.

## 2. Objectives

- Detect empty and occupied parking spaces.
- Display parking availability in a web dashboard.
- Process video frames using OpenCV image-processing techniques.
- Store parking-space status information in a database.

## 3. Technologies Used

- Python
- OpenCV
- NumPy
- Flask
- SQLite
- HTML and CSS

## 4. Methodology

The current implementation uses traditional computer vision techniques.

The video frame is converted to grayscale and processed using Gaussian
blurring, adaptive thresholding, median filtering, and dilation.

Predefined parking-space coordinates are loaded from `source/CarParkPos.txt`.
The number of non-zero pixels in each processed parking region is counted
and compared with a threshold to estimate whether the space is empty or occupied.

The estimated status is displayed on the dashboard and can be stored in the
SQLite database.

## 5. Project Structure

- `main.py` - Starts the Flask application.
- `parking_detector.py` - Processes frames and estimates parking occupancy.
- `database_manager.py` - Manages database operations.
- `parking_data.db` - SQLite database file.
- `schema.sql` - Database schema.
- `source/carPark.mp4` - Parking video used by the application.
- `source/CarParkPos.txt` - Predefined parking-space coordinates.
- `templates/` - Web dashboard templates.
- `requirements.txt` - Python dependencies.

## 6. Setup Instructions

### Prerequisites

Install Python and pip.

### Install Dependencies

Create and activate a virtual environment, then run:

    pip install -r requirements.txt

### Run the Application

Run the following command from the project directory:

    python main.py

Open the local address displayed by the application in your web browser.
The current development configuration uses port 5001.

## 7. Dataset and Evaluation

The current application processes the parking video included in the project
and uses predefined parking-space coordinates.

A separate labelled dataset and a trained deep-learning model have not yet
been verified as part of this implementation. Dataset-based experiments and
quantitative evaluation must be documented only after they have actually
been performed.

## 8. Limitations and Future Work

- Evaluate the system on a labelled parking occupancy dataset.
- Measure classification performance using appropriate metrics.
- Investigate a trained deep-learning model for parking occupancy detection.
- Improve robustness under different lighting and weather conditions.
- Evaluate performance on additional parking-lot videos.

## 9. Original Project

This project was adapted from an existing project repository.

Original repository:
https://github.com/nandinireddy000/Open-Cv

Appropriate credit should be given to the original author and contributors.