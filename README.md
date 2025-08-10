
##  CIFAR-10 Image Classification with CNN

This project implements a **Convolutional Neural Network**  in **TensorFlow** to classify images from the **CIFAR-10 dataset** into 10 object categories.  
It includes **data preprocessing, model training, evaluation, and visualization** of results.

---

##  Project Overview

The CIFAR-10 dataset is a widely-used benchmark dataset in computer vision.  
It contains **60,000 color images (32x32 pixels)** across **10 classes**, each with **6,000 images**.

In this project:
- Train a **deep CNN** to classify images.
- Achieve ~**78% training accuracy** and ~**69% test accuracy**.
- Visualize **training curves** and **model predictions**.
- Demonstrate **end-to-end workflow**: dataset loading → model design → training → evaluation → prediction.

---

##  Dataset

**CIFAR-10 Classes**:
```

['airplane', 'automobile', 'bird', 'cat', 'deer',
'dog', 'frog', 'horse', 'ship', 'truck']

````

- **Training set**: 50,000 images  
- **Test set**: 10,000 images  
- Image size: **32×32×3** (RGB)  

---

##  Model Architecture

```python
Sequential(
    Conv2D(32, (3,3), activation='relu', input_shape=(32,32,3)),
    MaxPooling2D((2,2)),
    Conv2D(64, (3,3), activation='relu'),
    MaxPooling2D((2,2)),
    Conv2D(64, (3,3), activation='relu'),
    Flatten(),
    Dense(64, activation='relu'),
    Dense(10, activation='softmax')
)
````

* **Optimizer**: Adam
* **Loss function**: Sparse Categorical Crossentropy
* **Metrics**: Accuracy
* **Epochs**: 10

---


##  Installation & Usage

#### 1. Clone Repository

```bash
git clone https://github.com/Zeyad-Baloch/cifar-10-classification.git
cd cifar-10-classification
```

#### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

**`requirements.txt`**:

```
numpy
pandas
matplotlib
seaborn
tensorflow
```

#### 3. Run the Script

```bash
python cifar10_classification.py
```



##  Contributing

Pull requests are welcome!
For major changes, please open an issue to discuss your ideas.

---
