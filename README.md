

# DeFungi-CNN

***Aim:*** Classify images of 5 species of microscopic fungi which cause Dermatomycosis (fungal skin infections)

***Strategy:***  CNNs w/o Augmentation and transfer learning with EfficientNetV2 models

***Results:*** ENv2-B0 as best model with a Macro-F1 = 0.86 on test set

---

***Reference:*** [Sopo et al. 2021, DeFungi: Direct Mycological Examination of Microscopic Fungi Images](https://arxiv.org/abs/2109.07322)  

***Data Repository:*** [UCI ML (Donated on 1/28/2023)](https://archive.ics.uci.edu/dataset/773/defungi) 

***Data description:***
The real-world data was provided by LEMM, including 3,025 unlabeled images of superficial fungal infections caused by dermatophyte fungi, moulds, or yeasts. All the raw images were sourced from a Sony’s DSC W830 compact camera. After collection, patching, filtering, and additional data preprocessing steps were executed to make the images fit for fungal infection detection. An automated procedure was developed using Python programming language to generate 500 × 500 pixels patches for each image. This was done to filter out the insignificant regions in the raw images that did not contain any fungi. Further, noise and unwanted artifacts were also removed via this method. The final number of relevant images was ***9114***, with 4404, 2334, 819, 818, and 739 images belonging to TSH, BASH, GMA, SHC, and BBH classes, respectively.

***Data format:*** Images (500x500, RGB)

***Split strategy:*** 
- **Training set-----> 75% (6834)**
- **Validation set---> 15% (1364)** (To optimize hyperparameters and to monitor loss for early stopping)
- **Test set---------> 10% (916)** (Hold-out for final evaluation)

***Running time:*** ~1h30m (Apple M1 Pro w/ Metal GPU acceleration)

---

- **Introduction**
  - **Five types of fungi**
  - **Import libraries**
  - **Define functions**
  - **Metrics Computed per Individual Class**
  - **Macro-F1**
  - **Download and split data**
  - **Setup plotting parameters**
  - **Setup data parameters**
  - **ImageDataGenerator**
  - **Class distribution (imbalanced)**
  - **View some random selected images for each class**
- **CNN**
  - **Class weights**
  - **EarlyStopping**
  - **ReduceLROnPlateau**
- **CNN(+ Dropout + Augmentation)**
  - **Augmentation**
  - **Visualize augmented images**
  - **Dropout**
- **Transfer learning**
  - **EfficientNetV2B0 (6M)**
    - **Feature extraction**
    - **Fine-tuning *(unfreeze last layers weights)***
  - **EfficientNetV2S (20M)**
    - **Feature extraction**
    - **Fine-tuning *(unfreeze last layers weights)***
- **Evaluate the best model on Test set (Hold-out)**

---

For reproducibility all **packages and versions** in ```conda.yml```
