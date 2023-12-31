<h1>FNN Builder</h1>

A simple NumPy feedforward neural networks builder</br>

<a name="usage"/>

## Usage

#### Build

```python
model = FNN(lossFunction = Loss.CE, inputs = 4)
model.normalize(x = True, y = False)
model.addLayer(activation = Activation.RELU, neurons = 4)
model.addLayer(activation = Activation.SIGMOID, neurons = 3)
model.addLayer(activation = Activation.SOFTMAX, neurons = 3)
```
#### Train

```python
model.train(x_train, y_train, epochs = 10000, rate = .01, batch_size = 5)
```

#### Predict

```python
model.predict(x_test)
```

#### Test

```python
model.test(y_test)
```
</br>

> *y_train*, *y_test* : `pandas.core.series.Series`  
> *x_train*, *x_test* : `pandas.core.frame.DataFrame`

---

 <div align="center">
   
 [Usage](#usage) 
| [Features](#features) 
| [Requirements](#requirements) 
| [Notebook](FNN.ipynb) 
 
 </div>


<a name="features"/>

## Features

#### Activation functions
- Sigmoïd `Activation.SIGMOID`
- ReLU `Activation.RELU`
- Softmax `Activation.SOFTMAX`

#### Loss functions
- Categorical Cross Entropy `Loss.CE`
- Mean Squared Error `Loss.MSE`

#### Normalization
- Rescaling (min-max normalization)

#### Gradient-based Optimization
- Stochastic Gradient Descent : `batch_size = 1`
- Mini-batch : `batch_size = n` 
- Batch :  `batch_size = len(x_train.index)`



<a name="requirements"/>

## Requirements
- numpy
- pandas
- matplotlib
