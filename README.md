# complex_surface_analysis
This repository includes unsupervised (k-means clustering) and supervised (RF and CNN) machine learning models for analyzing complex surface topographies. 
_________________________________________________________________________________________________________________________________________________________________________
Cite as: {Henkel, M., Sprenger, M., and Lieleg, O., Machine learning for small data sets: an exemplary study on the classification of highly complex surface micromorphologies, unpublished work}
_________________________________________________________________________________________________________________________________________________________________________
The k-means clustering model and the RF model can be tested using the attached numerical datasets comprising:
-  pristine (NOD) Polytetrafluorethylen (PTFE) samples;
-  PTFE samples subjected to abrasive (ABR), adhesive (ADH), and erosive (ERO) wear;
-  PTFE samples subjected to dual combinations of these wear types.
These datasets where obtained by calculating a set of surface parameters according to DIN EN ISO 25178-2:2012-09 from the individual surface topografies of each sample.

Furthermore, to run these codes, the repository provides the NETCORE algorithm that is used by these models to remove redundant features in the datasets
_________________________________________________________________________________________________________________________________________________________________________
The CNN models comprise:
-  a shallow CNN for training (CNN.ipynb and config_CNN.yaml) ;
-  a CNN predictor for calssifying new data based on a previously trained CNN model(CNN_predictor.ipynb and config_predictor.yaml);
-  a few-shot learning (FSL) model for training on scarce data based on a pretrained CNN-backbone (FSL.ipynb and config_FSL.yaml).

To test these models, the repository includes a set of trained model parameters for each of these models:
-  best_model.pth: Model parameters of the CNN;
-  feature_extractor.pth: Model parameters for the CNN-backbone for FSL;
-  best_fsl_model.pth: Model parameters of the FSL model (trained on 20 images/class)

To test these models, the repository further includes a small test dataset containing topgraphy images of:
-  pristine (NOD) Polytetrafluorethylen (PTFE) samples;
-  PTFE samples subjected to abrasive (ABR), adhesive (ADH), and erosive (ERO) wear;
-  PTFE samples subjected to dual combinations of these wear types.
_________________________________________________________________________________________________________________________________________________________________________
