# Sequential VS Functional

Threre are two ways to build Keras models : sequential and functional

The sequential API allows to create models layer-by-layer for most problems. It is limited in that it does not allow you to create models that share layers or have multiple inputs or outputs

But, the functional API allows to create models that have a lot more flexbility as you can easily define models where layers connect to more than just the previous and next layers. In fact, layers can conncect to any other layer. Creating complex nextworks as **siames networks** and **residual networks** become possible 


## Sequential

```
form keras.models import Sequential
from keras.layers import Dense

model = Sequential()
model.add(Dense(2, input_dim=1))
model.add(Dense(1))

```

- Sequential API is used in developing deep learning models in most situation, but there are three limitations 
1. multiple inputs cannot be created
2. multiple outpus cannot be created
3. cannot reuse layers


## Functional

```
from keras.models import Model
from keras.layers import Input
from keras.layers import Dense

Input = Input(shape(2,))
hidden = Dense(2)(Input)

model = Model(inputs=Input, outputs=hidden)
```

- Functional API can create multiple input or output models as well as models that share layers
- Models defined by defining a **Model** that specifies the layers to act as the **input** and **output** to the model. 
- **input** and **output** should be definitely defined by ther hyperparemter **shape**
