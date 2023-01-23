# Breast-Cancer-Classification


Breast cancer is one of the most common cancer and is causing a huge number of deaths in women. The high incidence and mortality of breast cancer is due to its considerably low accuracy of diagnosis. In this paper, we explore machine learning models that can be applied to help increasing the accuracy of the diagnosis of breast cancer. The main problem of the project is to detect breast cancer based on a set of features calculated from a digitized image of the Fine Needle Aspiration (FNA) of a breast mass from a patient.
Breast cancer is one of the most common cancer in women
and the second leading cause of women’s cancer death[1].
Despite the lack of effective treatment, the low accuracy of
diagnosis is also a major cause of the high incidence and mortality of breast cancer. Mammography is a traditional method
used for diagnosing breast cancer. According to UCHealth’s
report, only 78% of breast cancer can be accurately diagnosed
by mammography [2]. Many cases such as doctors’ negligence or incompetence in addition to a mammography error
may also result in a late diagnosis or misdiagnosis, which
can be considered a cause of breast cancer death [3]. In the
long term, early-stage diagnosis could significantly increase
the survival rate of breast cancer [4], therefore, it is important
to improve the accuracy of breast cancer diagnosis.
Machine learning has been applied in medical diagnosis
in a large number of papers [5]. In order to increase the accuracy of breast cancer diagnosis, we aim to use machine learning models and choose the model with higher performance.
We first cleaned the dataset by removing samples with empty
values. There are 683 samples after removing invalid samples. We then realized that the dataset with 683 samples is
rather small. To enhance the dataset, we generated a new
dataset by copying original dataset and add Gaussian noise to
it. Afterward, we appended the generated dataset to the original dataset. This process doubles the dataset to 1398 samples.
Then we rescaled data to [0,1] using MinMaxScaler.
By plotting scatter matrix of the features, we realized the
data is significantly right skewed, which may make the model
biased towards the majority of the features.Thus, we took the
square root of the feature data to mitigate the data skew problem.
We used 7 traditional models for the classification of breast
cancer cases. Feature selection is applied to increase the rate
of accurate prediction. Additionally, deep learning model is
also built for the diagnosis system. Finally, we compare the
performance of all the models applied and choose the one
with the highest performance.
(1) Logistic Regression (LR): Logistic regression predicts the
probability of the default class (e.g. Class 2 in this case) and
transforms the probability into a binary value (0 or 1) for classification using ”sigmoid” function as shown in Equation 1.
f(x) = 1/(1 + e−x)
In many machine learning algorithms, there is a decrease of
accuracy when the number of features is redundant [16].In
order to improve the accuracy of the models and avoid overfitting, we performed feature selection on the data. For the
traditional models, we used two techniques to select features
from the dataset. For the Decision Tree and Random Forest
model, we generate the feature importance of the last training
result and choose features accordingly. 
