# Kaggle: INGV - Volcanic Eruption Prediction

Current state: *in progress, debugging*

Version: *4*

## About:
The task of the competition is to detect patterns in a large volcanic dataset. Dataset is comprised of 10 minutes of recordings of 10 seismic sensors being placed around active volcanos. Approximately 4 thousand of recording pieces have corresponding time-to-eruption value, while model task is to predict this metric for another 4 thousand pieces.
## Model:
Currently, model extracts spectrograms from corresponding waveforms to detect patterns as proposed in Chouet article on eruption forecasting. After, spectrograms are being fed to 
16 layer CNN(7 conv layers, 5 pooling layers, 4 fully connected layers). Model is being trained on Kaggle GPU.

Hyperparameter | Value
---|---
Learning rate | *1e-3*
Optimizer | *Adam, beta1=0.9, beta2=0.999, eps=1e-6*
Number of epochs | *10*
## Todo:
As for right now, model might simultaneously start to produce Nan values as gradients become Nan during the training process. Model is thought to be suffering from exploding gradinets problem, which is being object for investigation and debugging.
## References:
[Competition page](https://www.kaggle.com/c/predict-volcanic-eruptions-ingv-oe)

[Article on eruption forecasting](https://www.nature.com/articles/380309a0)
