# Bottleneck Transformers for Visual Recognition

## Experiments

| Model | Params (M) | Acc (%) |
|:-:|:-:|:-:|
| ResNet50 baseline ([ref](https://github.com/kuangliu/pytorch-cifar)) | 23.5M | 93.62 |
| BoTNet-50 | 18.8M | 95.11% |
| BoTNet-S1-50 | | |

## Summary
<img width="516" alt="스크린샷 2021-01-28 오후 4 50 19" src="https://user-images.githubusercontent.com/22078438/106106482-f04da900-6188-11eb-8f15-820811c2f908.png">

## Usage (example)
```python
from model import MHSA

mhsa = MHSA(planes, width=14, height=14)
```


## Reference
 - [Paper link](https://arxiv.org/abs/2101.11605)
 - Author: Aravind Srinivas, Tsung-Yi Lin, Niki Parmar, Jonathon Shlens, Pieter Abbeel, Ashish Vaswani
 - Organization: UC Berkeley, Google Research
