# Background-Substraction---Image-processing
The aim of this project is to enhance a neuro-intervention video to improve the visualization of moving tools. We will develop a pipeline of methods to create a binary mask for each input image. These masks will enable tracking the movement of the specific tool.


In the following, the construction of the pipeline will rely on the following steps:

• Background Subtraction:
This initial step involves producing an image with the moving tool + noise. It is necessary to remove the noise before proceeding to segmentation, known as preprocessing.

• Image Preprocessing:
Intelligent use of image preprocessing is crucial for solving problems and ultimately achieving better detection of desired features. Various methods will be explored to determine the best combination of transformations/filters that positively impact segmentation results.
Based on common methods in medical image processing, the following families of methods will be explored:

Intensity (histogram) transformations: Gamma correction, histogram equalization, intensity rescale.
Spatial filtering:
o Low-pass filtering for pre-segmentation and noise reduction.
o High-pass filtering, bilateral filtering, and Laplacian filtering for contour detection.
Frequency filtering:
o Gaussian or Butterworth filters (high-pass or low-pass as needed).

• Segmentation:
Now the goal is to produce the binary mask using one of the known segmentation methods like Otsu, Canny, etc. It is advisable to explore global and local thresholding methods and choose the ones that perform the best.

• Morphological Transformation:
Regardless of the quality of the preprocessing phase, some noise will persist in the final binary mask. Morphological transformations such as erosion and opening help reduce this noise and improve the final mask. Additionally, "Skeletonization" may be considered to produce finer features like manual masks.
