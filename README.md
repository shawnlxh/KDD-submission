# KDD-submission 394

The source code and dataset for our paper: Dynamic Graph Collaborative Filtering. We have implemented our methods in Pytorch.
 
## Usage

To train the DGCF model using the ```data/<network>.csv``` dataset, use the following command. This will save a model 
for every epoch in the ```saved_models/<network>/``` directory.

```python DGCF.py --network <network> --model DGCF --epochs 50 --method attention  --adj --span_num 500 --length 20 ```

This code can be given the following command-line arguments:

```--network:``` choose to the train data:```reddit\wikipedia\lastfm```

```--model:``` this is the name of the model  

```--epochs:```  this is the maximum number of interactions to train the model.

```--embedding_dim:``` this is the number of dimensions of the dynamic embedding.

```--method:```  this is the type of aggregator function in second-order aggregation

```--adj:```  this is a boolean input indicating if use the second relationship.

```--span_num:``` this is to control the size of t-batch

```--length：``` this is the aggregator size in second-order aggregator function.

  
la_all.sh is the batch file to test the model on lastFM. For other datasets, you can use the same format.

Required environments:  
Python 2  
numpy==1.14.6  
gpustat==0.5.0  
tqdm==4.32.1  
torch==0.4.1  
scikit_learn==0.19.1  

For the data download, you can use:  
bash download_data.sh

Some parts of our codes are from jodie: https://github.com/srijankr/jodie/, running environment and initialization are the same as jodie.
