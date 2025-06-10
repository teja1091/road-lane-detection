# road-lane-detection
## Code Overview

The core functionality is implemented in the `lane_detection` function, which orchestrates the following steps:

1.  **`preprocess_image(image)`**: Converts the image to grayscale, applies Gaussian blur, and detects edges using the Canny edge detector.
2.  **`region_of_interest(edges)`**: Masks the edge-detected image to focus on a specific region where lanes are expected to be found (typically the lower part of the image).
3.  **`detect_lines(edges)`**: Uses the Hough Transform to detect lines within the region of interest.
4.  **`display_lines(image, lines)`**: Draws the detected lines onto a copy of the original image.
5.  **`lane_detection(image_path, output_path)`**: Loads the image, applies the processing steps, and saves the resulting image.

## Functions

*   `preprocess_image(image)`: Preprocesses the input image for edge detection.
*   `region_of_interest(edges)`: Defines and applies a mask to focus on the relevant image area.
*   `detect_lines(edges)`: Detects line segments in the processed image.
*   `display_lines(image, lines)`: Overlays the detected lines onto the original image.
*   `lane_detection(image_path, output_path)`: Main function to perform lane detection on an image file.

## Example

Assuming you have an input image named `input.jpeg` in the `/content/sample_data/` directory, running the script will generate an `output.jpg` file with the detected lanes.
