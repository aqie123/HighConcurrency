高并发解决方案：
	前段资源cdn处理
	应用集群部署
	大的应用拆分为小的应用
	应用缓存redis等
	搜索引擎使用solr等
	数据库分库分表
	swoole+redis+nginx
	cdn+静态化+redis+go改造的http请求服务（异步请求数据），嵌套在nginx中的反向代理中。这里网络swoole的PHP第三方扩展异步开发请求
	数据库优化好
	使用缓存
	服务器性能好
	只是http应用的话，减少io，尽可能减少io，所有高并发方案都是为了这个目的
	1.Webserver (Nginx) 静态资源地址单独部署
	2.PHP处理节点
	3.高速缓存：用的memcached
	4.中间件
	5.架构还可以选择性地使用队列 beantalkd，Redis
	6.LVS+PHP集群
	7.memcache集群缓存，key-value高性能存储，异步队列任务系统