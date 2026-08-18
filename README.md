# Waste Image Classification using EfficientNet-B1 & Pytorch
End-to-end computer vision project for household waste image classification using EfficientNet-B1 with PyTorch.

This project presents a complete computer vision pipeline for classifying household waste images into 15 categories using an EfficientNet-B1 model built with PyTorch.
The project covers dataset preparation, transfer learning, model training, evaluation, local deployment, and performance analysis.

---
## Project Highlights
- End-to-end ML pipeline (data → training → evaluation → deployment)
- Transfer Learning using EfficientNet-B1
- Custom evaluation script (PyTorch-based)
- Local offline inference
- Real-world waste sorting simulation

---
## Key Features
- Multi-class image classification (15 categories)
- Local inference using PyTorch
- GUI-based image selection (Tkinter)
- Confidence score prediction
- Custom evaluation script
- Confusion Matrix
- Classification Report
- Macro & Weighted F1 Score

---
## Project Structure

---
## Instalation
Clone this repository:
git clone https://github.com/septiandwitomo39/waste-ImageClassification-EfficientNetB1.git

cd waste-ImageClassification-EfficientNetB1

install Dependencies :
pip install -r requirements.txt

---
## Usage
### a. Run Model Evaluation
Evaluate the trained model on the validation or test dataset.
```bash
python deployment/evaluate.py
```
```
This script provides:

- Validation / Test Accuracy
- Macro F1 Score
- Weighted F1 Score
- Classification Report
- Confusion Matrix Visualization
```

### b. Run Local Prediction
Predict a single image using the trained EfficientNet-B1 model.
```bash
python deployment/predict.py
```
```
Features:

- Image selection using Tkinter GUI
- Predicted class
- Confidence score
- Offline inference using PyTorch
```

### c. Model File
The trained model is stored in:

```text
model/best.pt
```
The prediction and evaluation scripts automatically load this model.

---
## Local Inference
This project performs inference entirely on the local machine using PyTorch.
No internet connection, cloud service, or external API is required.
The trained model (`best.pt`) is loaded directly from the local repository for both prediction and evaluation.

---
## Model Details
- Model Architecture : EfficientNet-B1
- Framework : PyTorch
- Transfer Learning : Yes
- Task : Multi-class Image Classification
- Number of Classes : 15
- Training Images : 323
- Validation Images : 93
- Test Images : 46
- Input Size : 224 × 224

---
## 📈 Training Performance

The training and validation curves show the model's learning progression across 50 training epochs.

![Training Performance](assets/training_summary.jpg)

---
## Performance Summary
The model was evaluated on both validation and test datasets to measure its ability to generalize to unseen data.

### a. Validation Performance
The model was evaluated on 93 validation images across 15 waste categories.
| Metric | Score |
|---|---:|
| Accuracy | **69.89%** |
| Macro F1 Score | **69.39%** |
| Weighted F1 Score | **69.71%** |
![Validation Classification Report](assets/Validation_Summary.JPG)
![Validation Classification Report](assets/Validation_Summary_Accuracy_and_F1.JPG)

### b. Test Performance
Accuracy : 58.70%
Macro F1 : 56.76%
Weighted F1 : 56.61%

---
## Key Insights
- EfficientNet-B1 performs reasonably well on a relatively small dataset.
- Strong performance on visually distinct waste categories.
- Most misclassifications occur between visually similar plastic and glass objects.
- Test performance indicates room for improvement through larger datasets and additional fine-tuning.

---
## Limitation
- Small dataset (~21 training images per class on average)

---
## Future Improvements
- Increase dataset size
- Improve class balance
- Compare with additional CNN architectures
- Build web application using Gradio
- Deploy to Hugging Face Spaces

---
## Skills Demonstrated
- Transfer Learning
- PyTorch Model Deployment 
