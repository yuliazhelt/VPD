# VPD Segmentation Project Overview

[WandB report with code execution](https://wandb.ai/yuliazhelt/thesis_vpd/reports/Application-of-Generative-Models-in-Discriminative-Tasks--Vmlldzo2ODQ4MTMz)

## Code structure:

```
VPD/
│
├── checkpoints/
│   ├── fpn_vpd_sd1-5_512x512_slim.ckpt (Pre-trained VPD for segmentation)
│   └── v1-5-pruned-emaonly.ckpt (StableDiffusion)
│
├── data/
│   └── ade/
│       └── ADEChallengeData2016/
│           ├── annotations/
│           │   ├── training/
│           │   └── validation/
│           └── images/
│               ├── training/
│               └── validation/
│
├── depth/
│
├── refer/

Repository needed for segmentation task:

├── segmentation/ 
│   ├── configs/
│   │   ├── _base_/
│   │   │
│   │   └── fpn_vpd_sd1-5_512x512_gpu8x2.py (Config for pre-trained VPD for segmentation)
│   │
│   ├── models/
│   │   └── vpd_seg.py (Main model VPD for segmentation)
│   │
│   ├── class_embeddings.pth (Class representations that have been pre-encoded with TextEncoder)
│   ├── dist_test.sh (Bash script for running test.py)
│   ├── dist_train.sh (Bash script for running train.py)
│   ├── README.md 
│   ├── test.py
│   └── train.py
│
├── stable-diffusion/ (git submodule)
│
└── vpd/ 
    └── models.py (Main architecture blocks: UNetWrapper, TextAdapter and so on)
```

## Links to download data and checkpoints:

- [fpn_vpd_sd1-5_512x512_slim.ckpt](https://cloud.tsinghua.edu.cn/f/78ca31e53c5549779abd/?dl=1)
- [v1-5-pruned-emaonly.ckpt](https://huggingface.co/runwayml/stable-diffusion-v1-5/resolve/main/v1-5-pruned-emaonly.ckpt)
- [ADEChallengeData2016](http://data.csail.mit.edu/places/ADEchallenge/ADEChallengeData2016.zip)

