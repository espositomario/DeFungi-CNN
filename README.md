# DeFungi-CNN
Microscopic Fungi Images Classification w/ Transfer Learning (EfficientNetV2)

## Data Introduction

***Reference:*** [Sopo et al. 2021, DeFungi: Direct Mycological Examination of Microscopic Fungi Images](https://arxiv.org/abs/2109.07322)  

***Data Repository:*** [UCI ML (Donated on 1/28/2023)](https://archive.ics.uci.edu/dataset/773/defungi) 

***Description:***
The real-world data was provided by LEMM, including 3,025 unlabeled images of superficial fungal infections caused by dermatophyte fungi, moulds, or yeasts. All the raw images were sourced from a Sony’s DSC W830 compact camera. After collection, patching, filtering, and additional data preprocessing steps were executed to make the images fit for fungal infection detection. An automated procedure was developed using Python programming language to generate 500 × 500 pixels patches for each image. This was done to filter out the insignificant regions in the raw images that did not contain any fungi. Further, noise and unwanted artifacts were also removed via this method. The final number of relevant images was ***9114***, with 4404, 2334, 819, 818, and 739 images belonging to TSH, BASH, GMA, SHC, and BBH classes, respectively.

***Data format:*** Images (500x500, RGB)

***Split strategy:*** 
- **Training set-----> 75% (6834)**
- **Validation set---> 15% (1364)** (To optimize hyperparameters and to monitor loss for early stopping)
- **Test set---------> 10% (916)** (Hold-out for final evaluation)

***Running time:*** ~1h30m (Apple M1 Pro w/ Metal GPU acceleration)
