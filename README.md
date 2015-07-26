# DeepBeliefNet
A simple, clean Python implementation of Deep Belief Networks with binary units based on 
> Fischer, Asja, and Christian Igel. "Training restricted Boltzmann machines: an introduction." Pattern Recognition 47.1 (2014): 25-39.

## Usage
This implementation follows the scikit-learn way to work:
  
    # Create a DBN with three layers containing 50, 50 and 200 hidden units respectively
    dbn = DBN(hidden_layers_structure=[50, 50, 200], learning_rate=0.1, max_iter_backprop=30,
              max_epochs_rbm=10, lambda_param=0.1)
    
    # Learn from data in X in a unsupervised way
    dbn.fit(X)
    
    # Or learn in a supervised way performing fine-tuning using labels
    dbn.fit(X, y)
    
    # Transform data in X
    X_transformed = dbn.transform(X)
    
    # Predict data in X (if learnt in a supervised way)
    X_predicted = dbn.predict(X)
    
## Requierements
NumPy and scikit-learn packages must be installed in the system. If aren't, simply do:
    
    pip install numpy
    pip install scikit-learn
  
