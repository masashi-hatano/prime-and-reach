# Prime and Reach: Synthesising Body Motion for Gaze-Primed Object Reach

<div align="center">

[![Paper](https://img.shields.io/badge/arXiv-2504.08654-red)](https://arxiv.org/abs/2512.XXXXX)
[![Project Page](https://img.shields.io/badge/Project-Page-blue)](https://masashi-hatano.github.io/prime-and-reach/)

</div>

**This is the official code releasse for "Prime and Reach: Synthesising Body Motion for Gaze-Primed Object Reach".**


The code will be available upon acceptance.


## Dataset Overview
We curate prime and reach sequences from 5 different datasets:
- **HD-EPIC**
- **MoGaze**
- **HOT3D**
- **ADT**
- **GIMO**

<img src="assets/dataset_samples.png" alt="Example Sequences"/>

The dataset provides motion and gaze data across these sources.

You can download the dataset [here](https://uob-my.sharepoint.com/:f:/g/personal/ve22636_bristol_ac_uk/IgCGqhTjsmu8T6V1LJS8ydcFAVubcEW-b4UCIP60kIokv-w?e=6flrzW).

The data is organized by source dataset. Each dataset folder contains subdirectories for `motions` and `gazes`.

```text
root/
├── HD-EPIC/
│   ├── motions/
│   ├── gazes/
│   └── target_information.json
├── MoGaze/
│   ├── motions/
│   ├── gazes/
│   └── target_information.json
├── HOT3D/
│   ├── motions/
│   ├── gazes/
│   └── target_information.json
├── ADT/
│   ├── motions/
│   ├── gazes/
│   └── target_information.json
└── GIMO/
    ├── motions/
    ├── gazes/
    └── target_information.json
````

The `motions` folder has 22 joint position data for each sequence in the data. It comprises of motion sequences as from  `0000000000.npy,0000000001.npy,...` where each `npy` file corresponds to an unique sequence. The motion data is shaped as `Nx22x3` where N is the length of the sequence.
Note that our motion is +y-up, i.e. y-axis is the gravity axis.

Similarly `gazes` folder has the gaze information for each of the sequences `0000000000.npy,0000000001.npy,...`. They are also saved as `npy` files with shapes `Nx3` where the 3 values `x,y,z` represent the 3D unit vector in the gaze direction originating from the head joint.

The `target_information.json` has information related to the goal location, text prompt, train/test subset and primed frame number for each sequence. Each key in the json corresponds to each unique sequence under which we provide all the information.


## Code/Model

Coming Soon



## ✍️ Citation

If you find our work useful in your research, please consider citing:

```bibtex
@article{hatano2025primeandreach,
  title={Prime and Reach: Synthesising Body Motion for Gaze-Primed Object Reach},
  author={Hatano, Masashi and Sinha, Saptarshi and Chalk, Jacob and Li, Wei-Hong and Saito, Hideo and Damen, Dima},
  journal={arXiv preprint arxiv:2512.XXXXX},
  year={2025},
}
```