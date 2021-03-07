# Membership Inference Attacks - Repository For New Trends In Data Analytics Winter's Term 2020/2021

## About the MIA

* Goal: Determine for a machine learning model M whether given data x with output y is part of the training data T of M
* Most difficult scenario: M is only available as a blackbox; ability to get output y of M for x
* Idea: Train an attack Model A on differences of M's output that might indicate whether x is in T or not. Underlying phenomenon: M's different output for data that is in the training set vs data that is not in the training set
  - This behavior gets worse the more overfitted M is
* Problem for the attacker: No knowledge about T and M
  - Train Shadow Models SM that should behave similarly to M on known training data
  - Classify out-of-the-sample and in-the-sample data with SM
  - Let A learn the differences in results for the two groups of data classified by SM
  - Now A is trained to **tell, if given data y is in T by taking M's response to y, which is x, as input**
  - A works with classification results and knows how to distinguish classification results between "true" and "false" regarding the question whether they had been in the training set of the classification model

## Problems so far

* Understand difference in one classification setup - what are "training accuracy" and "testing accuracy"?
* What is "cumulative fraction of classes" in the performance evaluation?

## Literature

Scientific:

* [shokri-2017_membership-inference-attacks-against-machine-learning-models](https://arxiv.org/abs/1610.05820)

Other:

* [Demystifying the Membership Inference Attack](https://medium.com/disaitek/demystifying-the-membership-inference-attack-e33e510a0c39)
* [Membership Inference Attacks on Neural Networks](https://gab41.lab41.org/membership-inference-attacks-on-neural-networks-c9dee3db67da)
