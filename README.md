# From Toxicity to Dialogue: Hate Speech and Counter-Speech in Social Media Environments

Due to restrictions on sharing TikTok data, the exact implementation used in the thesis is not included. Instead, we provide schematic implementations of key components—such as training procedures for hate speech (HS) and counter speech (CS) predictors, a basic implementation of BERTopic, and video clustering using X-CLIP embeddings—alongside guidelines for replicating the techniques and processes discussed. While user handles and video IDs were retained for quality control, we took care not to deanonymize users or access personal information beyond what was publicly available. Given the challenges of full anonymization and the potential for misuse of sensitive data, particularly regarding the LGBTQIA+ community, we opted not to make the full dataset publicly available. However, in the interest of methodological transparency, we will release the code and a sample dataset, enabling integration with labeled datasets from the literature while prioritizing individual safety and data integrity.

## Repository Contents

- **`XCLIPTopic.ipynb`**: Contains a schematic guide for using X-CLIP to embed videos and apply BERTopic. Includes a section on using X-CLIP for text embeddings.

- **`BERTopic.ipynb`**: Provides a basic schematic representation of a general BERTopic implementation.

- **`HateRegularitiesPrediction.ipynb`**: Implements procedures from Section 6 of the thesis to detect hate speech regularities based on video clusters. Includes analysis of SHAP values, percentage of hate per cluster, and hate distribution per hashtag or hashtag pair.

- **`HSandCSPredictionModels.ipynb`**: Contains code for training both hate speech and counter-speech prediction models.

- **`LabeledDataLoading.ipynb`**: Integrates labeled datasets from the literature to create `LabeledHateTrainingDataset.csv` (HS) and `LabeledDialoguesForCounterTraining.csv` (CS).
  
- **`HS&CSPrediction+TopicModeling.ipynb`**: With small sample datasets, replicates the data pipeline from predicting HS and CS, to performing topic modeling on the hate messages.

- **Joined Labeled Data**: Includes the following files with raw data (no pre-processing step has been applied yet). These files are originated from bringing together the different datasets of the folder `Original Labeled Data`:
  - `LabeledHateTrainingDataset.csv` (HS)
  - `LabeledDialoguesForCounterTraining.csv` (CS)

- **Original Labeled Data**: Contains the labeled datasets from the literature used by `LabeledDataLoading.ipynb` to create the files in the folder `Joined Labeled Data`. All links and references to these datasets can be found both in the thesis and the `LabeledDataLoading.ipynb` file:
  - SBIC.v2 folder contains the files of the Social Bias Frames data.
  - DIALOCONAN.csv: DIALOCONAN dataset.
  - Ethos_Dataset_Multi_Label.csv: Ethos dataset.
  - Multitarget-CONAN.csv: Multitarget CONAN dataset.
  - queerPhobia.csv: QueerPhobia dataset.
  - test_suite_cases.csv: HateCheck datest.
  - train.tsv: FRENK dataset.
  - dataset.json: HateXplain dataset.
  
