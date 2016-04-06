## 版本
* [spark-1.6.1](http://apache.01link.hk/spark/spark-1.6.1/spark-1.6.1-bin-hadoop2.6.tgz)

## 下载安装 Spark
```
$ wget http://apache.01link.hk/spark/spark-1.6.1/spark-1.6.1-bin-hadoop2.6.tgz
$ tar -xzvf spark-1.6.1-bin-hadoop2.6.tgz
$ ln -s /opt/spark-1.6.1-bin-hadoop2.6 spark
```

## python 交互模式
```
$ /opt/spark/bin/pyspark

>>>

# 版本
>>> sc.version

# 应用名字
>>> sc.appName
```

## 分析 nginx access log
* 在交互模式下输入，创建一个 RDD，textFile 会按行读入一个文件，这种方式读入的文件，不会随文件的更新数据进行更新。第二篇将进行脚本的编写和使用 Stream 进行实时数据的统计。
```
>>> log=sc.textFile('/var/log/nginx/access.log');
>>> log.count(); # 统计行数
>>> log.first(); # 返回第一行
>>> log.filter(lambda line: "200" != line.split('|')[4]).count()
```


## 参考文献
* [Spark入门学习(一) 分析nginx log文件](http://www.tuicool.com/articles/BNVjArm)
