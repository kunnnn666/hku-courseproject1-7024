# CIVL7024 Assignment 1: Image Processing and 3D Reconstruction

Course project repository for **CIVL7024 Computer Vision for Infrastructure Construction and Management** (The University of Hong Kong, **Group 12**).

## Repository Contents
- **`A1_solution.ipynb`**: Main Jupyter Notebook with all Python implementations, embedded figures, and discussions for Part I and Part II.
- **`Part2_3D_Reconstruction.ply`**: 3D colored surface model (589,901 vertices, 1,172,457 faces) reconstructed from 52 self-collected multi-view photographs using COLMAP.

## Summary of Tasks
1. **Part I - Q1 (Quebec Bridge Image Processing)**:
   - Downsampling to 1/4 pixel count, bilinear upsampling, and full-reference quality evaluation (`MAE`, `PSNR`, `SSIM`).
   - Spatial filtering comparison (`Box`, `Gaussian`, and `Bilateral` filters).
   - Frequency-domain low-pass and high-pass filtering via 2D FFT.
   - Custom multi-stage Canny edge detector built from Gaussian smoothing, Sobel gradients, subpixel non-maximum suppression, and hysteresis thresholding.
2. **Part I - Q2 (Tung Ping Chau Image Stitching)**:
   - Grayscale conversion and Harris corner detection.
   - `SIFT` keypoint/descriptor extraction, `BFMatcher` with Lowe's ratio test, `RANSAC` homography estimation, perspective warping, and feather-blended panorama generation.
3. **Part II (3D Reconstruction & Self-Collected Pair Stitching)**:
   - COLMAP sparse Structure-from-Motion (52/52 views registered), CUDA PatchMatch Multi-View Stereo, and Screened Poisson surface reconstruction on a plush puppy dataset.
   - Pairwise homography stitching on adjacent self-collected views using the Part I pipeline.

## How to View
- **`A1_solution.ipynb`**: View directly on GitHub or open in VS Code / Jupyter Notebook (all output plots are embedded).
- **`Part2_3D_Reconstruction.ply`**: Open in [MeshLab](https://www.meshlab.net/), [CloudCompare](https://www.cloudcompare.org/), or drag directly into [3dviewer.net](https://3dviewer.net/).