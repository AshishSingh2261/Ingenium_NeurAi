# Ingenium_NeurAi
Repository for INGENIUM HACKATHON 2021 by team NeurAi

## Idea
Our idea for this hackathon is to segment tumor and healthy brain in Brain MRIs and then provide further analysis such as:
1. Volumetric analysis :- We are using methods like convexhull and Hounsfield unit counting to calculate volume of healthy brain  and the tumor.
2. Survivability :- Using the predictions made by our models and combining it with other metadata we are predicting the survivability of patients.
3. 3D Reconstruction :- We are creating a 3D model of the brain alongside the tumor so that it can be visualised better.

Our idea is aimed to be a simple to use and economically more feasible solution for underfunded medical institutes.

## Brain Tumor segmentation
The brain_tumor_segmentation_u_net.ipynb takes nifti as input and prdicts 3D segmented tumor mask.The predicted output mask is classified into:
* Not tumor = 0
* Necrotic/core =1
* Edema = 2
* Enhancing =3

## Survivability prediction
The survival_prediction.ipynb takes Dicom files and other meta data of the patients and predicts the severity of the tumor along with the survival period:
* Long('Span >450')
* Short('Span 0-300 days')
* Medium('Span 300-450')

## Inference and 3D Reconstruction
The notebook Volumetric_Analysis_and_3D_Reconstruction is the final notebook. It loads the trained model to segment the brain. It then continues to predict volumes of the tumor and healthy areas of brain and then finally gives the 3D reconstruction.

