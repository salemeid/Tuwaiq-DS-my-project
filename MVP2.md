## MVP

#### Summary
    
   This an initial commit regarding my findings and understanding during exploration of the chess dataset , The analysis is still at early stage. There is much work ahead. 

#### Findings 

   * My first observation is that dependant column **(traget)** datapoints are imabalancned as per below figure.
   
   ![Target Imbalance Chart](target_imbalance.png)
   
   
   

#### Conclusion and Future Direction
   Starting with logistic regression as The base model, which scored around 67%. 
   
|              |   precision |   recall |   f1-score |     support |
|:-------------|------------:|---------:|-----------:|------------:|
| 0            |    0.994778 | 0.957286 |   0.975672 |  398        |
| 1            |    0.664654 | 0.711763 |   0.687402 | 4021        |
| 2            |    0.649175 | 0.600555 |   0.623919 | 3605        |
| accuracy     |    0.673978 | 0.673978 |   0.673978 |    0.673978 |
| macro avg    |    0.769536 | 0.756535 |   0.762331 | 8024        |
| weighted avg |    0.674074 | 0.673978 |   0.673179 | 8024        |




   The below confusion matrix shows the effect of imbalances and probably some scaling needs to be done.
   ![Confusion Matrix](conf_matrix.png)
   
   
   

