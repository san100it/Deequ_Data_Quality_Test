# Deequ_Data_Quality_Test

**********  This is Custom Implementation of Data Quality check Tool - Pydeequ By AWS. which is Data Qulity check library for Spark. *****************
***************************************** This is Implemented in Python on AWS Glue ******************************************

Spark Version - 3.0.0
Pydeequ version :- 1.2.2
Glue version :- Glue3.0 -Supports spark 3.1, scala 2, Python 3
Jar :- deequ-1.2.2-spark-3.0.jar

Required :
Pydeequ Configuration for AWS Glue :-  
Pass parameter **--ConfgurationFile**="Path for Deequ Configuration File.csv"
**Python library path** =  "Path containing pydeequ.zip" 
Steps for Creating pydeequ.zip :-  wget https://repo1.maven.org/maven2/com/amazon/deequ/deequ/1.2.2/deequ-1.2.2-spark-3.0.jar 
                                   cd python-deequ && zip -r ../pydeequ.zip pydeequ && cd ../
                                   aws s3 cp deequ-1.2.2-spark-3.0.jar  s3://<__YOUR_BUCKET__>/dependencies/
                                   aws s3 cp pydeequ.zip s3://<__YOUR_BUCKET__>/dependencies/

**Dependent jar path** :- "Path for directory containing deequ-1.2.2-spark-3.0.jar"

It Performs Below Data Qulity checks for Data on AWS s3 ( exposed using athena tables)

1. Completness check (Not null exist check)
2. Referential Integrity check
3. DUplicate check
4. If value exists in column check
