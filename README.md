# pecl
php version >= 7.0

##### 解压扩张包

##### 扩展php扩展模块
phpize

##### 执行
./configure

##### 执行 make安装
make && make install

#####  php.ini添加对应扩展

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

[xdebug]  
zend_extension=xdebug.so

[redis]  
extension=redis.so

[mongodb]  
extension=mongodb.so

[memcached]  
extension=memcached.so

[amqp]  
extension=amqp.so
