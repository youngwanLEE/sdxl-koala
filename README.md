<!-- # KOALA: Self-Attention Matters in Knowledge Distillation of Latent Diffusion Models for Memory-Efficient and Fast Image Synthesis -->

<p align="left">
  <img src="asset/github_logo.svg"  alt="logo" style="width: 100%; max-width: none;">
</p>


## Abstract
### TL;DR
> We propose an fast text-to-image model, called KOALA, by compressing SDXL's U-Net and distilling knowledge from SDXL into our model. KOALA-700M can generate a 1024x1024 image in less than 1.5 seconds on an NVIDIA 4090 GPU, which is more than 2x faster than SDXL.

<details><summary>FULL abstract</summary>
Stable diffusion is the mainstay of the text-to-image (T2I) synthesis in the community due to its generation performance and open-source nature. 
Recently, Stable Diffusion XL (SDXL), the successor of stable diffusion, has received a lot of attention due to its significant performance improvements with a higher resolution of 1024x1024 and a larger model. 
However, its increased computation cost and model size require higher-end hardware (e.g., bigger VRAM GPU) for end-users, incurring higher costs of operation. 
To address this problem, in this work, we propose an efficient latent diffusion model for text-to-image synthesis obtained by distilling the knowledge of SDXL. 
To this end, we first perform an in-depth analysis of the denoising U-Net in SDXL, which is the main bottleneck of the model, and then design a more efficient U-Net based on the analysis. 
Secondly, we explore how to effectively distill the generation capability of SDXL into an efficient U-Net and eventually identify four essential factors, the core of which is that self-attention is the most important part. 
With our efficient U-Net and self-attention-based knowledge distillation strategy, we build our efficient T2I models, called KOALA-1B &-700M, while reducing the model size up to 54% and 69% of the original SDXL model. 
In particular, the KOALA-700M is more than twice as fast as SDXL while still retaining a decent generation quality. 
We hope that due to its balanced speed-performance tradeoff, our KOALA models can serve as a cost-effective alternative to SDXL in resource-constrained environments.


![teaser](asset/teaser.svg)

### Latency and memory usage comparison on different GPUs
![latency](asset/latency_gpu.svg)


### Code comming soon


## Acknowledgement
This work was supported by Institute of Information \& communications Technology Planning \& Evaluation (IITP) grant funded by the Korea government (MSIT) (No. RS-2022-00187238, Development of Large Korean Language Model Technology for Efficient Pre-training).



# 📖BibTeX
```bibtex
  @article{Lee2023koala,
          title={KOALA: Self-Attention Matters in Knowledge Distillation of Latent Diffusion Models for Memory-Efficient and Fast Image Synthesis}, 
          author={Lee, Youngwan and Park, Kwanyong and Cho, Yoohrim and Lee, Yong Ju and Hwang, Sung Ju},
          journal={arXiv preprint arXiv:2305.03726},
          year={2023}
  }
```