## 和聚宝后台工程概览(非业务模块)

该工程采用spring cloud框架进行开发，总共包含13个功能模块，具体如下：

### hjb-register-center (port:8761)

服务注册中心，治理所有后台服务，是所有后台服务的大管家。通过认证之后登录注册中心，可以看到所有注册的服务，点击服务则可以连接到该服务的接口文档页面。

### hjb-service-gateway (port:8711)

服务网关，所有对外暴露的服务，其访问路径都要先经过服务网关，类似后台服务的防火墙。

### hjb-common

工程通用组件。

### hjb-service-api

服务接口定义，供服务提供方实现该接口，供服务消费者调用该接口。

### hjb-config-server

配置中心服务

### spring-admin-server

SpringCloud微服务监控模块，在待监控项目中如下配置即可：

```
info:
   version: @project.version@
endpoints:
   sensitive: false
spring: 
   boot:
      admin:
         url: http://localhost:8080  #spring-admin-server访问地址
```
## 和聚宝后台工程(业务模块)

### hjb-user-center
用户服务

### hjb-asset-service
资产服务

### hjb-risk-service

风险模块

### hjb-prod-service
产品模块
 
### hjb-clear-service
清算模块

### bank-trans
银行优选业务服务
 
### bank-trans-asyn
银行优选异步业务服务

### hjb-h5-channel
H5渠道服务

### hjb-manage-channel
管理台服务

### bank-bosc-adapter
上海银行服务
 
### hjb-hb-adapter
和包服务