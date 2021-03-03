# Character-based Language Modeling with Long short-term memory 

# Running.

First, ensure that you are in the same directory with the python files and the "data" directory with the "input.txt" inside. 

## Training
- This code is provided as a simple implementation of the LSTM model, and how to generate character sequences from this model. You are encouraged to change the model hyper-parameters (model size, learning rate, batch size ...) to see their effects in training.

```
python lstm.py train
```


## Gradent checking 
- Checking the gradient correctness. This step is normally important when implementing back-propagation. The idea of grad-check is actually very simple:

+ We need to know how to verify the correctness of the back-prop implementation.
+ In order to do that we rely on comparison with the gradients computed using numerical differentiation
+ For each weight in the network we will have to do the forward pass twice (one by increasing the weight by \delta, and one by decreasing the weight by \delta)
+ The difference between two forward passes gives us the gradient for that weight
+ (maybe the code will be self-explanationable)

```
python lstm.py gradcheck
```

