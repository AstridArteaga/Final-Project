# **Speech analysis and Text classification** 
##Introduction
Text and speech classification models are the future in terms of mental health illness diagnosis as depression. According to the World Health Organization (WHO), 322 million people worldwide suffer from depression. The objective of this investigation is to analyze some of the newest models for classification to determine whether they are a good tool that doctors and therapists could use un a near future.  

## Methods
### Dataset

For the datasets we used IEMOCAP that contains the audio files needed for speech analysis as well as its transcription, thanks to this features we were able to use this dataset for both speech and text analysis. We also used EmoDB dataset for speech analysis.

### lassification
For speech analysis we used EmoAudioNet model shown in figure 1.
The models used for text classification were BERT and LSTMs, we used this models as we consider we would get   results with good accuracy. We used  Pytorch as our open source machine learning library for BERT as well as Keras for  EmoAudioNet and for our LSTM + BERT text analysis.
{"A?":"B","a":5,"d":"B","h":"www.canva.com","c":"DAEgjCKMOx4","i":"Aj_rj3cs5IiQPsCM_-RoAQ","b":1623013015194,"A":[{"A?":"I","A":1336.0215957370858,"B":37.364326052669355,"D":713.5803779662922,"C":354.0582579802123,"a":{"B":{"A":{"A":"MAEglIQKUDI","B":1},"B":{"A":-5.684341886080802e-14,"B":-5.684341886080802e-14,"D":713.5803779662923,"C":354.05825798021243}}}}],"B":1728,"C":2304}

## Results
### EmoAudioNeta
After 150 epochs in speech analysis we ended up with a 87% accuracy a great result for our speech model.
BERT
{"A?":"B","a":5,"d":"B","h":"www.canva.com","c":"DAEgjCKMOx4","i":"Aj_rj3cs5IiQPsCM_-RoAQ","b":1623013015194,"A":[{"A?":"I","A":492.3881549098701,"B":979.1879109598171,"D":278.35191084512905,"C":250.7010587744208,"a":{"B":{"A":{"A":"MAEglHBYcpE","B":1},"B":{"A":-5.684341886080802e-14,"D":278.35191084512905,"C":250.70105877442091}}}}],"B":1728,"C":2304}
### BERT
For BERT we got a 89% accuracy, despite this fact some of the emotions had a lower accuray, this could be caused by our dataset label distribution.
{"A?":"B","a":5,"d":"B","h":"www.canva.com","c":"DAEgjCKMOx4","i":"Aj_rj3cs5IiQPsCM_-RoAQ","b":1623013015194,"A":[{"A?":"I","A":942.1509781970626,"B":816.4763418954157,"D":397.74587947909583,"C":267.2033214381859,"a":{"B":{"A":{"A":"MAEglKeQNik","B":1},"B":{"A":5.684341886080802e-14,"B":-5.684341886080802e-14,"D":423.3063144889153,"C":267.20332143818575}}}}],"B":1728,"C":2304}
###BERT+LSTM{"A?":"B","a":5,"d":"B","h":"www.canva.com","c":"DAEgjCKMOx4","i":"Aj_rj3cs5IiQPsCM_-RoAQ","b":1623013015194,"A":[{"A?":"I","A":1037.0592466627515,"B":1221.661426216973,"D":292.56079515753885,"C":172.29505297249705,"a":{"B":{"A":{"A":"MAEglHAH90M","B":1},"B":{"A":-8.526512829121202e-14,"B":-17.517515865388333,"D":345.23950885435266,"C":173.70541326005167}}}}],"B":1728,"C":2304}
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
