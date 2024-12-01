# smart-sales-spark

This project provides an introduction to using Apache Spark for data processing and analysis. 
It includes hands-on examples for working with Spark DataFrames and instructions for setting up Spark on your local machine.

Apache Spark is a powerful distributed computing framework widely used for big data processing, machine learning, and real-time analytics. 

We can use Spark with structured data using Spark DataFrames, query data with SQL, or process unstructured data using RDDs (Resilient Distributed Datasets).

## Versions Matter!

This guide has been tested with:

-Python 3.10.11 (newest is 3.12.4 - which does NOT work)
-PySpark 3.5.3
-Spark 3.5.3
-JDK 17
-Winutils for Spark 3

## Apache Spark Homepage

Read about Spark’s features and capabilities on the [Apache Spark Homepage](https://spark.apache.org/).

## Apache Spark Examples

Visit the [Apache Spark Examples Page](https://spark.apache.org/examples.html) to work through Spark’s official examples, including:
- DataFrame Example -  demonstrates creating a Spark DataFrame and performing operations like filtering, aggregation, and adding columns.
- SQL Example - illustrates how to query data using Spark SQL.
- RDD Example - ntroduces RDDs for processing unstructured data.
- Streaming Example - shows how to handle real-time data-in-motion with structured streaming.

## FIRST: Set Up Your Machine

Follow the instructions to set up your system first:

- [Setup for macOS/Linux](SETUP_SPARK_MAC_LINUX.md)
- [Setup for Windows](SETUP_SPARK_WINDOWS.md)

## SECOND: Activate your local Virtual Enviroment & Install Dependencies

Examples of .gitignore and requirements.txt are provided (yours may vary).

The project assumes the smart sales respository is organized like the following (yours may vary - adjust your paths using pathlib to reflect your existing project layout). 

```
project/
├── data/prepared
│   ├── customers_data_prepared.csv
│   ├── products_data_prepared.csv
│   ├── sales_data_prepared.csv
├── scripts/
│   ├── spark_basic.py
│   ├── spark_sales_yourname.py
├── .gitignore
├── README.md
└── requirements.txt
```

Follow the instructions to manage your local virtual environment:

- [VIRTUAL_ENV](VIRTUAL_ENV.md)

## THIRD: Run PySpark Basic Script

We keep our Python scripts in the scripts folder.

Create a new file scripts/spark_basic.py in your scripts folder. 
Paste the contents from the file provided in this repo.

### Windows 

1. In VS Code, open a PowerShell terminal in the root project folder. 

2. Activate your local project environment everytime you open a terminal to work on the project. 

```shell
.\.venv\Scripts\activate
```

Protip: After running the command once, you can usually get it back by typing just the initial dot and then hitting the right arrow key  - or use the up arrow to access prior commands. 

3. Execute the script

```shell
py scripts\spark_basic.py
```

Protip: After running the command once, you can usually get it back by typing just the initial py and then hitting the right arrow key - or use the up arrow to access prior commands. 

If you get a Windows Firewall alert regarding the JDK, click Allow. 


### Mac/LInux 

1. In VS Code, open a terminal in the root project folder. 

2. Activate your local project environment everytime you open a terminal to work on the project. 

```zsh
source .venv/bin/activate
 
```

3. Execute the script

```zsh
python3 scripts/spark_basic.py
```

## FOURTH: Run PySpark Project Script

Create a new file scripts/spark_sales_yourname.py in your scripts folder. 
Change yourname to reflect your unique name or brand.

Paste the contents from the file provided in this repo.

Execute the script to get started.Choose the appropriate command. 

```shell
py scripts/spark_sales_yourname.py
python3 scripts/spark_sales_yourname.py
```

## Adjust for Project Objectives

After running both provided scripts successfully, modify the the spark sales script to reflect your unique project objectives. 


## Troubleshooting



```powershell
$Env:HADOOP_HOME

Test-Path "$Env:HADOOP_HOME\bin\winutils.exe"

$env:Path = [System.Environment]::GetEnvironmentVariable("Path", "Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path", "User")
```


# BYPASS LOCAL INSTALLATION - TRY IT ON THE WEB

- <https://hub.ovh2.mybinder.org/user/apache-spark-rwmw01td/notebooks/python/docs/source/getting_started/quickstart_df.ipynb>

- <https://colab.research.google.com/drive/1fa2G3YuXx3Isqyby5kFETqmWotFwtqlH?usp=sharing>

- <https://github.com/apache/spark/tree/master/examples/src/main/python>