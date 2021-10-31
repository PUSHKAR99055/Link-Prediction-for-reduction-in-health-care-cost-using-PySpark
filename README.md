# Link-Prediction-for-reduction-in-health-care-cost-using-PySpark

We are using CNGF algorithm here:

The algorithm helps in predicting which nodes in a graph are most likely to be connected in the future. 
This can be used for Social Networks to envision connection between various entities.

The algorithm proves to be more efficient than traditional algorithms as it uses the subgraph of two nodes x and y and their common neighbours to forsee their connection in future and not the whole graph. 
It first calculates the Guidance by dividing the degree of a common neighbour in the subgraph with the log of degree of that neighbour in the whole graph. 
Then it takes the sum of guidances of all common neighbours of x and y to compute Similarity. Higher the similarity, more the chance of a connection in future.

It used Jaccard coefficient for predicting similarity.

We can run the file using >> $SPARK_HOME/bin/spark-submit --packages graphframes:graphframes:0.8.0-spark3.0-s_2.12 test.txt " "
for small graph to see the results fast.

or $SPARK_HOME/bin/spark-submit --packages graphframes:graphframes:0.8.0-spark3.0-s_2.12 list.txt " " 
as list.txt contains diseases and their symptoms being arranged into two columns separted by space.
We have to pass two arguments while running one is txt file path and other the separator between the columns of the txt file containing vertices through which graph would be created.

For creating the txt file we can run the main.py file which reads data from dataset.csv file which we collected.

We can also obtain the graph picture being created by running main.py file.(The snapshot is in this folder)

*Snapshots of the result are also in this folder*
