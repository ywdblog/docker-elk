### 服务信息

ELK全家桶

1：单节点es（9200），cerebro（9000），kibana（5601），都是7.3.0版本

2：安装 es hanlp 和 pinyin 插件

设置host：

```
主机IP  xwj-es-1.com
主机IP  xwj-es-2.com
主机IP  xwj-es-3.com
```

### 安装说明

```
docker-compose build
docker-compose up
docker-compose down
```

测试：

```
curl -XGET 'http://192.168.64.2:9200/_cluster/state?pretty'
curl -XGET 'http://192.168.64.2:9200/_cat/plugins' 
```

### 参考

- [Docker-Compose made Easy with Elasticsearch and Kibana](https://levelup.gitconnected.com/docker-compose-made-easy-with-elasticsearch-and-kibana-4cb4110a80dd)
- [docker cerebro](https://github.com/lmenezes/cerebro)
- [docker Kibana](https://www.elastic.co/guide/en/kibana/current/docker.html)
- [docker es 官方](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)
- [docker es 官方镜像说明](https://github.com/elastic/elasticsearch/blob/7.16/distribution/docker/docker-compose.yml)
- [docker es 官方镜像说明](https://www.docker.elastic.co/r/elasticsearch)
- [How to install ElasticSeach plugins using docker compose](https://stackoverflow.com/questions/39691652/how-to-install-elasticseach-plugins-using-docker-compose)