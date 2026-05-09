# Latent-IRSDE
<p align="center">

  <h1 align="center">High-Resolution Aerial Image Restoration with Latent Diffusion Models</h1>


  <p align="center">
    <a href="https://github.com/hapless19" rel="external nofollow noopener" target="_blank"><strong>Yong Wang</strong></a>
    ·
    <a href="https://github.com/liw11111" rel="external nofollow noopener" target="_blank"><strong>Wei Li</strong></a>
    ·

  </p>
<p align="center">
    <a href="" rel="external nofollow noopener" target="_blank">2024 IEEE International Conference on Unmanned Systems (ICUS)</a>
  <p align="center">
    <img src="assets/1.jpeg" alt="Description of the image" width="600" height="600">
  <p align="center">
<p align="center" style="font-size: 18px; color: gray;">
    Fig. 1. Applications of tracking a fixed-wing UAV. (a) a UAV landing on a ship. (b) a UAV landing on airport. (c) a UAV pose estimation. (d) a UAV pose estimation.
</p>
<p align="center">
    <img src="assets/2.jpeg" alt="" width="600" height="600">
</p>
<p align="center" style="font-size: 18px; color: gray;">
    Fig. 2. Pipeline of the fixed-wing UAV tracking.
</p>

## **Abstract** 📝
This paper aims to improve the performance of diffusion models in high-resolution unmanned aerial vehicle (UAV) aerial image restoration tasks. We propose an efficient image restoration algorithm based on diffusion models, named Latent-IRSDE, which consists of two parts: pretrained encoder-decoder networks and diffusion-based image restoration networks. Diffusion-based image restoration networks have the remarkable ability to generate high-quality aerial images with low-quality visions. Pretrained encoder-decoder networks transform high-resolution aerial images into small latent images. We leverage the frozen internal representations of pretrained encoder-decoder networks to perform an efficient high-resolution aerial images restoration. We select some data from an open-source dataset to create our IR-UAV2UAV dataset for evaluating our method. The experiments show that our proposed method can restore high-resolution aerial images and achieve fastest inference time in quantitative comparisons of image deblurring and deraining tasks on IR-UAV2UAV dataset with images sized at 1920×1080 pixels.

---


---

## Table of Contents 📑
- [Introduction](#introduction)
- [Contributions](#contributions)
- [Experimental Results](#experimental-results)
- [Visualizations](#visualizations)
- [Reproduction](#reproduction)
- [Citation](#citation)

---

## **Introduction** 🌟

UAV aerial images often suffer from degradation such as motion blur and rain streaks in real scenarios.
Standard diffusion models deliver high-quality generation but are slow for high-resolution images.
Latent Diffusion Models (LDM) enable efficient high-resolution synthesis by working in a compressed latent space, which is suitable for aerial image restoration.

---

## **Contributions** ✨

Applies latent diffusion to high-resolution UAV image restoration for the first time.
Uses frozen pretrained autoencoders to boost efficiency without changing the diffusion structure.
Achieves state-of-the-art inference speed on deblurring and deraining tasks for 1080p aerial images.

---

## **Quick View** 📊
### Dataset Examples
#### The fixed-wing UAV.
<p align="center">
    <img src="assets/3.jpeg" alt="Dataset Overview" width="600" height="600">
</p>

#### Dataset Overview 
<p align="center">
    <img src="assets/4.jpeg" alt="" width="600" height="600">
</p>
<p align="center" style="font-size: 18px; color: gray;">
    The UAV is denoted in red rectangle box.(a) Tiny object. (b) Motion blur. (c) Out of focus. (d) 3D rotation.
</p>

#### Bounding Box 
<p align="center">
    <img src="assets/5.jpeg" alt="" width="600" height="600">
</p>
<p align="center" style="font-size: 18px; color: gray;">
    (a) Area distribution of the UAV bounding box. (b) Width distribution of the UAV bounding box. (c) Height distribution of the UAV bounding box.
</p>

#### Illustration of the training images
<p align="center">
  <img src="assets/6.jpeg" alt="" width="600" height="600">
</p>

## **Experimental Results**🖼️
### Success and precision of the hand-crafted feature-based methods
<p align="center">
    <img src="assets/7.jpeg" alt="" width="600" height="600">
</p>

### Success and precision of the deep learning-based methods
<p align="center">
    <img src="assets/8.jpeg" alt="" width="600" height="600">
</p>

### Qualitative results of four methods in three typical difficult challenges
<p align="center">
    <img src="assets/9.jpeg" alt="" width="600" height="600">
</p>
<p align="center" style="font-size: 18px; color: gray;">
    (a) low resolution. (b) motion blur and rotation. (c) scale variation.
</p>

---

## **Quick Start** 🚀

### Dataset
- **GFUAVT**: [Baidu Drive (mt2h)](https://pan.baidu.com/s/1w59YcuoDV_X7bq23Yo2Tew)  


### Dataset Structure
```

├── GFUAVT                      # GFUAVT dataset
│   ├── anno                    # Annotations (47)
│   │   ├── img001001.txt
│   │   └── ...
│   ├── frames                  #  Images
│   │   ├── img001001
│   │   │   ├── 00000041.jpg
│   │   └── ...

```

---

## **Citation** 📚

If you find **GFUAVT** helpful in your research, please consider citing:
```bibtex
@inproceedings{GFUAVT,
  title={Ground view fixed-wing UAV tracking dataset and experimental evaluation},
  author={Yong Wanga, Wei Lia, Xiangyu Zhua, Lu Dingb},
  booktitle={Unmanned Systems},
  year={2026}
}
```

---
