# Apache Spark
Apache Spark is an open-source,distributed computing system designed for big data processing and analytics.
Hadoop is designed for processing large scale data by distributing the workload across multiple machines.However,it stores the data on the disk,which makes data processing slower because each operation requires reading from and writing to disk.
Compared to Hadoop with Apache Spark,Apache Spark stores the data in the memory which is 10x times faster than Hadoop which minimizes the disk usage.
Apache Spark handles large scale data by distributing the workload across cluster of machines.

# PySpark
PySpark is the Python API for Apache Spark.
It allows you to use Python programming to harness the power of Apache Spark's distributed computing engine.

# Pyspark Architecture
PySpark is built on top of Apache Spark and follows Master-Slave architecture.
Components:
1.Driver Program
2.Spark Context
3.Cluster Manager
4.Worker Node
5.Executor

**Workflow**:
Spark follows master-slave architecture. Driver Program acts as the master and Executor acts as the slave/worker nodes.
1.User writes a spark application and submits it to the cluster.
2.Driver Program is the heart of the spark application which starts and creates a spark context(entry point), which establishes a connection/spark session with the cluster manager.
3.Cluster Manager allocates resources(CPU,memory) on worker nodes and launches executor processes.
4.Driver Program then breaks the jobs into tasks and sends them to executors.
5.Executors runs the tasks in parallel,process the data and store intermediate results in memory for fast access.
6.Results are sent back to the Driver Program,which combines them and returns the final output to the user and stops the cluster.
