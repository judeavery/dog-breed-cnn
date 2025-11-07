# Dog Breed Classification using Transfer Learning (MobileNetV2)

**Student:** Jude Avery • **NetID:** jsa210001  
**Course:** CS 4372
**Instructor:** Dr. A. Nagar  

---

###  Overview
This project applies **transfer learning** with **MobileNetV2** to classify dog breeds from the [Kaggle Dog Breed Identification dataset](https://www.kaggle.com/competitions/dog-breed-identification).  
Images are resized to 224×224, augmented, and used to fine-tune the final 20 layers of the pretrained model.

---

### Results
| Metric | Accuracy |
|:--------|:---------|
| **Top-1** | **76.9 %** |
| **Top-5** | **96.7 %** |

Plots for training/validation accuracy and loss are in `outputs/plots/`.  
25 example predictions are visualized directly in the notebook.

---

###  How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/cnn_dogbreed.git
   cd cnn_dogbreed
Install dependencies

bash
Copy code
pip install -r requirements.txt
Download the dataset from Kaggle
Kaggle Dog Breed Identification

Extract the files under:

bash
Copy code
data/train/
data/labels.csv
Run the notebook
Open cnn_dogbreed.ipynb in Jupyter or Google Colab and execute all cells in order.

Notes
Base model: MobileNetV2(weights="imagenet")

Train/validation split: 80 / 20 (stratified by breed)

Optimizer: Adam, LR = 1e-4

Loss: sparse_categorical_crossentropy

 References
TensorFlow / Keras documentation

Kaggle Dog Breed Identification dataset

yaml
