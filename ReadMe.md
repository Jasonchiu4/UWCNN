# Underwater Scene Prior Inspired Deep Underwater Image and Video Enhancement
This repository is for Underwater Scene Prior Inspired Deep Underwater Image and Video Enhancement (UWCNN) introduced in the following paper

# Paper
[Chongyi Li](https://li-chongyi.github.io/),[Saeed Anwar](https://saeed-anwar.github.io/),  [Fatih Porikli](porikli.com), ["Underwater Scene Prior Inspired Deep Underwater Image and Video Enhancement"](https://www.sciencedirect.com/science/article/pii/S0031320319303401), Pattern Recognition, 2019. [[arxiv]](https://arxiv.org/pdf/1807.03528.pdf).

 ## Contents
1. [Introduction](#introduction)
2. [Network](#network)
2. [Train](#train)
3. [Test](#test)
4. [Datasets](#datasets)
5. [Results](#results)
6. [Citation](#citation)
7. [Acknowledgements](#acknowledgements)

## Introduction
In underwater scenes, wavelength-dependent light absorption and scattering degrade the visibility of images and videos. The degraded underwater images and videos affect the accuracy of pattern recognition, visual understanding, and key feature extraction in underwater scenes. In this paper, we propose an underwater image enhancement convolutional neural network (CNN) model based on underwater scene prior, called UWCNN. Instead of estimating the parameters of underwater imaging model, the proposed UWCNN model directly reconstructs the clear latent underwater image, which benefits from the underwater scene prior which can be used to synthesize underwater image training data. Besides, based on the light-weight network structure and effective training data, our UWCNN model can be easily extended to underwater videos for frame-by-frame enhancement. Specifically, combining an underwater imaging physical model with optical properties of underwater scenes, we first synthesize underwater image degradation datasets which cover a diverse set of water types and degradation levels. Then, a light-weight CNN model is designed for enhancing each underwater scene type, which is trained by the corresponding training data. At last, this UWCNN model is directly extended to underwater video enhancement. Experiments on real-world and synthetic underwater images and videos demonstrate that our method generalizes well to different underwater scenes.

## Network
<p align="center">
  <img width="600" src="https://github.com/saeed-anwar/UWCNN/blob/master/Figs/Net.png">
</p>



## Datasets
### Synthesized
To synthesize underwater image degradation datasets, we use the attenuation coefficients described in Table 1 for the different water types of oceanic and coastal classes (i.e., I, IA, IB, II, and III for open ocean waters, and 1, 3, 5, 7, and 9 for coastal waters). Type-I is the clearest and Type-III is the most turbid open ocean water. Similarly, for coastal waters, Type-1 is the clearest and Type-9 is the most turbid. We apply Eqs (1) and (2) (please check the paper) to build ten types of underwater image datasets by using the RGB-D NYU-v2 indoor dataset which consists of 1449 images. To improve the quality of datasets, we crop the original size (480*640) of NYU-v2 to 460*620. This dataset is for non-commercial use only.

Type-I:   [[Baidu]](https://pan.baidu.com/s/13k3qNGG93aFwdthjRtxi3Q)

Type-IA:  [[Baidu]](https://pan.baidu.com/s/13lRAbZYyYLyb-Z8qcpW-4Q)

Type-IB:  [[Baidu]](https://pan.baidu.com/s/12qXACo20C6ee9bViItZAFA)

Type-II:  [[Baidu]](https://pan.baidu.com/s/1iZM9md_mdeHXqw3XchvKHg)

Type-III: [[Baidu]](https://pan.baidu.com/s/1fIKVcvU6jg5Mi0Sw-k8VmA)

Type-1:   [[Baidu]](https://pan.baidu.com/s/1V10iXd9QnFbevm17Ua0jwQ)

Type-3:   [[Baidu]](https://pan.baidu.com/s/1DEI4T700jmU-cUYgAxRQAw)

Type-5:   [[Baidu]](https://pan.baidu.com/s/1jlPodNRPqySGnFxr7-qRRg)

Type-7:   [[Baidu]](https://pan.baidu.com/s/12l0gCsPYOtEx7hCvp9C-fw)

Type-9:   [[Baidu]](https://pan.baidu.com/s/1IPKimxXA1CsX3wjRE4VYNQ)

## Results
**All the results for RIDNET can be downloaded from GoogleDrive from [SSID](https://drive.google.com/open?id=15peD5EvQ5eQmd-YOtEZLd9_D4oQwWT9e), [RNI15](https://drive.google.com/open?id=1PqLHY6okpD8BRU5mig0wrg-Xhx3i-16C) and [DnD](https://noise.visinf.tu-darmstadt.de/submission-detail). The size of the results is 65MB** 

### Quantitative Results
<p align="center">
  <img width="500" src="https://github.com/saeed-anwar/RIDNet/blob/master/Figs/DnDTable.PNG">
</p>
The performance of state-of-the-art algorithms on widely used publicly available DnD dataset in terms of PSNR (in dB) and SSIM. The best results are highlighted in bold.

<p align="center">
  <img width="500" src="https://github.com/saeed-anwar/RIDNet/blob/master/Figs/SSIDTable.PNG">
</p>
The quantitative results (in PSNR (dB)) for the SSID and Nam datasets.. The best results are presented in bold.

For more information, please refer to our [papar](https://arxiv.org/abs/1904.07396)

### Synthetic Visual  Results
![Visual_PSNR_Synthetic1](/Figs/Synth1.PNG)
![Visual_PSNR_Synthetic2](/Figs/Synth2.PNG)
![Visual_PSNR_Synthetic3](/Figs/Synth3.PNG)
Comparison on more samples from DnD. The sharpness of the edges on the objects and textures restored by our method is the best.

### Real Visual  Results
![Visual_PSNR_Real1](/Figs/Real1.PNG)
![Visual_PSNR_Real2](/Figs/Real2.PNG)
Comparison on more samples from DnD. The sharpness of the edges on the objects and textures restored by our method is the best.

### Videi Visual  Results
![Visual_PSNR_VideoFrames](/Figs/Videoframes.PNG)
Comparison on more samples from DnD. The sharpness of the edges on the objects and textures restored by our method is the best.

## Citation
If you find the code helpful in your resarch or work, please cite the following papers.
```
@article{Anwar2019UWCNN,
title = "Underwater scene prior inspired deep underwater image and video enhancement",
journal = "Pattern Recognition",
volume = "98",
pages = "107038",
year = "2020",
issn = "0031-3203",
doi = "https://doi.org/10.1016/j.patcog.2019.107038",
url = "http://www.sciencedirect.com/science/article/pii/S0031320319303401",
author = "Chongyi Li and Saeed Anwar and Fatih Porikli",
}

@article{anwar2019diving,
  title={Diving Deeper into Underwater Image Enhancement: A Survey},
  author={Anwar, Saeed and Li, Chongyi},
  journal={arXiv preprint arXiv:1907.07863},
  year={2019}
}
```
