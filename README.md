# Project Title

XAI-CNVMARKER: : Explainable AI-based Copy Number Variant Biomarker Discovery for Breast Cancer Subtypes

## Description

XAI-CNVMarker is an explainable AI-based post-hoc biomarker discovery framework to discover a small set of interpretable biomarkers. We exploit the power of deep learning to build DLmodel -- a deep learning model  for breast cancer classification. Subsequently, the trained model is analyzed using different explainable AI methods to arrive at a set of 44 CNV biomarkers. Using 5-fold cross-validation, we obtained a classification accuracy of 0.712. Gene set analysis revealed 37 subtype-specific enriched Reactome and Kegg pathways, 21 druggable genes, and 13 biomarkers linked with the prognostic outcome. Finally, we validated the efficacy of the identified biomarkers on METABRIC. Thus, the proposed framework demonstrates the role of explainable AI in discovering clinically reliable biomarkers.

## Getting Started

### Dependencies

For data pre-processing, model construction, and visualization, Python libraries namely, Pandas, Numpy, Imblearn, Keras, Matplotlib, Scikit-Learn, and Seaborn have been used. Methods of the DeepExplain tool and SHAP libraries have been applied for the purpose of explainability. Runtime environment used in this project is Google Colaboratory using Python 3.7 on NVIDIA Tesla K80 GPU.


### Executing program

**Autoencoder.ipynb:** We first exploit the power of deep learning to build DLmodel -- a deep learning model comprising an autoencoder for dimensionality reduction. An autoencoder comprises an encoder and a decoder. The encoder network compresses a large number of input features to a small number of outputs. The outputs of the encoder network are fed to the decoder network which tries to reconstruct the original input data.
**Phase2+3_DLModel.ipynb:** The second module of _DLmodel_ is a classifier modeled as a feed-forward neural network that takes as input, the output of the encoder module of the autoencoder (a vector of size 500). The network comprises a hidden layer having 200 nodes, followed by an output layer comprising five nodes representing the five breast cancer subtypes.
**KneeLocator_Attributions_Positive_Analysis.ipynb**: CNV Biomarker Discovery Algorithm (CBDA) that incorporates different explainable AI methods to mark the relative relevance of the genes
**Classifier_44+SHAP.ipynb**: Relevance of discovered biomarkers in distinguishing different breast cancer subtypes determined using SHapley Additive exExplanations (SHAP).


## Authors

Sheetal Rajpal, Ankit Rajpal, Manoj Agarwal, Virendra Kumar, Ajith Abraham, Divya Khanna, Naveen Kumar
