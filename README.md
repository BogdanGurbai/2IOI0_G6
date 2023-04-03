# 2IOI0_G6

<mark>Warning</mark>, install the required packages before running the notebook.
## python version
3.9.13 or higher

## File
The main JupiterNotebook of this project is the **Jnote.ipynb**. <br>
The final CSV is **S4_Decision_Tree_Estimator.csv**. It contains all the columns from the previous estimators.
## Predictor
The follow list contains all the Predictors our group has implemented:
1. Naive Predictor (Trace based)
2. Mode and Mean Predictor
3. Linear Regression Predictor
4. Decision Tree Predictor

## Structure
The notebook is structured in the way that we list the needed helper methods, then construct the predictor.

## Package
Uncomment the line to install the missing packages. Juypter Note will install them for you.
<br>
```# %pip install pandas``` -> ```%pip install pandas```


# CSV & Other form of outputs


### Sprint 1
- ```S1_Ground_Truth.csv``` -> <br>
```BPI_Challenge_2012.XE-test``` + [Ground_Truth]
- ```S1_Naive_Estimator.csv``` -> <br>
```BPI_Challenge_2012.XE-train.csv``` + [Ground_Truth + naive_predictions]

### Sprint 2
- ```S2_Agreggation_Estimator.csv``` -> <br>
```S1_Naive_Estimator.csv``` + [Mode_Estimator(event+time)]
- ```S2_Remove_Overlap.csv``` -> <br>
```S1_Ground_Truth.csv``` - Traces that overlap with the test set and outliers

### Sprint 3
- ```aggregation_encoding_train.csv``` -> <br>
[Ground_Truth] + [encoding_of_the_train_prefixes] + ['holidays'] + ['last_activity']

- ```aggregation_encoding_test.csv``` -> <br>
[Ground_Truth] + [encoding_of_the_test_prefixes] + ['holidays'] + ['last_activity']

- ```S3_Regression_Estimator.csv``` -> <br>
```S2_Agreggation_Estimator.csv``` + [Regression_Estimator(event+time)]

- ```S3_Random_Dict_Predictions``` -> <br>
10 * ```S3_Regression_Estimator.csv``` made with different mappings of activity -> numbers to test if the transforming of the data adds additional unwanted meaning to it

### Sprint 4
- ```S4_Decision_Tree_Estimator.csv``` -> <br>
```S3_Regression_Estimator.csv``` + [Decision_Tree_Estimator(event+time)]
