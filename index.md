## Neural Video Coding using Multiscale Motion Compensation  and Spatiotemporal Context Model

<sup>1</sup> Haojie Liu, <sup>1</sup> Ming Lu, <sup>1</sup> Zhan Ma, <sup>2</sup> Fan Wang, <sup>2</sup> Zhihuang Xie, <sup>1</sup> Xun Cao and <sup>3</sup> Yao Wang

<sup>1</sup> Nanjing University, <sup>2</sup> OPPO.Inc, <sup>3</sup> New York City
## Introduction
  We propose an end-to-end deep neural video coding framework (NVC), which uses variational autoencoders (VAEs) with joint spatial and temporal prior aggregation (PA) to exploit the correlations in intra-frame pixels, inter-frame motions and inter-frame compensation residuals, respectively. Novel features of NVC include: 1) To estimate and compensate motion over a large range of magnitudes, we propose an unsupervised multiscale motion compensation network (MS-MCN) together with a pyramid decoder in the VAE for coding motion features that generates multiscale flow fields, 2) we design a novel adaptive spatiotemporal context model for efficient entropy coding for motion information, 3) we adopt nonlocal attention modules (NLAM) at the bottlenecks of the VAEs for implicit adaptive feature extraction and activation, leveraging its high transformation capacity and unequal weighting with joint global and local information, and 4) we introduce multi-module optimization and a multi-frame training strategy to minimize the temporal error propagation among P-frames. NVC is evaluated for the low-delay causal settings and compared with H.265/HEVC, H.264/AVC and the other learnt video compression methods following the common test conditions, demonstrating consistent gains across all popular test sequences for both PSNR and MS-SSIM distortion metrics.

### Architecture
Our NVC framework is designed for low-delay applications.As with all modern video encoders, the proposed NVC com-presses  the  first  frame  in  each  group  of  pictures  as  an  intra-frame using a VAE based compression engine (neuro-Intra). Itcodes remaining frames using motion compensated prediction. It  uses  the  VAE  compressor  (neuro-Motion)  to  generate  the  multiscale  motion  field  between  thecurrent frame and the reference frame. Then, MS-MCN takesmultiscale compressed flows, warps the multiscale features ofthe  reference  frame,  and  combines  these  warped  features  togenerate  the  predicted  frame.  The  prediction  residual  is  thencoded using another VAE-based compressor (neuro-Res).
![Image](https://github.com/NJUVISION/Neural-Video-Coding/blob/master/images/NVC.png)

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/NJUVISION/Neural-Video-Coding/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
