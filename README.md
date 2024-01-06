# LLM-detect-AI-Generated_Text_Garvit-Gupta

The objective of this project is to discern AI-generated essays and determine which ones were composed by a sophisticated language model. The dataset comprises training prompts and essays, with labels indicating whether the text was generated by AI or written by a human. The methodology encompasses pre-processing, constructing, and training a BERT model using TensorFlow and TensorFlow Hub. The model's performance is assessed through the utilization of a confusion matrix.

Data Exploration
The project commences with the loading and exploration of the given datasets. Utilizing count plots for visualization yields insights into the distribution of AI-generated and human-written text across various categories. Notably, the train essays dataset exhibits an imbalance. To address this, an additional dataset, Daigt-V2-Train, is introduced. Through concatenation of both datasets, the imbalance is rectified, and the target variable ('generated') is scrutinized.


Data Preprocessing
Data is split into training and testing sets using the train_test_split function from scikit-learn. The necessary columns, including 'text' and 'generated,' are selected. Labels are assigned to training and testing sets for ease of model training.


Model Architecture:
The architecture of the model involves constructing a BERT model using TensorFlow and TensorFlow Hub. The model incorporates a preprocessor responsible for tokenization and encoding, followed by dense layers that include dropout for additional processing. The ultimate layer produces a binary classification result utilizing a sigmoid activation function.


Model Training:
For model training, the model is compiled using an Adam optimizer, binary cross entropy loss, and accuracy as the evaluation metric. The training process spans five epochs with a batch size of 8. To enhance performance and mitigate overfitting, a ModelCheckpoint and EarlyStopping callback are incorporated. These callbacks serve to save the best model based on validation accuracy and halt the training process if overfitting is detected.


Results and Evaluation
After training the model, it is evaluated on the testing set, and predictions are obtained. These predictions, along with true labels, are used to generate a confusion matrix. The confusion matrix is visualized using ConfusionMatrixDisplay from scikit-learn, including the F1 score in the title. The F1score provides a balance between precision and recall and is a suitable metric for imbalanced datasets.


Conclusion
The project demonstrates the process of building and training a BERT model for the detection of AI-generated text. It involves data exploration, preprocessing, model construction, and evaluation using a confusion matrix.



Garvit Gupta
21112046
Chemical Engineering, 3rd year











