# ELKStack
###简介
本项目是基于 Docker 和 ELKStack 构建的一个日志收集、存储和分析平台。

将每台主机的应用日志和系统日志根据要求，输出到指定目录。我们用 Filebeat 监控日志文件的变化，并将最新的日志数据发送到 Logstash。由 Logstash 收集来自各个 Filebeat 的日志数据后（当然也可以通过 HTTP 接收日志数据），对数据进行加工（如过滤、清除、格式化等）处理后，将数据发送给 Elasticsearch。Elasticsearch 对数据进行存储和索引，并对外提供相应的查询等接口。Kibana 用于访问 Elasticsearch 的接口获取的日志数据，并可以以图表化的形式将日志数据展示出来。

###如何使用

项目的部署及使用方式见 [blog.smoker.cc](http://blog.smoker.cc/docker/20160325.html)
