# hello-hadoop
Initialization repo for assignment 2

## Blog post

+ [assignment 2 blogpost](PLACEHOLDER).

Remember to update this README file with a link to the published blog post when you are done!

## The assignment

First look at the assignment!
https://rubigdata.github.io/course/assignments/A2-mapreduce.html

Also read the [hadoop instructions](https://rubigdata.github.io/course/background/hadoop.html),
including how to move files between your desktop and the docker container.

## Helpful commands

Here is a number of commands from my commandline history:

    export PATH=${JAVA_HOME}/bin:${PATH}
    export HADOOP_CLASSPATH=${JAVA_HOME}/lib/tools.jar
    bin/hadoop com.sun.tools.javac.Main /mnt/bigdata/hello-hadoop/WordCount.java

    pushd /mnt/bigdata/hello-hadoop
    jar cf wc.jar WordCount*.class
    popd

    bin/hdfs dfs -mkdir /user/root/input
    bin/hdfs dfs -put /mnt/bigdata/100.txt.utf-8 input
    bin/hadoop jar /mnt/bigdata/hello-hadoop/wc.jar WordCount /user/root/input /user/root/output
    bin/hadoop fs -ls output


