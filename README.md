# Adaptive Synthetic Sampling Approach for Imbalanced Learning 

ADASYN is a python module that implements an adaptive oversampling technique for skewed datasets.

### Dependencies
* pip (needed for install)
* scipy
* scikit-learn
* numpy

### Installation

To use ADASYN you will need to clone this repository and install it running the following :

    git clone https://github.com/stavskal/ADASYN.git
    cd ADASYN
    pip install -r requirements.txt
    
    
After you have installed the packages you can proceed with using:
    ```python    
    from adasyn import ADASYN
    adsn = ADASYN(k=7,imb_threshold=0.6, ratio=0.75)
    #your imbalanced dataset is in X,y
    new_X, new_y = adsn.fit_transform(X,y)
    ```
    
    
Original paper can be found [here](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=4633969&url=http://ieeexplore.ieee.org/xpls/abs_all.jsp%3Farnumber%3D4633969) 

This module extends the idea presented in the paper by Haibo He et al. to include oversampling for **multiclass** classification problems. It is designed to be compatible with [scikit-learn] (https://github.com/scikit-learn/scikit-learn). It focuses on oversampling the examples that are harder to classify and has shown results which sometimes outperform SMOTE or SMOTEboost.

Props to [fmfn](https://github.com/fmfn) who implemented different oversampling techniques for his good code structure and documentation


An example can be seen below:

![alt tag](https://github.com/stavskal/ADASYN/blob/master/sample.jpg)
