# **Speech analysis and Text classification** 
##Introduction
Text and speech classification models are the future in terms of mental health illness diagnosis as depression. According to the World Health Organization (WHO), 322 million people worldwide suffer from depression. The objective of this investigation is to analyze some of the newest models for classification to determine whether they are a good tool that doctors and therapists could use un a near future.  

## Methods
### Dataset

For the datasets we used IEMOCAP that contains the audio files needed for speech analysis as well as its transcription, thanks to this features we were able to use this dataset for both speech and text analysis. We also used EmoDB dataset for speech analysis.

### Classification
For speech analysis we used EmoAudioNet model shown in figure 1.
The models used for text classification were BERT and LSTMs, we used this models as we consider we would get   results with good accuracy. We used  Pytorch as our open source machine learning library for BERT as well as Keras for  EmoAudioNet and for our LSTM + BERT text analysis.


## Results
### EmoAudioNet
After 150 epochs in speech analysis we ended up with a 87% accuracy a great result for our speech model.

### BERT
For BERT we got a 89% accuracy, despite this fact some of the emotions had a lower accuray, this could be caused by our dataset label distribution.

### BERT+LSTM
After getting those values with Bert we decided to combine such model with an LSTM to obtain better results, at the end of our training we ended up with a 94% accuracy actually improving our previous model.

## Conclusion
Despite having some trouble at the beginig with EmoAudioNet we ended up getting great accuracy of 84%. For text classification with BERT and LSTMs the results were great as well 89% and 94% accuracy.
This models can be used in the future for an acurrate sentiment classification that could help specialists in mental health areas.


# Cómo correr los códigos
# Final-Project : Speech and text classification for sentiment analysis
## EmoAudioNet
Para este modelo se deben usar los archivos de la carpeta data --> ColabTrainingFiles.
## BERT + LSTM
El dataset utilizado es IEMOCAP y se encuentra en la carpeta data--> text_audio.csv
## BERT 
El dataset para correr el clasificador de sentimientos se encuentra en el folder data-->DATASET_PROYECTO_NLP.csv el cual también pertenece al dataset de IEMOCAP.

En la siguiente liga se encuentra el checkpoint del entrenamiento de dicho modelo. 

checkpoints: https://drive.google.com/drive/folders/1r0hBIOWnKkLzQnUXplr5D_HPLFBCmSeT?usp=sharing
