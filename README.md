blog-spark-recommendation
=========================

Simple example on how to use recommenders in Spark / MLlib using the Play framework.
More info on our blog: http://chimpler.wordpress.com/2014/07/22/building-a-food-recommendation-engine-with-spark-mllib-and-play/

Setup
=====

You will need:

* Scala 2.10+
* Play Framework
* MongoDB

Scala and Play Framework will be automatically installed by `sbt` command, while MongoDB should be installed **manually**.

Download the food review file (500K reviews) using the `download.sh` script.

Running the example
===================
Run mongodb daemon in a shell:
```
mongod --dbpath=/data/db --fork --logpath=log/mongodb.log
```

Start application in another shell:
```
sbt
[blog-spark-recommendation] $ play
[blog-spark-recommendation] $ package
[blog-spark-recommendation] $ run 9010
```
Any stage could be interrupted due to unknown reason. Retry these commonds until success.

**Note**: This project use Apache Spark, which is integrated in the project. Outer Spark has no effect with this project.
