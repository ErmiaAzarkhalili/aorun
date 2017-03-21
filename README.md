# Aorun: A high-level API for PyTorch

Aorun is highly inspired by Keras API.

## Getting started

Here is a simple regression example:

```python
from aorun.models import Model
from aorun.layers import Dense, Activation
from aorun.optimizers import SGD

model = Model()
model.add(Dense(10, input_dim=3))
model.add(Activation('relu'))
model.add(Dense(1))

sgd = SGD(lr=0.001)
model.fit(X_train, y_train, loss='mse', optimizer=sgd)

y_pred = model.forward(X_test)
```

## TODO:

* Model.fit:
    - verbose level
    - validation set
    - set optimizer with string
* Add layers:
    - Convolutional2D
    - RNN
    - GRU
    - LSTM
* Add losses:
    - Hellinger distance
* Add optimizers:
    - Adam
    - RMSProp
* Add initializations:
    - glorot normal
    - glorot uniform
* Add examples:
    - mnist
    - cifar10
* Refactoring:
    - variational loss

## Why Aorun?

[Aorun](https://en.wikipedia.org/wiki/Aorun) is a Dinosaur. Dinosaurs are cool.
