# Diabetic Retinopathy Detection using Hybrid EfficientNet + ViT

## Project Overview
This project aims to detect diabetic retinopathy (DR) stages from retinal fundus images using a hybrid deep learning model that combines EfficientNet and Vision Transformer (ViT). The model classifies images into five stages of DR severity:

1. **No DR (0)** - No signs of diabetic retinopathy.
2. **Mild (1)** - Early signs of DR.
3. **Moderate (2)** - More severe symptoms affecting vision.
4. **Severe (3)** - High risk of vision loss.
5. **Proliferative DR (4)** - Advanced stage with significant vision impairment.

## Dataset
The dataset consists of labeled retinal fundus images, categorized into five classes representing different DR stages. The dataset is structured into training, validation, and testing sets.

## Model Architecture
The model integrates:
- **EfficientNet-B0** for feature extraction from images.
- **Vision Transformer (ViT)** for capturing long-range dependencies.
- A fully connected layer that combines extracted features for classification.

## Training Pipeline
1. **Data Preprocessing:**
   - Images are resized to 224x224 pixels.
   - Normalization and data augmentation are applied.
2. **Model Training:**
   - Uses AdamW optimizer with learning rate scheduling.
   - Implements early stopping to prevent overfitting.
   - Utilizes mixed-precision training for efficiency.
3. **Evaluation Metrics:**
   - Accuracy, F1-score, Precision, and Recall.

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/diabetic-retinopathy-detection.git
   cd diabetic-retinopathy-detection
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download and prepare the dataset.

## Running the Model
### Training
Run the training script:
```bash
python train.py
```

### Inference (Single Image Prediction)
Use the following command to classify an image:
```python
from model import predict_image

image_path = "path/to/image.jpg"
result = predict_image(image_path, model_path="hybrid_model.pth")
print(f"Predicted DR stage: {result}")
```

## Results
The model achieves high accuracy in classifying diabetic retinopathy stages, making it a reliable tool for early detection and diagnosis.

## Contributors
- **Your Name**
- **Other Team Members**

## License
This project is licensed under the MIT License.

