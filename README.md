# CSAN
CSAN: Cascaded Structural-Aware Network for Image-Text Matching
# Introduction
The framework of CSAN:


<img width="5918" height="2099" alt="fig2" src="https://github.com/user-attachments/assets/0a7fe1a4-4a4a-4375-8cec-b64cba2a1edc" />

# Requirements
Utilize pip install -r requirements.txt for the following dependencies.
- Python 3.7.11
- PyTorch 1.7.1
- NumPy 1.21.5
- Punkt Sentence Tokenizer:

```
import nltk
nltk.download()
> d punkt
```
# Download data and vocab
We follow SCAN to obtain image features and vocabularies, which can be downloaded by using:
```
https://www.kaggle.com/datasets/kuanghueilee/scan-features
```
```
data
├── coco
│   ├── precomp  # pre-computed BUTD region features for COCO, provided by SCAN
│   │      ├── train_ids.txt
│   │      ├── train_caps.txt
│   │      ├── ......
│   │
│   └── id_mapping.json  # mapping from coco-id to image's file name
│   
│
├── f30k
│   ├── precomp  # pre-computed BUTD region features for Flickr30K, provided by SCAN
│   │      ├── train_ids.txt
│   │      ├── train_caps.txt
│   │      ├── ......
│   │
│   └── id_mapping.json  # mapping from f30k index to image's file name
│   
│
└── vocab  # vocab files provided by SCAN (only used when the text backbone is BiGRU)
```
# Training
```
python train.py
```
# Evaluation
```
python evaluation.py
```




