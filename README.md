# Time Series Forecasting
## Description of the problem
The goal of the project is to predict future samples of a multivariate time series. 
The TimeSeries Forecasting problem is characterized by analysing a sequence of data showing past interactions and behaviour, and eventually exploiting recurrencies and seasonalities the model can make a reliable prediction of how will be the future for a fixed number of timesteps
<p align=center>
  <img width="412" alt="Schermata 2021-11-29 alle 14 37 38" src="https://user-images.githubusercontent.com/79969755/143877722-613956ca-cdd1-4ce9-be17-075853540133.png">
</p>

## Final Model 
In the end, what proved to make a significant difference was the implementation of an
Attention layer. The model is as follows:
1. Bidirectional LSTM, 512 units and return sequences + Dropout(p=0.3)
2. Attention Layer
3. RepeatVector
4. TimeDistributed Dense, 512 units + Dropout(p=0.3)
5. Bidirectional LSTM, 512 units and return sequences + Dropout(p=0.3)
6. Attention Layer
7. Dense + Reshape as seen in class to correctly format output tensor  

Hyperparameters: Window: 800 | Stride: 5 | Telescope: 144 | Batch Size = 128  
We tried to combine this Attention Layer with various models, using different approaches
and different architectures but in the end this model listed here was the best performing
one on the leaderboard, with a score of 3.6204 RMSE.

# Group components:
Group Name:<b> Gamma </b>

- [Gabriele Rivi](https://github.com/GabrieleRivi)
- [Mattia Redaelli](https://github.com/redaellimattia)
- [Ariel Ratzonel](https://github.com/ArielRatzonel00)

