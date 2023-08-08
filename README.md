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
Pleiades Imagery (0.5 m) of Hinton Canada is used for this DL project which is then subset to five patches. Four pixel-sized subset picture patches (605 x 605) are used for training, whereas one patch of the same size is utilized for testing. To train the model, LC classes are manually digitized in the ArcMap environment, which serves as a mask layer, and converted to a raster format. After producing the mask layers for these five subset images, the masks and images have been further divided into small patches of pixel size (256 × 256).
