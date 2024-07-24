# ImageClassification
This repository is for the classification of Images with a confidence score
For this project, I've used a dataset from Kaggle "https://www.kaggle.com/datasets/utkarshsaxenadn/fruits-classification".
Ensure your UiPath studio and orchestrator are connected to the same folder via UiPath Assistant.
In this project, we are mainly using an AI center to train the ML models

**Project Setup and Data Preparation**

1. Enable AI Center: Ensure that AI Center is enabled in your UiPath Orchestrator.
2. Create a Project: Start a new project in the AI Center called "ImageClassification".
3. Upload Dataset:
Organize your dataset in the following structure:

DataSet
├── Training
│   └── Images
│       └── Apple
│           └── apple1.png
└── Evaluation
    └── Images
        └── Apple
            └── apple1.png
Upload this structured dataset to the Orchestrator.

**Model Training and Evaluation**

4. Create an ML Package:
  Navigate to "ML Packages".
  Select "Out of the box Packages".
  Choose "UiPath Image Analysis -> ImageClassification" for image classification tasks.
5. Create a Pipeline:
  Create pipelines for both the training and evaluation datasets.
  For training, select the "Trial run" option.
  For evaluation, select the "Evaluation run" option and choose a higher minor version from the dropdown.
6. Create ML Skill:
  After the model is trained and evaluated, create an ML Skill in the AI Center.
  
**Testing and Deployment**

7. Test the ML Model:
  Create a simple workflow in UiPath Studio to test the model.
  Install the ML Services package via "Manage Packages".
8. Use MLSkill Activity:
  Drag and drop the MLSkill activity into your workflow.
  Provide an input image to the ML model, which will return a confidence score for the classification.
