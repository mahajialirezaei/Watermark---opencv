# Watermark opencv

This project demonstrates a method for removing watermarks from images using image processing techniques with OpenCV and Matplotlib in Python. The code loads an original image and a watermarked version of that image, computes the difference, and then processes the images to remove the watermark.

## Requirements

To run this project, you need to have the following libraries installed:

- OpenCV
- NumPy
- Matplotlib

You can install these libraries using pip:

bash
pip install opencv-python numpy matplotlib

## How It Works

1. **Load Images**: The original and watermarked images are loaded from specified file paths.
2. **Convert Color Space**: Both images are converted from BGR (OpenCV default) to RGB for proper display using Matplotlib.
3. **Display Images**: The original and watermarked images are displayed side by side for comparison.
4. **Calculate Difference**: The difference between the watermarked image and the original image is computed to identify the watermark.
5. **Convert to Grayscale**: The difference image is converted to grayscale to simplify further processing.
6. **Thresholding**: A binary mask of the watermark is created using thresholding, where pixel values above a certain threshold are set to white (255) and others to black (0).
7. **Create 3-channel Mask**: The binary mask is converted to a 3-channel format to allow for bitwise operations with color images.
8. **Invert Mask**: The binary mask is inverted so that the watermark area becomes black, allowing the original image to be combined with the non-watermarked parts.
9. **Bitwise Operations**:
   - The bitwise AND operation is performed between the watermarked image and the inverted mask to isolate the non-watermarked areas of the watermarked image.
   - Another bitwise AND operation is performed between the original image and the binary mask to extract the watermark area from the original image.
10. **Combine Results**: The results from the two bitwise operations are added together to form the final image, which should have the watermark removed.
11. **Display Final Image**: The final image is displayed, showing the result of the watermark removal process.

## Usage

To use this code:
1. Place your original image as ori.png and your watermarked image as wa.png in the ../Data/ directory relative to your script.
2. Run the Jupyter Notebook cells sequentially to process the images and visualize each step.

## Example Output

The output will include:
- The original image
- The watermarked image
- The difference between the two images
- The grayscale difference
- The binary mask of the watermark
- The inverted mask
- The intermediate results after bitwise operations
- The final image with the watermark removed

## Acknowledgements

This project utilizes OpenCV for image processing and Matplotlib for visualization. For more information on these libraries, please refer to their official documentation:
- [OpenCV Documentation](https://docs.opencv.org/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)


## 🛠 Developer

Developed by [Mohammad Amin Haji Alirezaei](https://github.com/mahajialirezaei)
Feel free to ⭐️ this repo or open an issue if you'd like to contribute or have questions!
