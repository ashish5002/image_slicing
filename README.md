# 🧠 3D Medical Image Preprocessing Pipeline

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![SimpleITK](https://img.shields.io/badge/SimpleITK-2.2.1-blue)](https://simpleitk.readthedocs.io/)
[![Colab Compatible](https://img.shields.io/badge/Colab-Compatible-brightgreen)](https://colab.research.google.com/)


This project provides a clean, modular pipeline for **3D medical image preprocessing** using **SimpleITK** and **NumPy**, suitable for deep learning tasks like segmentation, classification, and anomaly detection.

---

## 🚀 Features

✅ NIfTI format support (`.nii` / `.nii.gz`)  
✅ Intensity windowing and normalization  
✅ Resampling to consistent voxel spacing  
✅ 2D center cropping or padding (for spatial uniformity)  
✅ Patch-based slicing in Z-direction  
✅ Slice visualization using `matplotlib`

---

## 🧩 Preprocessing Steps

1. **Read and resample** the 3D image to a spacing of `[1.5, 1.5, 1.0]`
2. **Clamp** intensities to Hounsfield window `[-200, 200]`
3. **Normalize** to `[0, 1]` scale
4. **Center crop or pad** each slice to `(256, 256)`
5. **Split** into overlapping 3D patches (depth=32, stride=16)
6. **Visualize** the central slice of the first patch

---

## 🔧 Installation

```bash
pip install numpy SimpleITK matplotlib
