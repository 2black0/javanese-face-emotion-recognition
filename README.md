# 😐😄😡 Javanese Facial Expression Dataset for Emotion Recognition

This repository contains a structured dataset of facial expression images labeled in **Javanese emotion categories**. It is intended for **training and testing emotion recognition models** using computer vision or deep learning approaches.

---

## 📁 Dataset Structure

The dataset is divided into two main folders:

```

.
├── dataset\_train/        # Training set (80% split recommended)
│   ├── gembira/
│   ├── marah/
│   ├── netral/
│   ├── sedih/
│   ├── takut/
│   └── terkejut/
├── dataset\_test/         # Testing set (20% split recommended)
│   ├── gembira/
│   ├── marah/
│   ├── netral/
│   ├── sedih/
│   ├── takut/
│   └── terkejut/

```

Each subfolder contains `.jpg` image files of individual faces showing the respective **facial expression**.

---

## 😄 Emotion Labels (in Bahasa Jawa)

| Label     | Translation (English) | Description                        |
|-----------|------------------------|------------------------------------|
| `gembira` | Happy                  | Smiling, joyful, or amused         |
| `marah`   | Angry                  | Frowning, intense facial tension   |
| `netral`  | Neutral                | No clear expression                |
| `sedih`   | Sad                    | Drooping face, frown, tears        |
| `takut`   | Fear                   | Wide eyes, tension, eyebrows up    |
| `terkejut`| Surprise               | Open mouth, raised eyebrows        |

---

## 🏷️ Image File Naming Convention

Each image filename follows this structured pattern:

```

XX-YY-ZZ\_WW NNN.jpg

```

Where:

| Segment   | Meaning                                | Example        |
|-----------|----------------------------------------|----------------|
| `XX`      | Actor/Actress ID (unique person)       | `01` → Person 1|
| `YY`      | Sentence/phrase spoken (ignored here)  | `01`           |
| `ZZ`      | Emotion ID                             | `03` → `gembira` |
| `WW`      | Looping / trial number                 | `01`           |
| `NNN`     | Image number / camera capture count    | `021`          |

📌 **Example**: `01-01-03_01 010.jpg`  
→ Person 1, Sentence 1, Emotion **gembira**, trial 1, frame 10.

---

## 🧪 Intended Use

This dataset is suitable for:

- Emotion classification using deep learning
- Transfer learning for expression recognition
- Cultural-specific emotion modeling (Javanese facial dataset)
- Research in computer vision and affective computing

---

## 🧠 Suggested Preprocessing Steps

1. **Face detection** (e.g. using MTCNN, HaarCascade, or Dlib)
2. **Image normalization** (resize, grayscale, histogram equalization)
3. **Label encoding** (map `gembira → 0`, etc.)
4. **Train-test split** (already structured)
5. **Augmentation** (rotation, flip, brightness variation)

---

## 🧑‍🔬 Baseline Model Ideas

You can use:

- CNN (Convolutional Neural Network)
- MobileNetV2 + fine-tuning
- ResNet18/34 pretrained models
- OpenCV-based classical features (e.g. LBP + SVM)

---

## 🔓 License

This dataset is released under the [MIT License](LICENSE).  
Use it for educational and research purposes. For commercial use, please contact the author.

---

## 🙋‍♂️ Credits

Created by **Ardy Seto Priambodo**  
📧 ardyseto@uny.ac.id

---

## ⭐ How to Cite

If you use this dataset for your research, please cite:

```

@misc{javanese\_emotion\_dataset,
author       = {Fatchul Arifin, Ardy Seto Priambodo, Aris Nasuha, Anggun Winursito, Teddy Surya Gunawan},
title        = {Development of Javanese Speech Emotion Database (Java-SED)},
year         = {2022},
howpublished = {\url{[https://github.com/2black0/Javanese-Face-Emotion-Recognition-Dataset}}](https://github.com/2black0/Javanese-Face-Emotion-Recognition-Dataset}}),
note         = {Accessed: YYYY-MM-DD}
}

```

---

## 📌 Notes

- Dataset is lightweight and suitable for embedded experiments (e.g., ESP32-CAM, Jetson Nano).
- Future versions may include `.csv` metadata, bounding box labels, or video sequences.
