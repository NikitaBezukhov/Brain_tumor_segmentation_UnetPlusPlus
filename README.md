# MRI brain tumor semantic segmentation with PyTorch Unet++! (ResNet101 backbone)
####
### The dataset is __[Brain MRI segmentation from Kaggle](https://www.kaggle.com/mateuszbuda/lgg-mri-segmentation)__.
### Was built in __[Google Colab](https://colab.research.google.com/)__ environment, so make any adjustments needed for it to work on your machine.
### You can find code and detailed project analysis in __[brain_tumor_segmentation.ipynb](https://github.com/NikitaBezukhov/Brain_tumor_segmentation_UnetPlusPlus/blob/main/brain_tumor_segmentation.ipynb)__ notebook.
### The results of the training will be presented below.
## Dataset consists of 3929 unique MRI brain scans and corresponding ground truth masks of patients with and without brain tumor. 
## Model stopped training after 312 epochs (around 9 hours on 1 Tesla V100 GPU) with Early stopping point at 262 epochs. 
## Resulting training metrics were:
![Screenshot_1](https://user-images.githubusercontent.com/74721678/127385763-67944f57-2ea2-477e-b7e5-5f05517fff18.png)
![Screenshot_2](https://user-images.githubusercontent.com/74721678/127385798-c1e5e8aa-63c6-4ce4-8e69-3256d79b7976.png)
![Screenshot_5](https://user-images.githubusercontent.com/74721678/127385820-31cae37a-487d-4e01-86eb-652f6d1a9c2e.png)
![Screenshot_6](https://user-images.githubusercontent.com/74721678/127385825-3f3540ad-7c5b-4019-84e5-a764ba80e6aa.png)
![Screenshot_7](https://user-images.githubusercontent.com/74721678/127385834-3037dd78-80ec-424b-afd4-76f9d704a22e.png)
### Also if we use our model as a classifier (look at how many tumors we predicted when there were none and backwards, etc.) we can calculate TP, TN, FP and FN, Recall, Precision and F1 score:
![Screenshot_3](https://user-images.githubusercontent.com/74721678/127385928-33f9a923-0bdf-4468-a780-f44a3824415e.png)
![Screenshot_4](https://user-images.githubusercontent.com/74721678/127385936-11cb8a4b-852a-4db7-b18a-50b354756cd8.png)
### So this means that we predicted 94.4% out of all the scans with tumors (not necessarily each tumor in every scan) and 96.6% of scans we predicted to have tumor, had it. 
### Below you can see examples of model performance:
![prediction_77](https://user-images.githubusercontent.com/74721678/127386248-99c3a599-dde3-4720-ba01-849eaf062afa.png)
![prediction_2](https://user-images.githubusercontent.com/74721678/127386251-40ee3cab-f930-42c7-8ede-22e4481b7860.png)
![prediction_3](https://user-images.githubusercontent.com/74721678/127386254-50c5791a-99f7-4f5c-b399-b1078d959d4f.png)
![prediction_4](https://user-images.githubusercontent.com/74721678/127386255-fa5947a8-a103-4f2b-9bf8-e77b549b0f15.png)
![prediction_14](https://user-images.githubusercontent.com/74721678/127386257-889a9f50-ec32-46b1-9011-257a56b9f4a7.png)
![prediction_16](https://user-images.githubusercontent.com/74721678/127386258-01282ea5-2caa-4f0f-a7cb-f68c1c43a37a.png)
![prediction_23](https://user-images.githubusercontent.com/74721678/127386261-3457b2c3-ec6b-4451-b4a8-17101ee25181.png)
![prediction_29](https://user-images.githubusercontent.com/74721678/127386265-b46c70e9-51be-4468-b8f9-069e7b9168cf.png)
![prediction_40](https://user-images.githubusercontent.com/74721678/127386268-78b204a9-59b6-4c48-babb-73b29a850d8b.png)
![prediction_41](https://user-images.githubusercontent.com/74721678/127386270-f71eb8cc-6975-4e1f-bd24-8f82019cd888.png)


