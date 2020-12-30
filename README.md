# TooJpeg-Teensy4.1
A modification to tooJpeg by Stephan Brumme  to allow compression of YCbCr images from OV7670

The original required RGB888 input.  For the Teensy 4.1, this meant converting either an RGB565 or YUV422 image to RGB888 format using the Pixel Pipeline.   
This required about 100 milliseconds and a 921KB buffer in EXTMEM to hold the RGB888 image.  While directly compressing  the camera YUV422 output
is not significantly faster, it does save a 100 milliseconds of conversion time and the necessity for the RGB888 buffer.
