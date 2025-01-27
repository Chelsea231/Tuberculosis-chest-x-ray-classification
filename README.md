# Tuberculosis-chest-x-ray-classification
Author
Chelsea Rodrigues - 23200333

Introduction
Tuberculosis is caused by a bacterium called Mycobacterium, which is contagious and spreads through the community.TB is one of the leading causes of death throughout the world. Every year, millions of people become ill with tuberculosis (TB). In 2018, approximately ten million people were infected with tuberculosis, and a million and a half people died as a result of the infection. The disease's impact varies greatly, from fewer than 5 to more than 500 new patients per 100 000 citizens each year, depending on the severity of the disease. The fundamental reason for this high death rate is a failure in tuberculosis detection: more than one-third of the approximately ten million tuberculosis incidents are not registered and detected. There were a slew of solutions developed.

Chest X-Ray is one of these procedures (CXR) Chest X-rays (CXRs) are the preferred method of TB diagnosis for most early cases, owing to the low radiation dose, low cost, wide availability distinguish it from other TB detection methods. Researchers have been working on developing a computer-aided detection (CAD) system to aid in the preliminary diagnosis of tuberculosis-related diseases using medical imaging for several decades. Convolutional neural networks (CNNs) have consistently outperformed other traditional recognition algorithms in terms of achieving superior performance for image-based classification and recognition problems, due to advancements in deep learning.

Project Overview
Tuberculosis (TB) is an infectious disease that primarily affects the lungs and is responsible for the deaths of millions of people worldwide each year. Early detection of TB is crucial in combating its spread and improving patient outcomes. As powerful models for extracting informative features from images, Convolutional Neural Networks (CNNs) have demonstrated advantages in medical image recognition applications as well as other fields.. It is critical in this modern age to use X-rays to detect and classify diseases affecting the chest because of the limited number of qualified radiologists available in this field. We will look at the classification of tuberculosis in chest x-ray images using DenseNet and Deep forest models.

Motivation
The limited availability of qualified radiologists poses a significant challenge in diagnosing chest-related diseases, including TB. Automating this process using deep learning and image processing techniques can alleviate the strain on healthcare systems and improve diagnostic accuracy.

Methodology
⦁ Datasets In this database, you will find X-ray images of the chest taken from Tuberculosis (TB) positive cases as well as normal images. At the time of this release, we have 700 TB images that are publicly accessible and 2800 TB images that can be downloaded from the NIAID TB portal after signing an agreement, in addition to 3500 standard images.
Data Preparation:
It is necessary to undertake pre-processing in order for machine learning to be performed in accordance with medical guidelines. This includes data cleaning and normalization as well as noisy data filtering and the handling of missing values. It is vital to note that data pre-processing has a significant impact on the performance of machine-learning algorithms, and if it is not done correctly, it might result in biased output.

⦁ Preprocessing: All CXR images have been enhanced using contrast limited adaptive histogram equalization (CLAHE) with a clip limit number equal to 1.25; in addition, all CXR images have been resized from their original sizes to 150 x 150 pixels in Deep Forest model and 300 x 300 pixels in DenseNet model in order to improve processing speed.

⦁ Data augmentation: In order to increase the number of images under the classes with fewer CXRs, techniques such as horizontal flipping, rotating, contrast adjustment, and position translation have been judiciously implemented, resulting in a more evenly distributed data set that eliminates interference.

Machine Learning Models:
To diagnose tuberculosis and localize it in CXR images, deep CNN models are being used in conjunction with unified approaches to improve the accuracy-stability of the disease detection process. These approaches include DenseNet and cascaded classifier-based Deep forest models, among others. Using a dataset that has been divided into testing groups, we examine the overall performance of the models under consideration.

1.Dense Net
DenseNet is a convolutional neural network in which each layer is connected to all other layers that are deeper in the network. This is done in order to ensure that the most amount of information can flow between the layers of the network. In order to maintain the feed-forward nature of the system, each layer obtains inputs from all of the previous layers and passes on its own feature maps to all of the layers that will come after it.

Dense Net is better then others because in other models each layer passes information only to next layer which might lead to information loss but in dense every layer gets information from all previous layers so it has full picture which leads to better understanding of complex things. Also Dense net focuses only on important features and ignores unnecessary things due to which less memory is used and is more efficient than other models. It better understand patterns that indicate presence of TB

Our investigation focuses on the binary classification of images in order to distinguish between TB abnormalities, while also performing a further diagnosis and localization of specific TB-related manifestations on the data set under consideration.

2. Deep Forest
Deep forest is a ensemble learning ,method which means it is an machine learning approach where multiple models are combined to make predictions which improves overall accuracy and robustness of prediction compared to single model. It predicts bounding boxes around areas of interest in chest xray to identify where TB can be. It utilizes Cascaded structure that is each stage refines prediction made by previous stage and performs well in classifying CXR images without segmentation. An ensemble of learners has long been recognised as having great generalization performance as compared to solo learners.

Prerequisites
Python 3.x
TensorFlow
Scikit-learn
OpenCV
Numpy
Pandas
Matplotlib
deepforest

How to Run the Project
Clone the repository:
git clone <repository-url> cd <repository-folder>
Install the required packages:
pip install -r requirements.txt
Run the project script:
jupyter notebook
Open and run the notebooks in the Jupyter Notebook interface.
Execution Time
The entire project, including training and evaluation, is expected to run in approximately 20 minutes.

Results
In this two-class problem, all of the evaluated pre-trained models perform exceptionally well in distinguishing between TB and normal images. Deep Forest outperforms the other networks trained with X-ray images without segmentation when it comes to classifying the X-ray images, according to the results.


