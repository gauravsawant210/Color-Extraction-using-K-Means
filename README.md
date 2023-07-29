# Image Color Palette Extraction using K-Means Clustering

This project demonstrates how to extract a color palette from an image using the K-Means clustering algorithm. The main goal is to identify dominant colors in an image and create a visually appealing color palette based on those colors.

## Table of Contents
- [Introduction](#introduction)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Explanation](#explanation)
- [Example](#example)
- [Contributing](#contributing)
- [License](#license)

## Introduction
In this project, we use K-Means clustering, an unsupervised machine learning algorithm, to partition the pixels of an image into K clusters. Each pixel is considered an individual data point with RGB values. By applying K-Means clustering to the RGB values of image pixels, the algorithm identifies cluster centroids that represents a dominant color in the image. By using K-Means clustering, we can effectively extract the most prevalent colors in the image and create a color palette based on them.

## Dependencies
To run this project, you need the following libraries:
- NumPy
- Pandas
- Matplotlib
- Scikit-Image
- Scikit-Learn
- PIL

You can install these libraries using pip:
```
pip install numpy pandas matplotlib scikit-image scikit-learn pillow
```


## Usage
1. Clone this repository to your local machine or download the files as a ZIP archive.
2. Make sure you have the required dependencies installed (see Dependencies section).
3. Run the provided script to see the color palette extracted from a sample image.

## Explanation
The code in `main.ipynb` extracts the color palette from an image using two different approaches. It uses K-Means clustering to group the pixels by color similarity. Here's a brief explanation of the code:
1. Import the necessary libraries, including NumPy, Pandas, Matplotlib, Scikit-Image, Scikit-Learn, and PIL.
2. Load the image from a URL using the `imageio.imread()` function from the Scikit-Image library.
3. Resize the image to a smaller size (e.g., 200x200 pixels) to speed up the clustering process.
4. Convert the image data into a Pandas DataFrame, where each row represents a pixel's RGB values.
5. Perform K-Means clustering on the image data to assign each pixel to one of the predefined clusters (in this case, 6 clusters).
6. Extract the cluster centers, which represent the dominant colors in the image, and store them in the `palette` variable.
7. Display the color palette by showing each dominant color in a separate image using Matplotlib.
8. Perform another K-Means clustering approach, but this time, the image is loaded and processed using the PIL library. Through a K-Means clustering approach, we identify the most dominant colors present in the image, and then apply quantification as a lossy compression technique. This quantification process involves grouping a range of color values together, effectively reducing the total number of colors needed to represent the image. As a result, the file size of the image decreases significantly. This compression is particularly valuable for displaying images on devices that support only a limited number of colors, optimizing their visual representation without compromising essential details.


## Contributing
Feel free to contribute to this project by opening issues or submitting pull requests. Any feedback or improvement is appreciated.
