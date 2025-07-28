🧬 OCT Organoid Segmentation with Deep Learning
This repository contains Python code for the automated segmentation of 3D tumor organoids in Optical Coherence Tomography (OCT) volumetric images using deep learning techniques.

The proposed pipeline takes raw 16-bit OCT volumes and produces corresponding binary masks for each slice. The main stages are:

Preprocessing

Deep learning-based segmentation

Postprocessing

The model is implemented using the PyTorch framework and is based on U-Net-inspired architectures.

⚠️ Due to privacy restrictions, training data and final results cannot be displayed. However, the model weights are provided for use on similar datasets.

🔍 Objective
To develop and evaluate a 3D segmentation pipeline capable of identifying and counting organoids in noisy, high-resolution OCT volumes. The approach integrates:

U-Net and U-Net++ architectures

Preprocessing (e.g., denoising, CLAHE)

Data augmentation using Albumentations

Morphological postprocessing

Evaluation using Dice coefficient and count error metrics

🧠 Model Overview
Two architectures were implemented and compared:

U-Net (baseline)

U-Net++ (Zhou et al.)

Training details:

Loss functions: Dice Loss + Binary Cross Entropy (BCE)

Framework: PyTorch

Additional strategies: early stopping, class balancing, and augmentation

<p align="center"> <img width="1003" height="335" alt="model" src="https://github.com/user-attachments/assets/4d03c847-1130-4644-a1e6-5e81706f131f" /> </p>
📊 Results Summary
Best-performing model: U-Net++ with BCE Loss

Average 3D Dice Score: ~0.87

Organ count error reduced using morphological filters

Pre/post-processing steps had greater impact than architecture choice

<p align="center"> <img width="710" height="297" alt="results" src="https://github.com/user-attachments/assets/aa22fdc0-7fb6-42c5-a61a-c3c156dbc84d" /> </p>
🚀 Usage
To use the trained model:

Open Submission.ipynb

Download the model weights (available on request)

Ensure your data is in the correct format:

.mat file

16-bit depth

800x1200 resolution

Follow the notebook instructions to run inference.

⚠️ Detection performance depends on the similarity of input data to the training distribution.

📁 Project Structure
Folder	Description
estrazione dataset/	Prepares and organizes the raw dataset
datasplit/	Splits data into training, validation, and test sets
allenamento_rete_neurale/	Model training, augmentation with Albumentations, loss/metric setup
calcolo_performance/	Evaluation: Dice score and organoid count error
slicer/	Exports results for visualization in 3D Slicer

📘 Report
For full technical documentation (in Italian):
📄 Challenge_OCT_Gruppo FB14 Relazione.pdf

👨‍💻 Author
Simone Quattrocchio
MSc Biomedical Engineering – Politecnico di Torino
🔗 LinkedIn
