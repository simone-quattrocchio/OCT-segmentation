# OCT Organoid Segmentation with Deep LearningThis repository contains python code for segmentation of tumor organoids in a volume of OCT medical images (Optical Coherence Tomography).
This project focuses on the **automated segmentation of 3D tumor organoids** in volumetric **Optical Coherence Tomography (OCT)** images using deep learning techniques.
This is done by using a pipeline that starting from raw 16-bit volumes returns the corresponding binary masks of each slice; the pipeline is made up of: (1) a first prepocesssing step, (2) application of deep learning model and (3) postprocessing.
The deep learning model is trained by using PyTorch framework and UNet inspired architetture
The deep learning algorithm was trained on control volumes in which organoids were grown over several weeks. 
## 🔍 Objective

To develop and evaluate a **3D segmentation pipeline** capable of identifying and counting organoids in noisy, high-resolution OCT scans using:

- U-Net and U-Net++ architectures
- Preprocessing techniques (denoising, CLAHE)
- Data augmentation (Albumentations)
- Morphological post-processing
- Dice coefficient and count error metrics

## 🧠 Model

Two models were implemented:
- **U-Net** (standard)
- **U-Net++** (Zhou et al.)

Training was performed with PyTorch using both **Dice Loss** and **Binary Cross Entropy**, with early stopping and data balancing strategies.

## 📊 Results

- Best model: **U-Net++ + BCE Loss**
- Average Dice 3D score: **~0.87**
- Organ count error reduced with **opening morphological filter**
- Data preprocessing and postprocessing had a greater impact than architecture choice

## Usage
For importing the model and use the trained weights use 'Submission.ipnyb/' and download the wieghts 'final_checkpoint.pth/' and follow instruction; note that the format of data must be coherent with the trained data (16 bit precision .mat file with 800x1200 dimensions) and quality of detection depends on similarity to trained data.

## 📁 Project Structure

See `src/` for full implementation details.

## 📘 Report

For full documentation (in Italian): `Challenge_OCT_Gruppo FB14 Relazione.pdf/'

## 👨‍💻 Author

**Simone Quattrocchio**  
MSc Biomedical Engineering – Politecnico di Torino  
[LinkedIn](https://www.linkedin.com/in/simone-quattrocchio-468428234/)
