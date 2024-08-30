# From Toxicity to Dialogue: Hate Speech and Counter-Speech in Social Media Environments

Due to restrictions on sharing TikTok data, this repository does not include the exact implementation used in the thesis. Instead, it provides the schema and guidelines for the techniques and processes discussed in the thesis, along with access to the labeled data. The repository features schematic implementations of key components, including training procedures for hate speech (HS) and counter speech (CS) predictors, a basic implementation of BERTopic, and video clustering using X-CLIP embeddings. Although the TikTok data itself cannot be shared, the code allows for integration with labeled datasets from the literature.

## Repository Contents

- **`XCLIPTopic.ipynb`**: Contains a schematic guide for using X-CLIP to embed videos and apply BERTopic. Includes a section on using X-CLIP for text embeddings.

- **`BERTopic.ipynb`**: Provides a basic schematic representation of a general BERTopic implementation.

- **`HateRegularitiesPrediction.ipynb`**: Implements procedures from Section 6 of the thesis to detect hate speech regularities based on video clusters. Includes analysis of SHAP values, percentage of hate per cluster, and hate distribution per hashtag or hashtag pair.

- **`HSandCSPredictionModels.ipynb`**: Contains code for training both hate speech and counter-speech prediction models.

- **`LabeledDataLoading.ipynb`**: Integrates labeled datasets from the literature to create `LabeledHateTrainingDataset.csv` (HS) and `LabeledDialoguesForCounterTraining.csv` (CS).

- **Joined Labeled Data**: Includes the following files with raw data (no pre-processing step has been applied yet):
  - `LabeledHateTrainingDataset.csv` (HS)
  - `LabeledDialoguesForCounterTraining.csv` (CS)

- **Original Labeled Data**: Contains the labeled datasets from the literature used by `LabeledDataLoading.ipynb`to create the files in the folder `Joined Labeled Data`.
  
