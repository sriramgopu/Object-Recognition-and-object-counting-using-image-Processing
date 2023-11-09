# Object-Recognition-and-object-counting-using-image-Processing
This code is a Python script that uses the OpenCV library to detect and label objects in an image. Specifically, it identifies and counts phones, pens, and books in the given image. Below is an explanation of each section of the code along with some details:

Importing Libraries
This section imports the necessary libraries for image processing, including OpenCV (cv2), numpy, and a function (cv2_imshow) from the Google Colab library for displaying images.

Detect Phone
This section focuses on detecting phones in the image:

The image is loaded using cv2.imread('image.png').
The loaded image is converted to the HSV color space, which is better for color-based object detection.
Lower and upper color range values are defined for the phone. These values represent a range of hues (color), saturation, and value.
A mask is created to identify regions in the image that match the color range specified for the phone.
Morphological operations (opening) are applied to the mask to enhance phone detection.
Contours of the detected phone regions are found.
Bounding boxes are drawn around the detected phones, and labels are added to them.
The count of detected phones is displayed along with the image.
Detect Pens
This section focuses on detecting pens in the image:

The same image is loaded and converted to the HSV color space.
Lower and upper color range values are defined for the pen, representing a range of hues, saturation, and value.
A mask is created for the pen based on the specified color range.
Morphological operations are applied to the pen mask to enhance pen detection.
Contours of the detected pen regions are found.
Bounding boxes are drawn around the detected pens, and labels are added to them.
The count of detected pens is displayed along with the image.
Detect Books
This section focuses on detecting books in the image:

The same image is loaded and converted to the HSV color space.
Lower and upper color range values are defined for books. In this case, there are multiple color range definitions for different shades of the book covers.
An empty mask for books is initialized, and the masks for different book shades are combined using a bitwise OR operation.
Morphological operations are applied to the book mask to enhance object detection.
Contours of the detected book regions are found.
Bounding boxes are drawn around the detected books, and labels are added to them.
The count of detected books is displayed along with the image.
Display
At the end of each section, the script uses cv2_imshow to display the image with bounding boxes and labels around the detected objects. To use this code, upload it to Google Colab and use "image.png" for testing purposes.

