
# The Sims4Action Dataset: a videogame-based dataset for Synthetic→Real domain adaptation for human activity recognition

Welcome to official homepage of the Sims4Action dataset [1]. Sims4Action dataset is built  with  the  popular  commercial  game THE SIMS 4 by specifically executing actions-of-interest in a top-down manner.

This page is currently **under construction**. The dataset can already be downloaded [here](https://cvhci.iar.kit.edu/~aroitberg/datasets/sims4action/Sims4ActionVideos.zip), but detailed instructions and the evaluation scripts will follow.
If you have any questions, please do not hesitate to contact [Alina Roitberg](https://aroitberg.github.io/) or [David Schneider](https://simplexsigil.github.io) .

# Dowload the dataset

You can download the dataset [here](https://cvhci.iar.kit.edu/~aroitberg/datasets/sims4action/Sims4ActionVideos.zip).

# Video providing the *Sims4Action* dataset overview

[![IMAGE ALT TEXT](https://img.youtube.com/vi/iSJ0fxXiS6s/0.jpg)](https://youtu.be/iSJ0fxXiS6s "Sims4Action dataset overview.")


# Overview

* **Motivation**  
  Recognizing Activities of Daily Living (ADL) is a vital process for intelligent assistive robots, but collecting large annotated datasets requires time-consuming temporal labeling and raises privacy concerns, e.g., if the data is collected in a real household.
* **Goal**  
  Exploring the concept of constructing training examples for ADL recognition by playing life simulation video games.  
* **We introduce the ***Sims4Action*  dataset** created with the commercial game THE SIMS 4**  
  *Sims4Action* was built by specifically executing actions-of-interest in a "top-down" manner, while the gaming circumstances allowed us to freely switch between environments, camera angles and subject appearances. It features ten hours of video material of eight diverse characters in environments similar to the Toyota Smarthome household. Ten actions are performed which have a direct correspondence to actions described by Toyota Smarthome [2].
* **Two benchmarks**  
  We provide evaluation protocolls and baseline results for two challenges on the Sims4Action and Toyota Smarthome datasets [2]
  * *Gaming→Gaming* (training and evaluation on Sims4Action) 
  * *Gaming→Real* (training on Sims4Action, evaluation on Toyota Smarthome).
* **Main challenge: *Gaming→Real* domain adaptation**  
  While ADL recognition on gaming data is interesting from a theoretical perspective, the key challenge arises from transferring knowledge learned from simulated data to real-world applications. *Sims4Action* specifically provides a benchmark for this scenario since it describes a *Gaming→Real* challenge, which evaluates models on real videos derived from the existing Toyota Smarthome dataset [2]. 
* **Baselines**  
  We evaluate two modern Convolutional Neural Networks (CNNs) ([I3D](https://github.com/hassony2/kinetics_i3d_pytorch) and [S3D](https://github.com/kylemin/S3D)) for video-based activity recognition with and without real world pre-training on our proposed challenges.
* **Baseline Results**  
  Direct cross-domain recognition is a  hard task for modern data-driven algorithms and the performance has large room for improvement, demonstrating the sensitivity of modern ADL recognition models to domain shifts. Still, all models clearly outperform the random baseline, providing encouraging evidence, that a cheap, synthetic data collection from sources such as life simulation video games is a promising direction for training ADL models.

## Evaluation Protocol
**Cross-subject evaluation**  
Training subjects: `[1, 2, 3, 5, 6]`  
Validation subjects: `[7]`  
Test subjects: `[4,8]`  

## File Names
The individual file names are interpretable and consist of 
* A two letter action code (e.g. `Co` for cooking)
* Subject and room (e.g. `S7K1` for subject 1 and kitchen 1)
* A camera identifier, either for a fixed or for a moving camera (e.g. `fC8` or `m3`)

Valid file names would be `Co_S7K1_fC8` or `Co_S4K1_m3`, for example.

The following regular expression can be used to extract the listed information from the file name (without extension):  
```^([^_]*)_S(\d*)([^_]*\d*)_(fC\d*|m\d*)```

# Citation

If you use our dataset, please cite our soon-to-appear IROS paper:

```
@InProceedings{RoitbergSchneider2021Sims4ADL,
    author    = {Roitberg, Alina and Schneider, David and Djamal, Aulia and Seibold, Constantin and Reiß, Simon and Stiefelhagen, Rainer},
    title     = {Let's Play for Action: Recognizing Activities of Daily Living by Learning from Life Simulation Video Games},
    booktitle=  {2021 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
    year      = {2021},
    organization = {IEEE}
}
```

# External Code

For our experiments, we used these Pytorch implementations of the [I3D](https://github.com/hassony2/kinetics_i3d_pytorch) and [S3D](https://github.com/kylemin/S3D) models.

# External Dataset

The *Gaming→Real* benchmark comprises evaluation on the external real-life dataset Toyota Smarthome [2]. The authors of Toyota Smarthome are not in any form connected to this work. Different [licenses](https://project.inria.fr/toyotasmarthome/files/2020/12/License_v2.pdf) apply. To obtain the Toyota Smarthome benchmark for evaluation on the real data, please follow the instruction of the [official website](https://project.inria.fr/toyotasmarthome/) and cite the paper [2] accordingly if you use the dataset. 


# References 

[1] [Let's Play for Action: Recognizing Activities of Daily Living by Learning from Life Simulation Video Games.](http://arxiv.org/abs/2107.05617
)\
Alina Roitberg*, David Schneider*, Aulia Djamal, Constantin Seibold, Simon Reiß, Rainer Stiefelhagen,\
In *International Conference on Intelligent Robots and Systems (IROS)*, 2021
(* denotes equal contribution.)

[2] [Toyota smarthome: Real-world activities of daily living.](https://arxiv.org/pdf/2010.14982.pdf)\
Srijan Das, Rui Dai, Michal Koperski, Luca Minciullo, Lorenzo Garattoni, Francois Bremond, Gianpiero Francesca,\
In *International Conference on Computer Vision (ICCV)*, 2019.



