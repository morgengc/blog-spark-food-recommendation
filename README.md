blog-spark-recommendation
=========================

Simple example on how to use recommenders in Spark / MLlib using the Play framework.
More info on our blog: http://chimpler.wordpress.com/2014/07/22/building-a-food-recommendation-engine-with-spark-mllib-and-play/

Setup
=====

You will need:

* Scala 2.10+ (sbt will install it automatically)
* Play Framework (sbt will install it automatically)
* MongoDB (install it manually)

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
Any stage could be interrupted due to unkonwn reason. Retry these commond until it success.
