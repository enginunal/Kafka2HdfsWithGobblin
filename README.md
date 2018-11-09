# Kafka2HdfsWithGobblin
Apache gobblin from kafka to hdfs ingestion sample.

Before you get started please read https://gobblin.readthedocs.io/en/latest/Getting-Started/ . 
I listed some important steps to build and run gobblin binaries.

1. Unpackage the gobblin tgz file.

```
tar -xvf apache-gobblin-incubating-sources-0.13.0.tgz
```

2. If not exists copy gradle-wrapper.jar(my repo contains this jar) into gradle/wrapper directory than build

```
./gradlew :gobblin-distribution:buildDistributionTar
```

3. Get a file named apache-gobblin-incubating-bin-0.13.0.tar.gz from build/gobblin-distribution/distributions/ directory and unpack it.

```
cp apache-gobblin-incubating-bin-0.13.0.tar.gz /home/you/gobblin/
cd /home/you/gobblin/
tar -xvf apache-gobblin-incubating-bin-0.13.0.tar.gz
```
4. cd to the unpacked Gobblin distribution bin directory and enter gobblin-env.sh file, add this line:

```
HADOOP_BIN_DIR=${HADOOP_HOME}/bin
```

5. Run gobblin-standalone.sh file with parameters like this.

```
/home/engin/gobblin/gobblin-dist/bin/gobblin-standalone.sh start --conf /home/engin/deneme.pull --workdir /home/engin/workdir
```

