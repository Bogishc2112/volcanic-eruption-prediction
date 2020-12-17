# Kaggle: INGV - Volcanic Eruption Prediction
---
| Current stage | *model debugging* |

| Current version | *4* |

## About:
The task of the competition is to detect patterns in a large volcanic dataset. Dataset is comprised of 10 minutes of recordings of 10 seismic sensors being placed around active volcanos. Approximately 4 thousand of recording pieces have corresponding time-to-eruption value, while model task is to predict this metric for another 4 thousand pieces.
## Model:
Currently, model extracts spectrograms from corresponding waveforms to detect patterns as proposed in Chouet article on eruption forecasting. After, spectrograms are being fed to 
16 layer CNN(7 conv layers, 5 pooling layers, 4 fully connected layers). 
