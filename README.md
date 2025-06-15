---
license: mit
task_categories:
- image-classification
language:
- en
tags:
- animals
- cat
- dog
- snake
- classifier
size_categories:
- 1K<n<10K
---

# 🐾 Animal Image Classification

The **Animal Image Classification** project aims to build a deep learning model to classify images of animals into three categories: **cats**, **dogs**, and **snakes**. This project uses a curated dataset of 3,000 images, equally distributed across the three classes.

---

## 📦 Dataset Summary

The Animal Image Classification Dataset is a comprehensive collection of images tailored for the development and evaluation of machine learning models in the field of computer vision. It contains **3,000 JPG images**, carefully segmented into three classes:

- `cats/`: 1,000 images of cats, with various breeds, environments, and postures.
- `dogs/`: 1,000 images of dogs, across multiple breeds and activities.
- `snakes/`: 1,000 images of snakes in both natural and artificial habitats.

**Image Details:**
- **Resolution:** 256x256 pixels  
- **Format:** JPG  
- **Color Space:** RGB

**🔗 Source:** [Kaggle Dataset by BorhaniTrash](https://www.kaggle.com/datasets/borhanitrash/animal-image-classification-dataset)

**🔐 License:** MIT — images permitted for academic and non-commercial use.

---

## 📁 Dataset Directory Structure

Animals/
├───cats/
├───dogs/
└───snakes/


Each folder represents a label and contains 1,000 corresponding images.

---

## 🏷️ Label File Format (`label.txt`)

Labels are automatically extracted from the folder names. The format is simple:

cats
dogs
snakes

This file is essential when using the TFLite model to associate prediction outputs with their class names.

---

## 🧪 Image Preprocessing

Each image is preprocessed with the following steps:
1. **Convert color**: BGR → RGB  
2. **Resize**: to 256x256 pixels  
3. **Contrast enhancement**: via CLAHE  
4. **Normalization**: scale pixel values to [0, 1]  
5. **Labeling**: based on folder name

---

## 🚀 Model Export

The trained model is saved in multiple formats for flexibility in deployment:

├───saved_model/
│ ├───saved_model.pb
│ └───variables/
├───tflite/
│ ├───model.tflite
│ └───label.txt
├───tfjs_model/
│ ├───group1-shard1of1.bin
│ └───model.json

- `saved_model/`: TensorFlow standard format  
- `tflite/`: For mobile/embedded devices  
- `tfjs_model/`: For web deployment with TensorFlow.js

---



