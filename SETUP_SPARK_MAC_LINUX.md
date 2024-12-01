# Setting Up Spark on Mac/Linux

This guide explains how to set up Apache Spark on a Mac or Linux system.

We use PySpark and Python to interact with the Spark processing engine. 

Note: In this guide we are working in your system environment, not VS Code. 
**After** completing this work, we suggest you **restart your computer** to finalize configuration. 

-----

## Download and Install Python

1. Ensure Python 3.8 or greater is installed and available in your path. 


## Install Java Development Kit (JDK)
  
1. Download and install JDK 11 or 17 from [Adoptium](https://adoptium.net/) for an open-source JDK.

Java must be added to your system environment variable named Path. 
We do this later. 

## Install Apache Spark  

1. Go to your Documents folder and create a folder named spark. 

2. Download Apache Spark from the [Spark website](https://spark.apache.org/downloads.html). 

3. Save the .tgz file to your new  Documents\spark folder. 

4. Extract the file. Right click on the tgz file / Extract all. 

Extraction may nest folders (e.g., spark-3.5.3-bin-hadoop3/spark-3.5.3-bin-hadoop3). You can adjust or leave the path as is. 

Spark must be added to your system environment variable named Path. 
We do this later.

## Configure Environment Variables

All environment variables will be set in your shell configuration file.

1. Open your shell configuration file (~/.zshrc or ~/.bashrc) in a text editor:

```zsh
nano ~/.zshrc
```

2. Add the following lines to set up the required environment variables for Java, Spark, and Python:

```zsh
# Java Environment Variable
export JAVA_HOME=$(/usr/libexec/java_home)
export PATH=$JAVA_HOME/bin:$PATH

# Spark Environment Variable
export SPARK_HOME=~/Documents/spark/spark-3.5.3-bin-hadoop3
export PATH=$SPARK_HOME/bin:$PATH
```

3. Save and exit the file (Ctrl+O, Enter, Ctrl+X in nano).

4. Apply the changes.

```zsh
source ~/.zshrc
```

4. Verify the environment variables. 


```zsh
echo $JAVA_HOME
echo $SPARK_HOME
```
Ensure both commands output the correct paths.


## Verify

Restart your machine. 

Open a zsh (or bash) terminal and run the following commands one at a time. 
Be sure a valid version number appears. 
If not, post your results and any error messages in the discussion. 

```zsh
java -version
javac -version
python3 --version
spark-shell
```
