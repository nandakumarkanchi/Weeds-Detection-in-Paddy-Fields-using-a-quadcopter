# Weeds-Detection-in-Paddy-Fields-using-a-quadcopter


## 🔬 Research Context & Motivation

Weed infestation in paddy fields significantly reduces crop yield and farmer income, particularly in rice-dependent regions like India. Conventional approaches such as manual weeding and indiscriminate herbicide spraying are labor-intensive, environmentally harmful, and lack precision.

This project addresses these limitations by developing a **deep learning–based weed detection system integrated with a hexacopter UAV**, enabling accurate **real-time semantic segmentation of weeds** in paddy fields. The system combines aerial robotics and computer vision to support scalable and sustainable precision agriculture.

---

## 🧠 Core Contributions

* Designed a **VGG19-based encoder–decoder architecture** with skip connections for high-precision weed segmentation
* Integrated a **Pix2Pix (cGAN) output layer** to enhance spatial realism and boundary sharpness
* Achieved **~95% validation accuracy** using the Adam optimizer
* Demonstrated **robust generalization** across varying soil textures, lighting conditions, and weed densities

---

## 📂 Repository Structure

```
├── Model/
│   └── code snippets                # Deep learning model
│
│
├── figures/
│   ├── model_architecture.png  # Figure 4.2 – Deep learning architecture
│   ├── result_figure_5_1.png   # Figure 5.1 – Segmentation results
│   └── result_figure_5_2.png   # Figure 5.2 – Optimizer performance comparison
│
└── README.md
```

---

## 🏗️ System & Model Architecture

The proposed architecture follows a **U-Net–style encoder–decoder pipeline** with a **VGG19 backbone**, optimized for aerial agricultural imagery.

### 🔹 Architectural Highlights

* **Encoder:** Hierarchical feature extraction from 250×250 RGB drone images
* **Skip Connections:** Preserve fine-grained spatial information critical for pixel-level segmentation
* **Decoder:** Progressive upsampling for high-resolution output reconstruction
* **Pix2Pix Output Layer:** Improves segmentation realism under noisy field conditions

### 📐 Model Architecture Diagram

![Model Architecture](figures/model_architecture.png)

*Figure 4.2: Architecture of the proposed deep learning model combining VGG19, skip connections, and Pix2Pix-based output refinement.*

---

## 📊 Dataset & Preprocessing

* **Dataset Source:** Publicly available, pre-annotated paddy field weed dataset referenced in the project report fileciteturn0file0
* **Data Ownership:** The dataset was **not collected by the authors**; it is reused strictly for academic and research purposes
* **Classes:** Paddy crop, grass weeds, broad-leaved weeds, sedge weeds

### Preprocessing

* Image resizing and normalization
* Data augmentation to improve robustness
* Train–validation split for unbiased evaluation

Using a standardized external dataset enables fair benchmarking and reproducibility while focusing the research contribution on **model architecture and learning behavior** rather than data acquisition.

---

## 🧪 Experimental Results

### 🌱 Weed Segmentation Performance

![Result Figure 5.1](figures/result_figure_5_1.png)

*Figure 5.1: Visual comparison of input images, ground truth masks, and predicted segmentation outputs. The model accurately localizes weed clusters with minimal false positives.*

---

### ⚙️ Optimizer Comparison

![Result Figure 5.2](figures/result_figure_5_2.png)

*Figure 5.2: Training and validation accuracy comparison between RMSprop and Adam optimizers. Adam demonstrates faster convergence and superior stability, achieving ~95% validation accuracy.*

---

## 📈 Key Findings

* Adam optimizer outperforms RMSprop in both stability and accuracy
* Pix2Pix layer significantly improves boundary sharpness in dense vegetation
* Model remains robust under varying lighting and soil conditions
* Architecture is suitable for **real-time UAV deployment**

---

## 📜 Academic Reference

This repository is based on the project report:

> **“Weeds Detection System using a Hexacopter with Computer Vision Technology”**
> Department of Robotics and Automation, Symbiosis Institute of Technology, Pune (2024–25)

---

## 👨‍🔬 Author

**Nandakumar R**
B.Tech – Robotics & Automation
Research Interests: Aerial Robotics, Computer Vision, Deep Learning, Precision Agriculture

---

## 🤝 Collaboration

This repository is shared for **academic, research, and portfolio purposes**. Researchers and students interested in extending this work are welcome to connect or fork the project.
