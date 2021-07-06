
# The Sims4Action Dataset

Welcome to official homepage of the Sims4Action dataset [1]. Sims4Action dataset is built  with  the  popular  commercial  game THE SIMS 4 by specifically executing actions-of-interest in a top-down manner.


# Video providing the dataset overview

[![IMAGE ALT TEXT](https://img.youtube.com/vi/iSJ0fxXiS6s/0.jpg)](https://youtu.be/iSJ0fxXiS6s "Sims4Action dataset overview.")


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

[1] Let's Play for Action: Recognizing Activities of Daily Living by Learning from Life Simulation Video Games,\
Alina Roitberg*, David Schneider*, Aulia Djamal, Constantin Seibold, Simon Reiß, Rainer Stiefelhagen,\
In *International Conference on Intelligent Robots and Systems (IROS)*, 2021
(* denotes equal contribution.)

[2] [Toyota smarthome: Real-world activities of daily living.](https://arxiv.org/pdf/2010.14982.pdf)\
Srijan Das, Rui Dai, Michal Koperski, Luca Minciullo, Lorenzo Garattoni, Francois Bremond, Gianpiero Francesca,\
In *International Conference on Computer Vision (ICCV)*, 2019.



