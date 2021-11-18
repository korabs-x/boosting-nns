Disclaimer: While the approach seemed to work for MNIST, I couldn't improve the performance of other NNs with this approach.

# Boosting Neural Networks
A simple model for MNIST using boosting during training significantly outperforms the equivalent model trained normally in accuracy, but performs worse at minimising the loss.

### Accuracy
![accuracy](images/accuracy.png)

### Loss
![loss](images/loss.png)

### Distribution of number of times each data point is used during training
![Times used](images/times_used.png)

## Approach
Instead of using all data points in each training epoch, we always train on the ones with the previously highest loss. 
In particular, we store the loss value for each data point after each training step, and choose the ones with the highest loss as the next batch for training.
