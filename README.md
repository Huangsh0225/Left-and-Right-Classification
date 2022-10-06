# Left-and-Right-Classification

This repository contains the code to classify left or right eyes images.

The repository contain 2 main parts:

- Preprocessing

- Left or right eyes classification

Example data comes from Kaggle diabetic retionpathy detection, full data can be download at:

https://www.kaggle.com/c/diabetic-retinopathy-detection/data
  
# Preprocessing

To get a best result of classification, preprocessing is required.

Preprocessing contain 2 main parts:

- Cropping

- luminosity method and CLAHE


Since we only need the central part of images, here we need to crop a circle from our images,
here we used Canny to detect the biggest circle in the images and cropped it for further enhancement.

> Example of cropped image
![image](https://user-images.githubusercontent.com/114962712/194184607-3d0c6f39-3df4-4152-9f65-9ac486e5e105.png)

After images were cropped, we apply two method which has been proved its ability of increasing model's perfomance.

> Example of image enhancement
![image](https://user-images.githubusercontent.com/114962712/194184976-5083443f-3cd0-412f-9fbf-6a86c6b8e9e1.png)


# Left and right eyes classification

In classification part, three models were trained to do this task.

- ResNet50
- ResNet101
- DenseNet121

Deep Residual learning for Image Recognition: https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf

Densely Connected Convolutional Network: https://ieeexplore.ieee.org/document/8099726

Training dataset contains our private dataset and Kaggle diabetic retinopathy detection which has been mentioned above.

In order to get an more accuracy result, we do a majority voting by three models' result


> ResNet50's prediction on example data
![image](https://user-images.githubusercontent.com/114962712/194186630-abfbfea5-f1dd-44e8-8c2c-739fbfe09a5e.png)


> ResNet101's prediction on example data
![image](https://user-images.githubusercontent.com/114962712/194186686-6d7e04b6-584f-4452-925b-0ca8c7180e5c.png)


> DenseNet's prediction on example data
![image](https://user-images.githubusercontent.com/114962712/194186717-51545e45-a067-498e-a425-b39bfd066d6b.png)


> Final prediction
![image](https://user-images.githubusercontent.com/114962712/194186754-7ec3773c-0831-4bd2-8020-782179843ad8.png)


