# Bottleneck Transformers for Visual Recognition

## Update 2021/03/14
 - support Multi-head Attention

## Experiments

| Model | heads | Params (M) | Acc (%) |
|:-:|:-:|:-:|:-:|
| ResNet50 baseline ([ref](https://github.com/kuangliu/pytorch-cifar)) | 23.5M | 93.62 |
| BoTNet-50 | 1 | 18.8M | 95.11% |
| BoTNet-S1-50 | 1 | 18.8M | 95.67% |
| BoTNet-S1-59 | 1 | 27.5M | 95.98% |
| BoTNet-S1-77 | 1 | 44.9M | wip |

## Summary
<img width="516" alt="스크린샷 2021-01-28 오후 4 50 19" src="https://user-images.githubusercontent.com/22078438/106106482-f04da900-6188-11eb-8f15-820811c2f908.png">

## Usage (example)
 - Model
 ```python
 from model import Model

 model = ResNet50(num_classes=1000, resolution=(224, 224))
 x = torch.randn([2, 3, 224, 224])
 print(model(x).size())
 ```
 - Module
 ```python
 from model import MHSA

 resolution = 14
 mhsa = MHSA(planes, width=resolution, height=resolution)
 ```


## Reference
 - [Paper link](https://arxiv.org/abs/2101.11605)
 - Author: Aravind Srinivas, Tsung-Yi Lin, Niki Parmar, Jonathon Shlens, Pieter Abbeel, Ashish Vaswani
 - Organization: UC Berkeley, Google Research
