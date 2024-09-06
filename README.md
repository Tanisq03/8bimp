
# 8-BIMP: Bitmap Image Processor

### Submitted By:
Tanishq Kumar Toliya

### Department of Computer Science and Engineering  
NATIONAL INSTITUTE OF TECHNOLOGY DELHI  
2023

---

## Table of Contents

1. [Introduction](#introduction)
2. [Motivation](#motivation)
3. [Methodology](#methodology)
4. [Flowchart](#flowchart)
5. [Different Functions](#different-functions)
   - [Negative Transformation](#negative-transformation-function)
   - [Image Rotation Clockwise](#image-rotation-clockwise-function)
   - [Image Rotation Anticlockwise](#image-rotation-anticlockwise-function)
   - [Image Flip Function or Mirror Image](#image-flip-function-or-mirror-image-function)
   - [Brightness Increase](#brightness-increase-function)
   - [Brightness Decrease](#dark-function)
   - [Rotate Image by 180°](#rotate-180-function)
6. [Results/Working](#results-working)
7. [References](#references)
8. [Conclusion](#conclusion)

---

## Introduction

The purpose of the report is to document the work of a project focused on image processing. The project involved the development of functions to perform various operations on images, including copying an image, creating a negative image, and rotating an image. These functions were implemented using appropriate image processing techniques and algorithms. The project was carried out without the use of external libraries, using built-in functions and algorithms available in C language.

In this project, our main objective was to apply different changes and processes to an image. Image processing is a very important task performed daily on almost all images for different purposes like copying, rotating, etc. We had to solve this problem using C language.

---

## Motivation

Image processing plays a crucial role in various fields, including photography, editing, computer vision, and medical imaging. The ability to manipulate images programmatically provides flexibility and opens up possibilities for enhancing, analyzing, and transforming visual data. The motivation behind developing this program was to provide a simple yet effective tool for performing basic image processing operations using the C programming language.

Some key reasons for learning image processing are:

1. **Practical applications**: Image processing is widely used technology with numerous applications in healthcare, entertainment, surveillance, etc.
2. **Career opportunities**: Data in any form is in huge demand, and images are one of the most popular forms, creating significant career opportunities.
3. **Advancements in technology**: With the rise of technology, new technologies such as AI and machine learning rely heavily on image processing.
4. **Research and innovation**: Image processing is a vibrant field, enabling contributions to new algorithms, techniques, and solving challenging problems.
5. **Creative expression**: Image processing can be intellectually stimulating and personally rewarding.

---

## Methodology

### Environment and Tools

The project was implemented using the C programming language without external libraries.  
The code editor used was Visual Studio on Windows.

### Bitmap Image

We used the bitmap image format in this project for its features such as:

1. High raw data
2. Lossless compression
3. Structured storage of data

An image is structured as follows:  
**Image header -> Colour table (if any) -> Image data**

The BMP image has a 54-byte image header, a 1024-byte colour table if present, and the rest is the image data.

#### Image Header:

We extract the required information from the image header:

- **Width**: Stored in the 18th bit.
- **Height**: Stored in the 22nd bit.
- **Bitdepth**: Stored in the 28th bit.

We read the colour table and allocate the block of memory as per the image size.

### Gray Scale Image:

We use a gray scale image for the functions. In a grayscale image, the pixel value ranges between 0-255. For example, to find the complement, we subtract the read image value from 255:  
`New_pixel_data = 255 – old_pixel_data;`

We are using the **Lena image** for displaying the output.

---

## Flowchart

### The flowchart below illustrates the flow of the program:

1. **Start of the program**
2. **Prompt for image file**
3. **Choose operation (loop)**
4. **Read image header/data**
5. **Perform chosen image operation**
6. **Create output file and write header/data for new image**
7. **Inform user and display output image file**
8. **Continue or exit (loop)**
9. **End of the program**

---

## Different Functions

### Negative Transformation Function

The negative transformation function creates a negative version of an input image.

### Image Rotation Clockwise Function

The image rotation function rotates an input image by 90 degrees in the clockwise direction.

### Image Rotation Anticlockwise Function

The image rotation function rotates an input image by 90 degrees in the anticlockwise direction.

### Image Flip Function or Mirror Image Function

This function outputs the mirror image of the input image.

### Brightness Increase Function

This function increases the brightness of the image. The user inputs a value `x` between -30 to +30. A positive value increases brightness.

### Dark Function

This function darkens the background of the image. It works similarly to the brightness increase function but uses a negative value for `x`.

### Rotate 180 Function

This function rotates the image by 180 degrees by performing two 90-degree rotations.

---

## Results/Working

This project allows users to choose from a set of image processing operations, including negative transformation, image rotation (90 and 180 degrees), adjusting brightness, and mirroring/flipping the image. The program reads an input image file, performs the selected operation, and creates an output file with the modified image. The output image is displayed, providing a visual representation of the processed image.

---

## References

1. [Negative Image using C](https://abhijitnathwani.github.io/blog/2017/12/21/Negative-Image-using-C)
2. *Image Processing in C*, Dwayne Phillips

---

## Conclusion

This report discussed a C program for image processing. The project involved developing and combining functions to perform various image operations such as copying, creating a negative version, rotating, flipping, and adjusting brightness. These tasks were successfully accomplished, and the image is displayed after each operation.

---

## Expected Errors

1. The user may try to run the program on a non-BMP image format.
2. The user may use a different bit depth BMP (e.g., 24-bit BMP).
3. The user may use a colour BMP instead of grayscale, which may cause unexpected outputs in brightness control functions.
