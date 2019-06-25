# CancerClassification

Accurately identifying and categorizing breast cancer subtypes is an important clinical task, and automated methods can be used to save time and reduce error. This is what i attemp to do in CancerDetection.ipynb.
 
Invasive Ductal Carcinoma (IDC), the most common of all breast cancer. The dataset was originally curated by Janowczyk and Madabhushi and Roa et al. but is available in public domain linked below on Kaggle’s website.

![](https://github.com/Carl-E-B/breast-histopathology-detection/blob/master/8863_idx5_x1051_y1051_class1.png)

The dataset containes:
- 198,738 negative examples (i.e., no breast cancer)
- 78,786 positive examples (i.e., indicating breast cancer was found in the patch)

*NB: To save gpu computation time, several suboptimal modifications were made. Such as only using 50x50 pixel specimens, undertraining the model for only 7 epochs before full convergence, further focusing on the specimens with the most losses(plotted in the notebook) and only using a resnet34 instead of a deeper resnet such as the resnet50. The current model took 11 hours to train, with optimal code the computation time would be easily doubled, but, from experience, there would be an important increase in accuracy and True Positive Rate.*

Nonetheless, the model achieved State-Of-The-Art results with a 0.9 accuracy, better than most models available. In the notebook BreastCancer.ipynb I further attempt to interpret the model by calculating a confusion matrix, plotting the specimens which caused the highest loss(errors) and most importantly plottig the activation heatmap which shows where the model focused on to find the tumor cells.


sources:

* https://www.kaggle.com/paultimothymooney/breast-histopathology-images
* https://www.pyimagesearch.com/2019/02/18/breast-cancer-classification-with-keras-and-deep-learning/
* https://docs.fast.ai/
