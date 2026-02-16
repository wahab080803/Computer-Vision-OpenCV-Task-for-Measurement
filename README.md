# Computer-Vision-OpenCV-Task-for-Measurement
Building a Coin Detection and Measurement system that uses Computer Vision to automatically identify objects in an image and calculate their real-world physical dimensions. By using a known reference object, the system successfully converted abstract image pixels into meaningful physical units like millimeters.

# start.ipynb

You implemented this logic twice, first as an exploratory script and then as a refined, final measurement pipeline:

Initial Image Pre-processing:
Loaded high-resolution images and performed essential transformations including Grayscale conversion, Gaussian blurring to remove noise, and Adaptive Thresholding to isolate the coins from their background.
Applied Canny Edge Detection and explored various HSV color masking techniques to identify specific object boundaries.

Contour Analysis & Filtering:
Implemented Contour Retrieval to find the edges of all objects and used area-based filtering (min_area = 700) to ignore small noise or artifacts in the image.
Utilized the minEnclosingCircle function to accurately find the geometric center and radius of each coin for precise diameter calculation.

Refined Measurement Pipeline (The 2nd Implementation):
Established a Conversion Factor by mapping the pixel area of a specific reference coin (ID 35) to its known real-world diameter of 18.0mm.
Automated the calculation for 10 different coins, generating a Final Measurement Report that labeled each object with its ID, area in pixels, and final diameter in millimeters (e.g., 19.0mm, 23.1mm).
Added a visual feedback layer by drawing green bounding boxes and blue text labels directly onto the final output image.
