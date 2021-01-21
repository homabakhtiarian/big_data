# Spark
This notebook will serve as reference code for the Big Data section of the course involving Amazon Web Services. 

First we create a SparkContext. A SparkContext represents the connection to a Spark cluster, and can be used to create an RDD and broadcast variables on that cluster.

*Note! You can only have one SparkContext at a time the way we are running things here.*

We're start with a 'hello world' example, which is just reading a text file. So we have to create a text file.

After that we can take in the textfile using the **textFile** method off of the SparkContext we created. This method will read a text file from HDFS, a local file system (available on all
nodes), or any Hadoop-supported file system URI, and return it as an RDD of Strings.

Spark’s primary abstraction is a distributed collection of items called a Resilient Distributed Dataset (RDD). RDDs can be created from Hadoop InputFormats (such as HDFS files) or by transforming other RDDs. 

RDDs have actions, which return values, and transformations, which return pointers to new RDDs.

Now we can use transformations, for example the filter transformation will return a new RDD with a subset of items in the file.
