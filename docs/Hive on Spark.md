## Hive 默认以 MapReduce 执行
```
hive > set hive.execution.engine;
hive.execution.engine=mr
```

## Hive
```
$ wget http://apache.fayea.com/hive/hive-2.0.0/apache-hive-2.0.0-bin.tar.gz
$ tar -xzvf apache-hive-2.0.0-bin.tar.gz
$ mv apache-hive-2.0.0-bin /opt/
$ cd /opt/
$ ln -s apache-hive-2.0.0-bin hive
```

## 参考文献
* [Spark 实战，第 1 部分: 使用 Scala 语言开发 Spark 应用程序](https://www.ibm.com/developerworks/cn/opensource/os-cn-spark-practice1/)
