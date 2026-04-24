# Leopard Detection and Deterrent System 🐆

An automated computer vision system powered by YOLO (Ultralytics) designed to detect leopards in both pre-recorded video files and live camera feeds. Upon detection, the system triggers an initial buzzer warning, followed by an active simulated light and sound deterrent to scare off the animal and alert nearby individuals.

**Model Accuracy:** This custom YOLO model achieves an impressive **88% accuracy** in detecting leopards.

## Features

* **High-Accuracy Detection:** Powered by custom-trained `best_leopard.pt` YOLO weights.
* **Dual Modes of Operation:** Includes scripts for processing pre-recorded videos and monitoring live camera/CCTV feeds.
* **Early Warning Buzzer:** Triggers a standard auditory beep the exact moment a leopard enters the frame.
* **Active Deterrent System:** Emits a continuous high-frequency alarm and flashes a bright red visual warning on the screen for as long as the animal remains in the frame.
* **Performance Optimized:** Utilizes frame-skipping (configurable) to run efficiently on standard CPU environments without requiring high-end GPUs.

## Included Scripts

* **`main.py`**: Designed for processing pre-recorded video files (`.mp4`, `.avi`, `.mov`). It opens a file selection dialog, processes the video, simulates the deterrent, and saves an annotated output file (`leopard_detected_output.mp4`).
* **`live_main.py`**: Designed for real-time monitoring. It connects directly to your webcam (or an RTSP IP camera stream) and runs continuously without saving video files to save local storage.

## Prerequisites

Ensure you have Python installed on your system. These scripts are currently designed for Windows environments due to their reliance on the built-in `winsound` library for audio deterrents.

Install the required dependencies using pip:

```bash
pip install ultralytics opencv-python
