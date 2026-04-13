# MATLAB Lane Highlighting Simulation 🚗💻

## Overview
This repository contains a foundational video processing script built in MATLAB. It serves as a prototyping exercise to understand frame-by-frame video manipulation, matrix-level alpha blending, and static Region of Interest (ROI) masking before moving on to dynamic computer vision algorithms.

## What It Does
The script reads an input dashcam video (`22.mp4`), isolates the drivable road area using a predefined polygon mask, and outputs a new video (`roadHighlight.mp4`) with a transparent yellow overlay highlighting the lane.

## Key Features & Techniques
* **Frame Extraction:** Processes incoming `.mp4` video feeds frame-by-frame and converts them to grayscale (`rgb2gray`) for efficient masking.
* **Static ROI Masking:** Uses `poly2mask` with specific X and Y coordinates to generate a static binary mask over the lane.
* **Morphological Operations:** Applies morphological closing (`imclose` with a disk structuring element) to smooth and refine the generated mask.
* **Alpha Blending:** Uses matrix-level mathematics to blend a yellow visual overlay (`overlay`) with the original RGB frame at 50% transparency (`alpha = 0.5`).

## Tech Stack
* **Language:** MATLAB
* **Toolboxes Used:** Image Processing Toolbox, Computer Vision Toolbox (`vision.VideoPlayer`)

## How to Run
1. Clone this repository.
2. Ensure you have MATLAB installed along with the Image Processing and Computer Vision Toolboxes.
3. Place your input video named `22.mp4` in the same directory as the script.
4. Run the script.
5. The processed video will be saved in the directory as `roadHighlight.mp4`.

## Next Steps / Future Scope
This simulation establishes the foundational video input/output pipeline. The next iteration of this project will replace the static polygonal mask with dynamic lane detection algorithms utilizing Canny Edge Detection and Hough Transforms.
