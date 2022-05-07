
# AIR BOARD
# Description
Air Board is a hands-free digital drawing canvas that utilizes a PiCamera, and OpenCV to recognize and map hand gestures onto user’s screen.
# Implementation
The things required to do are 

1)Building canvas on the screen:
To put the ink&clear buttons(color options) for writing/drawing purpose.

2)Building a mask for our pointer:for computer to recognise the pointer, so for that 
converted the frame into hsv color space and created a trackbar in the Canvas and we should  adjust the trackbar values so as to identify a particular object. For example if our pointer is a blue object then we have to set the values in trackbar as:

Upper hue=153/180

Upper saturation=255/255

Upper value=255/255

Lower hue=64/180

Lower saturation=72/255

Lower value=49/255

3)Drawing contours to the detected mask:

With the help of detecting the contours around the pointer the bigger radius of the formed contour's radius will be the current_value of the pointer 

<img width="507" align="center" alt="image" src="https://user-images.githubusercontent.com/87426240/167252263-ca6cdc6f-b535-499e-9eb0-aaf8bad58bb9.png">

4)Storing the center value of the contour in a data structure(I used Deque array):

The current_value’s would be stored into a deque data structure for storing purposes and further color manipulation. For every color we mentioned in the canvas there should be a deque so that according to the threshold values of color and the current_value the coordinates would store in the respective color’s deque and futher color can be manipulated according to that.

<img width="300" align="center" alt="image" src="https://user-images.githubusercontent.com/87426240/167252251-cb1d57d7-4914-47e9-aaeb-4588b9923607.png">

# Conclusion
So totally we should be showing 3 windows when the program runs and they are the original frame where the camera accesses, the HSV color space where the object recognition takes place and mask forms and the third window is the HSV trackbar for adjusting the hsv values to detect the object/pointer. 
Hence the goals I set out to accomplish and learned a considerable amount about OpenCV, multicore processing, and programming in the process and we can do the drawing and writing over air and see the results on the screen

# Further developments
Further we can make a stable place than air cause we cannot write properly on air without support so one of my ideas where placing a transparent board or screen where we can write by placing our hand and still the computer should identify the pointer/pen/object.
With this idea of using free hands and objects and creating some changes over the system being as a side component we can even include this in many fields like we can modify this concept into Augmented reality, It is also useful for Architects. 
