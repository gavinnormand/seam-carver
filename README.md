# Seam Carver

As part of my Fundamentals of Computer Science II course, my partner and I worked together to create an image editor that supports the [seam carving](https://en.wikipedia.org/wiki/Seam_carving) algorithm in order to reduce the dimensions of images. Seam carving works by removing individual seams, which are the paths of pixels that are least important to the image, on every tick until it reaches the desired size. 

## How the carving works
1. **Measure Pixel Importance (Energy)**
   - Assign each pixel an "energy" score based on how visually important it is.
   - Pixels with edges or contrast have high energy.
   - Flat or uniform areas have low energy.
   - The energy is calculated using brightness differences with neighboring pixels.

2. **Find the Least Important Seam**
   - A seam is a connected path of pixels (top-to-bottom for vertical seams, left-to-right for horizontal seams).
   - Compute the total energy for every possible seam.
   - Select the seam with the lowest total energy; this is the least noticeable path to remove.

3. **Remove That Seam**
   - Delete the pixels along the selected seam.
   - Shift the surrounding pixels to fill the gap.
   - This reduces the image width or height by one pixel while keeping important features.

4. **Repeat**
   - Recalculate pixel energies, since the image has changed.
   - Find and remove another low-energy seam.
   - Continue until the image is resized to the desired dimensions.

## This program allows users to: 
* Press the space bar to start/stop the carving.
* Press "v" or "h" while the carving is paused in order to remove a single vertical or horizontal seam.
* Press "u" at any time to begin reinserting the removed seams on every tick.
* Press "e" to toggle between seeing the actual colors of each pixel, or being able to see each pixel's energy.

*By instructor policy, source code can be accessed only by request.*



# [Click here or look below for a demo!](https://www.youtube.com/watch?v=iTsX2446KKE)


https://github.com/user-attachments/assets/0ede6d0d-c503-4da7-add4-50d33c3d3096

