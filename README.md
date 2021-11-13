# Ingenium_NeurAi
Repository for INGENIUM HACKATHON 2021 by team NeurAi

## Brain Tumor segmentation & 3D Reconstruction
The brain_tumor_segmentation_u_net.ipynb takes nifti as input and prdicts 3D segmented tumor mask.The predicted output mask is classified into:
* Not tumor = 0
* Necrotic/core =1
* Edema = 2
* Enhancing =3

The survival_prediction.ipynb takes Dicom files and other meta data of the patients and predicts the severity of the tumor along with the survival period:
* Long('Span >450')
* Short('Span 0-300 days')
* Medium('Span 300-450')
