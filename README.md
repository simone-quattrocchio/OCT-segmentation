# OCT-segmentation
This repository contains python code for segmentation of tumor organoids in a volume of OCT medical images (Optical Coherence Tomography).
It is implemented by using a pipiline that starting from raw 16-bit volumes returns the corresponding binary masks of each slice; this is achieved by a first prepocesssing step, application of deep learning model and postprocessing.
The deep learning model is trained by using PyTorch framework and UNet inspired architetture
The deep learning algorithm was trained on control volumes in which organoids were grown over several weeks. 
