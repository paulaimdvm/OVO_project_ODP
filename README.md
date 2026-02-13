# OVO_project_ODP
# Unrolled Optimization with Deep Priors (ODP) – Image Restoration Project

This project explores the use of **Unrolled Optimization with Deep Priors (ODP)** for image restoration tasks, with a focus on **image denoising** and exploratory experiments on **RGB denoising and deblurring**.  
The goal is to better understand how unrolled optimization methods compare to classical approaches under realistic computational constraints.

The project is organized around two main experiments implemented as Jupyter notebooks.

---

## Project Overview

### Experiment 1 – Grayscale Image Denoising (Main Experiment)



**Objective:**  
The first experiment aims to faithfully reproduce the denoising setup presented in the paper *Unrolled Optimization with Deep Priors*, focusing on grayscale images.

- The ODP model is evaluated on **image denoising**
- Results are compared with **classical baseline methods**, such as:
  - Gaussian filtering
  - Forward–Backward splitting with TV regularization
- The implementation closely follows the paper’s methodology:
  - Same optimization structure
  - Similar network design and number of unrolled iterations
- The only major difference is the **dataset size**, which is reduced for computational reasons

**Dataset:**  
Images are taken from the **CBSD68 dataset**, converted to grayscale and split into training and test sets.

This experiment represents the **core and most rigorous part** of the project.

---

### Experiment 2 – Going Further: RGB Denoising and Deblurring



**Objective:**  
The second experiment explores extensions of ODP under **reduced computational settings**.

- RGB image denoising (3 channels)
- Preliminary tests on **image deblurring**, as discussed in the paper
- Parameters are intentionally reduced:
  - Fewer training epochs
  - Fewer unrolled iterations
  - Smaller models

This experiment is **not intended to provide state-of-the-art performance**, but rather:
- To test the flexibility of the ODP framework
- To validate that the method can be extended beyond grayscale denoising
- To observe qualitative behavior under low-computation constraints

---

## Folder Structure

- `data/train/` contains training images
- `data/test/` contains test images
- Images may have different spatial resolutions and are preprocessed inside the notebooks

---

## Key Characteristics of the Project

- Implemented in **PyTorch**
- Simple and readable code, written at a **student project level**
- Focus on:
  - Understanding unrolled optimization
  - Comparing learned priors with classical methods
  - Exploring computational trade-offs
- Emphasis on **clarity and experimental reasoning**, not raw performance

---

## References

[1] Mardani et al., *Unrolled Optimization with Deep Priors*,  
    arXiv:1705.08041  
    https://arxiv.org/abs/1705.08041

[2] D. Martin, C. Fowlkes, D. Tal, J. Malik,  
    *A Database of Human Segmented Natural Images and its Application to Evaluating Segmentation Algorithms*,  
    Proc. ICCV, 2001.  
    Dataset (CBSD68): https://github.com/clausmichele/CBSD68-dataset

