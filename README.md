# Multimodal Mood Detection in Dementia Patients

This project investigates the use of **2D and thermal images** to detect human emotions using **deep learning** models, specifically for applications in **dementia care**. It compares the performance of **ResNet-50** and **EfficientNet-B0** architectures on two datasets (KTFE and TUFT), utilizing late fusion to improve prediction accuracy.

---

## 🔍 Project Overview

Dementia patients often experience emotional outbursts due to Behavioral and Psychological Symptoms of Dementia (BPSD). Early detection of mood changes can help prevent these episodes and improve care. This project explores how multimodal image input (2D and thermal) can aid in detecting mood states such as **anger, fear, happiness, sadness, and surprise**.

---

## 📚 Datasets Used

### 🧠 KTFE Dataset
- 7 emotion classes: Anger, Disgust, Fear, Happy, Neutral, Sad, Surprise
- Modalities: RGB and Thermal
- Participants: East and Southeast Asian individuals

### 😴 TUFT Dataset
- 4 emotion classes: Neutral, Happy, Sleepy, Surprise
- Modalities: RGB and Thermal
- Participants: More diverse and exaggerated emotions

---

## 🧠 Models Trained

### 🏗️ Architectures:
- **ResNet-50**
- **EfficientNet-B0**

### 🧪 Training Types:
- Trained separately on 2D and thermal images
- Late Fusion of 2D + Thermal predictions

### 🎯 Saved Weights:
The following `.pth` files are included:

- `ktfe_RGB_efficientnet.pth`
- `ktfe_thermal_efficientnet.pth`
- `ktfe_RGB_resnet50.pth`
- `ktfe_thermal_resnet50.pth`
- `tuft_RGB_efficientnet.pth`
- `tuft_thermal_effcicientnet.pth`
- `tuft_RGB_resnet50.pth`
- `tuft_thermal_resnet50.pth`

---

## 🖥️ Installation & Setup

1. Clone the repo:

```bash
git clone https://github.com/your-username/Multimodal-Mood-Detection-Dementia.git
cd Multimodal-Mood-Detection-Dementia
```

2. Create a virtual environment (optional but recommended):

```bash
conda create -n mood_env python=3.10
conda activate mood_env
```

3. Install the requirements:

```bash
pip install -r requirements.txt
```

> If `requirements.txt` is not available, install key packages manually:
```bash
pip install torch torchvision matplotlib seaborn scikit-learn
```

4. (Optional) To run a model:

```bash
python main.py
```

---

## 📊 Results Summary

| Dataset | Model        | Best Recall        | Best Precision     | Best F1-score       |
|---------|--------------|--------------------|--------------------|---------------------|
| TUFT    | EfficientNet | Sleepy (1.00)       | Sleepy (1.00)       | Sleepy (1.00)        |
| TUFT    | ResNet-50    | Sleepy (0.95)       | Sleepy (1.00)       | Sleepy (0.95)        |
| KTFE    | EfficientNet | Happy (0.88)        | Disgust (0.95)      | Disgust (0.86)       |
| KTFE    | ResNet-50    | Happy (0.86)        | Anger (0.74)        | Happy (0.85)         |
| KTFE    | Late Fusion  | Disgust (0.79)      | Disgust (0.95)      | Disgust (0.86)       |

---

## 👨‍💻 Team Members

- **Ebba Norlin** 
- **Valento Bardhoshi** 
- **Somaiya Abdulrahman**
- **Sadeen Alkhalili**
- **Anas Mustafa Mohadin**


---

## 🤝 Acknowledgements

This work was done as part of the "Applied Artificial Intelligence" course at **Mälardalens University**, Sweden.

---

