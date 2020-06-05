# KBO_Classifier
###  Companion code and data for Smullen &amp; Volk (2020)

This repository contains data and code to train and run the Kuiper Belt object (KBO) classification algorithm presented in Smullen & Volk (2020).  If you use any data, code, or products from this repository, please cite our paper.  Any mistakes in this repository are unintentional.

**KBO Classifcation.ipynb** contains the trained classifier.  We also created three interfaces so users can apply our classifier to their own KBOs: 
- `compute_from_file()` computes features from a pre-existing file,
- `compute_from_aei()` creates features from simulations in which the user specifies the orbital elements of the KBO, and 
- `compute_from_jpl()` creates features from a simulation in which the user provides a JPL Horizons identifier.

**KBO Plotting.ipynb** shows a plotting function for visual inspection of KBO orbital evolution

**KBO_features.csv** contains the basic classifications and features for the 2305 observed KBOs used to train and test our algorithm.

`simulate_and_parse_backend.ipynb` and `plot_backend.ipynb` contain the code for running simulations, creating object features, and plotting.

`K04VD0X.follow`, `K04VD0X_bf.follow`, and `K13EF4J.follow` are simulation outputs we provide as example inputs to our functions. 

These notebooks were written in Python 3.6.  To run the machine learning algorithm, the code requires NumPy, pandas, and scikit-learn.  To plot, the code requires Matplotlib. To use the simulation interfaces, the code additionally requires the N-body package [Rebound](https://github.com/hannorein/rebound).
