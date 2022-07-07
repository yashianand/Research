# Master's Thesis

The aim of this work is to preserve the private information in every view of an object while utlizing the public information for any further machine learning tasks. We present a machine learning framework that achieves these two competing objectives in a distributed and resource constrained environment. In this work, we develop a data sanitizing algorithm as an interplay between the two competing objectives.

The dataset used is a synthetic 2-digit dataset derived from MNIST. Multiple views of an image in this dataset was created by cropping the image. The images resulted from the crop function are used as the input to the model. In the resulting 2-digit dataset, all the even numbers in the dataset were considered to be public information and all the numbers that are equal to or greater than 10 were considered to be private information. The ground truth of the dataset contains the private and public labels (marked 0/1, positive samples are marked 1 and negative samples are marked 0)

Note:
1. 'Private Model' classifies information as private or non-private while the 'Public Model' classifies information as public or non-public. 
2. A single image can contain both private and public information. A high accuracy for the public model means that the public information was correctly indentified. An ideal private model should have a 50% accuracy, meaning that the model can neither classify the information as private nor public.

The output features of an ideal sanitizer would make it impossible for even the best private detector to detect a private information while the public detector can correctly detect a public information.
