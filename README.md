zuulService 暂时没有使用集群
如果要使用集群，那么需要在zuul前面增加一个nginx，客户端请求到nginx 后， 通过nginx 在负载到多个zuulService上面。就可以做到集群了。
配置文件需要修改的eureka 的集群地址
springAdminService的地址
还有具体的路由指向
另外这个项目需要配置ribbon 和 zuul的超时时间，否则在其他微服务出现的超时的时候会出现zuulservice readtime
单独设置其他微服务的超时，不设置这个项目的也不行,所以我2个都设置了  