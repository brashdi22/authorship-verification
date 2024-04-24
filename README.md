language: en
license: cc-by-4.0
tags:
- text-classification
- authorship-verification
- PAN

repo: https://github.com/brashdi22/authorship-verification

---

# Model Card for r88993ia-j09180ga-AV

<!-- Provide a quick summary of what the model is/does. -->

This model is based on the ADHOMINEM (Attention-based Deep network architecture
      Hierarchical cOnvolutional siaMese bIdirectional recurreNt nEural-network Model).
      The model captures both low-level character features and high-level semantic patterns.


## Model Details

### Model Description

<!-- Provide a longer summary of what this model is. -->



- **Developed by:** Ismail Al Brashdi
- **Language(s):** English
- **Model type:** Supervised
- **Model architecture:** DNN

### Model Resources

<!-- Provide links where applicable. -->

- **Paper or documentation:** https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9005650

## Training Details

### Training Data

<!-- This is a short stub of information on the training data that was used, and documentation related to data pre-processing or additional filtering (if applicable). -->

The model was trained on all of the 30K pairs of texts provided as part of the AV training set.

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Training Hyperparameters

<!-- This is a summary of the values of hyperparameters used in training the model. -->


      - learning_rate: 1e-03
      - train_batch_size: 64
      - eval_batch_size: 64
      - seed: 37
      - num_epochs: 14

#### Speeds, Sizes, Times

<!-- This section provides information about how roughly how long it takes to train the model and the size of the resulting model. -->


      - overall training time: 40 minutes
      - duration per training epoch: ~3 minutes
      - model size: 127MB

## Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

### Testing Data & Metrics

#### Testing Data

<!-- This should describe any evaluation data used (e.g., the development/validation set provided). -->

The model was tested on the 6K pairs of texts provided as part of the AV development set.

#### Metrics

<!-- These are the evaluation metrics being used. -->


      - Matthew's Correlation Coefficient
      - ROC-AUC
      - Precision
      - Recall
      - F1-score
      - Accuracy

### Results

The model obtained:
      - Matthew's Correlation Coefficient 0.34:
      - ROC-AUC: 67%
      - Precision: 67%
      - Recall: 67%
      - F1-score: 67%
      - Accuracy: 67%

## Technical Specifications

### Hardware


      - RAM: at least 6 GB
      - Storage: at least 35GB,
      - GPU: L4

### Software


      - NLTK  3.8.1
      - TensorFlow  2.15.0
      - Scikit-Learn  1.2.2

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

Max sentences per document is 30, max words per sentence is 50, max characters per word
    is 20. Anything beyond these lengths will be truncated.

## Additional Information

<!-- Any other information that would be useful for other people to know. -->

The hyperparameters were determined by experimentation
      with different values.
