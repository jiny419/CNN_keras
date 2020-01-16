# Sequential VS Functional

Threre are two ways to build Keras models : sequential and functional

The sequential API allows to create models layer-by-layer for most problems. It is limited in that it does not allow you to create models that share layers or have multiple inputs or outputs

But, the functional API allows to create models that have a lot more flexbility as you can easily define models where layers connect to more than just the previous and next layers. In fact, layers can conncect to any other layer. Creating complex nextworks as **siames networks** and **residual networks** become possible 
