
**Replicate Package** -  [https://drive.google.com/drive/folders/1AUKoHZ2sPWzTogNX4YV9D9hJPymHWIQV?usp=sharing](https://drive.google.com/drive/folders/19Xs1k_Dbrtrb8TOGLUnt6w0_aBSCEH1D)
**Original Files** - [https://drive.google.com/drive/folders/1KQyf4UPRHOVlglXYjIDFJ-JdyTmaMoqV ](https://drive.google.com/drive/folders/1KQyf4UPRHOVlglXYjIDFJ-JdyTmaMoqV)

We implemented FairGenerate and all baselines using Python 3.10.11.

In this study, we utilized publicly available datasets. All datasets are available in the **Dataset** folder, except below, which were excluded due to size limitations.

They can be obtained from the below URLs.

Home Credit - https://www.kaggle.com/c/home-credit-default-risk <br />
MEPS15 - https://gitlab.liris.cnrs.fr/otouat/MEPS-HC/-/blob/main/h181.csv <br />
MEPS16 - https://gitlab.liris.cnrs.fr/otouat/MEPS-HC/-/blob/main/h192.csv

********************************************************************************************************

1. Adult Income dataset - http://archive.ics.uci.edu/ml/datasets/Adult
2. COMPAS - https://github.com/propublica/compas-analysis
3. German Credit - https://archive.ics.uci.edu/ml/datasets/Statlog+%28German+Credit+Data%29
4. Bank Marketing - https://archive.ics.uci.edu/ml/datasets/bank+marketing
5. Default Credit - https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients
6. Heart - https://archive.ics.uci.edu/ml/datasets/Heart+Disease
7. MEPS - https://meps.ahrq.gov/mepsweb/
8. Student - https://archive.ics.uci.edu/ml/datasets/Student+Performance
9. Home Credit - https://www.kaggle.com/c/home-credit-default-risk

The replicate folder contains the codes to replicate our results. 
The codes in the folder are named for the applicable scenarios. The Adult and COMPAS data sets include two protected attributes, so we divide them into two scenarios: Adult_sex (COMPAS_sex) and Adult_race (COMPAS_race).

Baselines
-----------------------------------------------------
**Fair-Smote: Proposed in the paper: Bias in Machine Learning Software: Why? How? What to Do?**
Fair-Smote is a pre-processing method that uses the modified SMOTE method to make the distribution of sensitive features in the data set consistent, and then deletes biased data through situation testing.
We use the code they provided in the code repository: https://github.com/joymallyac/Fair-SMOTE

**FairMask: Proposed in the paper: FairMask: Better Fairness via Model-Based Rebalancing of Protected Attributes**
Fairway is a hybrid algorithm that combines pre-processing and post-processing methods. 
We use the code they provided in the code repository: https://github.com/anonymous12138/biasmitigation 

**LTDD: Linear Regression Based Training Data Debugging**
LTDD is preprocessing algorithm that finds and removes the biased portion present in the features of the training data.
We use the code they provided in the code repository: https://github.com/fairnesstest/LTDD
 
**Reweighing: Data preprocessing techniques for classification without discrimination**
Reweighing is a pre-processing method that calculates a weight value for each data point based on the expected probability and the observed probability, to help the unprivileged class have a greater chance of obtaining favorable prediction results. 
We use the following python's AIF360 module to achieve it:

<code>from aif360.algorithms.preprocessing import Reweighing</code>

-----------------------------------------------------

All codes are run on the Ubuntu Operating System. 
sensitive features in the data set consistent, and then deletes biased data through situation testing.

We use the code they provided in the code repository: https://github.com/joymallyac/Fair-SMOTE
