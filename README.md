# Frame Extractor

A Python-based tool for efficiently extracting frames from `.mov` videos at fixed time intervals. Designed for preprocessing large video datasets for computer vision workflows.

---

## Overview

This script recursively scans a directory of videos, extracts frames at a specified time interval, and saves them into a single output folder with clean, consistent naming.

It supports parallel processing to improve performance when working with large datasets.

---

## Features

- Recursive video discovery across nested folders  
- Frame extraction at configurable time intervals  
- Parallel processing using multiple CPU cores  
- Clean, standardised file naming  
- Progress tracking with a real-time progress bar  
- Summary reporting of processed videos and saved frames  

---

## Tech Stack

- Python  
- OpenCV  
- concurrent.futures (parallel processing)  
- tqdm (progress tracking)  

---

## How It Works

1. Scans the input directory for `.mov` files  
2. Calculates frame intervals based on video FPS  
3. Extracts frames at fixed time steps  
4. Saves frames as `.jpg` files with structured naming  
5. Processes multiple videos in parallel for speed  

---

## Configuration

Update the following variables in the script:

```python
input_root = r"\Where\Your\Videos\Are"
output_folder = r"\Where\You\Want\To\Save\Frames"
frame_interval_seconds = 2
max_workers = 4
