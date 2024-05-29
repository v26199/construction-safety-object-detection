# Construction Safety Object Detection using YOLOv5

## Overview

Welcome to the Construction Safety Object Detection project repository! This project aims to enhance safety measures on construction sites through the use of advanced object detection techniques. Leveraging the YOLOv5 model architecture, we have developed a robust system capable of accurately detecting various safety hazards and objects commonly found in construction environments.

## Dataset Preparation

The dataset used in this project has been meticulously curated and preprocessed to ensure optimal model performance. Here's an overview of the dataset preparation steps:

- Data Cleaning: Removal of irrelevant or low-quality images such as blurry or unusable samples to enhance dataset quality.
- Dataset Splitting: Stratified splitting into training, validation, and test sets with appropriate proportions to facilitate robust model evaluation.
- Data Preprocessing: Standardization of image sizes (640x640) and auto-orientation to streamline training and inference processes.
- Data Augmentation: Incorporation of augmentation techniques including rotation (-15° to +15°) and brightness adjustments (-15% to +15%) to augment dataset diversity and improve model generalization.

## Model Training

The YOLOv5 model architecture was chosen as the foundation for this project due to its efficiency and accuracy in real-time object detection tasks. Here's an overview of the model training process:

- Pretrained Model Initialization: Initialization with pre-trained weights to leverage transfer learning and expedite convergence.
- Fine-Tuning: Customization of model hyperparameters and training configuration to adapt to the specifics of the construction safety dataset.
- Early Stopping Mechanism: Implementation of an early stopping mechanism to prevent overfitting and ensure optimal model generalization.

## Model Evaluation and Testing

After training the model, it was rigorously evaluated on the test dataset to assess its performance metrics, including precision, recall, and F1-score. The evaluation process involved:

- Evaluation Script: Utilization of a dedicated script to evaluate the trained model on the test dataset.
- Performance Metrics: Calculation of precision, recall, and F1-score to gauge the model's accuracy and robustness.
- Model Visualization: Visualization of detection results to gain insights into the model's performance and identify any areas for improvement.

## Usage

1. Clone the repository:

```bash
git clone https://github.com/v26199/construction-safety-object-detection.git
cd construction-safety-object-detection
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```
3. Train the model:

```bash
python src/train.py --data data/train.yaml --weights yolov5s.pt --epochs 50
```

4. Evaluate the model:

```bash
python src/evaluate.py --data data/test.yaml --weights models/yolov5_best.pt
```

## Conclusion

This project represents a significant step forward in construction site safety management by leveraging cutting-edge object detection techniques. The rigorous evaluation and testing processes ensure that the developed model is capable of accurately identifying safety hazards and objects, thereby mitigating risks and enhancing safety for construction personnel.


