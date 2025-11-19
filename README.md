# Project Description
I started with a simple convolutional neural network model based on the lecture source code, with the following structure:

1 convolutional layer, learning 32 filters using a 3x3 kernel  

1 max-pooling layer, using a 2x2 pool size  

1 hidden layer with 128 nodes  

0.5 dropout rate  

output layer with output units for all traffic sign categories  

I then tested different modifications to the base model, with the goal of finding a model with the best testing accuracy.

## Experiment Results
| Modification | Testing accuracy |
|---|---:|
| Base model|	                                                                                          0.0544|
| Add second convolutional layer, identical to the first |                                              0.9708|
| Add second maxpooling layer (after the second convolutional layer), identical to the first |	        0.9503|
| Remove second maxpooling layer, increase kernal size in second convolutional layer to (4, 4) |	      0.9480|
| Double number of filters (to 64) in second convolutional layer |	                                    0.9684|
| Double number of nodes in hidden layer to 256 |	                                                      0.9528|
| Add second hidden layer (both layers with 128 nodes) |	                                              0.9511|
| Remove dropout |	                                                                                    0.9486|
| Increase dropout rate to 0.7 |	                                                                      0.9022|
|	Decrease dropout rate to 0.2 |	                                                                      0.9491|


The base model performed very poorly, with only 0.0544 testing accuracy. Adding a second convolutional layer dramatically improved accuracy to 0.9708. None of the other tested models were able to top this accuracy score. However, adding a second max-pooling layer, doubling the number of filters in the second convolutional layer, and doubling the number of nodes in the hidden layer all yielded promising results, with accurcy scores above 0.95.
