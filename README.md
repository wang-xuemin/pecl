# PECL官网
http://pecl.php.net/package-stats.php
### amqp扩展依赖rabbitmq-c，需要先安装rabbitmq-c
```
MacOS安装
brew install rabbitmq-c
CentOS
yum install rabbitmq-c
Debian
apt install rabbitmq-c
FreeBSD
pkg install rabbitmq-c
```

### rdkafka扩展依赖librdkafka，需要先安装librdkafka
```
MacOS安装
brew install librdkafka
CentOS
yum install librdkafka
Debian
apt install librdkafka
FreeBSD
pkg install librdkafka
```
### PECL安装工具，命令行安装扩展
pecl install \<pakgname\>
```
pecl install redis
```
### PECL源码安装扩展
### php version >= 7.0 && version <= 7.999
```
1、解压扩展包
2、扩展php扩展模块，来生成编译检测脚本
phpize
3、执行configure，编译配置检测
./configure
4、执行make安装，编译并安装
make && make install
```
##### 生产环境不建议开启xdebug，消耗性能

#####  php.ini添加对应扩展
```
[yaf]
yaf.environ = product
yaf.library = NULL
yaf.cache_config = 0
yaf.name_suffix = 1
yaf.name_separator = ""
yaf.forward_limit = 5
yaf.use_namespace = 0
yaf.use_spl_autoload = 0
extension=yaf.so

[swoole]
extension=swoole.so

[rdkafka]
extension=rdkafka.so

[redis]
extension=redis.so

[memcached]
extension=memcached.so

[amqp]
extension=amqp.so

[mongodb]
extension=mongodb.so

[xdebug]
zend_extension=xdebug.so
xdebug.var_display_max_children = 10240
xdebug.var_display_max_data = 10240
xdebug.var_display_max_depth = 10240
;xdebug.auto_trace = on
;xdebug.collect_params = on
;xdebug.collect_return = on
;xdebug.trace_output_dir = "/Users/wangxuemin/nginx/xdebug"
;xdebug.remote_enable = on
;xdebug.profiler_enable = on
;xdebug.profiler_enable_trigger = on
;xdebug.profiler_output_name = cachegrind.out.%t.%p
;xdebug.profiler_output_dir = "/Users/wangxuemin/nginx/xdebug"

```
