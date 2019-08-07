# CarND-Semantic-Segmentation-Project

Self-Driving Car Engineer Nanodegree Program, Term3. CarND-Semantic-Segmentation-Project solution by Ernesto Cañibano.

## Training the model

In this section i explain the process of train the model.

### Hyperparameters

After several trainings, finally the hyperparameters selected for the final model are the following:
* **Dropout = 0.5** [Line 134](./main.py#L134)
* **Learning rate = 1e-5** [Line 135](./main.py#L135)
* **Epochs = 50** [Line 154](./main.py#L154)
* **Batch size = 4** [Line 155](./main.py#L155)
* **Standard deviation = 1e-2** [Line 62](./main.py#L62)
* **L2 regularization in layers = 1e-4** [Line 63](./main.py#L63)
* **L2 regularization additional = 1e-4** [Line 96](./main.py#L96)
 
### Training process

The first attempts were made without L2 additional regularization and with a value of the **L2 regularization value in layers** of **1e-5**.

###### 10 epochs
![](trainning_results/no_regularization/tranning_epochs=10.png) 
![](trainning_results/no_regularization/epochs=10/um_000000.png)
![](trainning_results/no_regularization/epochs=10/umm_000050.png) 
###### 20 epochs
![](trainning_results/no_regularization/tranning_epochs=20.png) 
![](trainning_results/no_regularization/epochs=20/um_000000.png)
![](trainning_results/no_regularization/epochs=20/umm_000050.png) 
###### 30 epochs
![](trainning_results/no_regularization/tranning_epochs=30.png) 
![](trainning_results/no_regularization/epochs=30/um_000000.png)
![](trainning_results/no_regularization/epochs=30/umm_000050.png) 
###### 40 epochs
![](trainning_results/no_regularization/tranning_epochs=40.png) 
![](trainning_results/no_regularization/epochs=40/um_000000.png)
![](trainning_results/no_regularization/epochs=40/umm_000050.png) 
###### 50 epochs
![](trainning_results/no_regularization/tranning_epochs=50.png) 
![](trainning_results/no_regularization/epochs=50/um_000000.png)
![](trainning_results/no_regularization/epochs=50/umm_000050.png) 

A test with **80 epochs** was made too but the result was pretty similar to the 50 epochs test.

Later I tried to improve the model adding an **additional L2 regularization**. I made trainings with different values but the best was with a value of **1e-4**.

###### 50 epochs, 1e-4 additional L2 regularization
![](trainning_results/regularization/tranning_regularizaction=0.0001-epochs=50_.png) 
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/um_000000.png)
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/umm_000050.png) 

Finally i tried some more test testing different values for the **Dropout** but I decided use **0.5**.

### Results
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/um_000007.png)
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/um_000020.png)
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/um_000073.png)
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/uu_000011.png)
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/uu_000062.png)
![](trainning_results/regularization/regularizaction=0.0001-epochs=50_/uu_000098.png)




