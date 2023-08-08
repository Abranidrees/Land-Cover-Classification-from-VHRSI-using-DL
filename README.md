# Land-Cover-Classification-from-VHRSI-using-DL
## Introduction
Land cover (LC) represents the Earth’s surface features, which include water, soil, vegetation, and so on with their respective sub-groups. Accurate and timely LC
information is important for decision-making processes and resource management at various levels. However, LC mapping is often difficult and time-consuming with
the conventional approach. The increased availability of Very High-Resolution Satellite Imagery (VHRSI) has given precedent to deep learning (DL) in
supervised LC because of their ability to handle big data and produce more accurate results with a considerable balance between accuracy and computational time.
Among the various models of deep learning, Convolutional Neural Network (CNN) stands out as the most emblematic, characterized by its deeper architecture and remarkable learning capacity.

## Objectives
There are two major objectives of this project:
1. To identify Land Cover using the U-Net architecture​ of CNN.
2. To assess the performance of the U-Net model with and without data augmentation.

## Data and Pre-processing
Pleiades Imagery (0.5 m) of Hinton Canada is used for this DL project which is then subset to five patches. Four subset images with a size of 605 x 605 pixels are used for training, whereas one subset image is utilized for testing. To train the model, LC classes are manually digitized in the ArcMap environment, which serves as a mask layer, and converted to a raster format. After producing the mask layers for these five subset images, the masks and images have been further divided into small patches of pixel size 256 × 256 using the Geotile library in the Python environment.

# Workflow
![image](https://github.com/Abranidrees/Land-Cover-Classification-from-VHRSI-using-DL/assets/126249551/99dffb67-8908-4aa9-8287-b2a8523ad390)

# Results
Fig 1 shows the results of the land cover classification from the U-Net architecture, a very popular DL model CNN, applied on VHR satellite imagery. The input masks have 6 classes: road, building, needle leaf, broad leaf, barren land, and unlabeled. In this study, image segmentation has been done in two different ways. One is with only the original images. The rest is with both original and augmented images. Five types of augmentation have been applied which are center cropping, horizontal flip, vertical flip, random rotation, and grid distortion. As a result, there is a considerable difference in results between these two. Classification with augmented data is performed better than classification without augmented images. Fig 2 demonstrates that both curves of accuracy and loss produced in both the training and testing stages from data without augmentation have fluctuated highly. Even, the loss is increased (initial loss 0.86 and the final loss 0.98) and accuracy is decreased (initial accuracy is 0.72 and the final accuracy is 0.56) over epochs in the testing stage (Fig 2). On the contrary, using both the original and augmented images, both curves of accuracy and loss are comparatively smooth, produced in both the training and testing stages (Fig 3). The loss is decreased (initial loss is 1.94 and the final loss is 0.78) and the accuracy is increased (initial accuracy is 0.30 and the final accuracy is 0.75) in the testing stage (Fig 3). So, it can be stated that U-Net architecture performs better with larger data.
