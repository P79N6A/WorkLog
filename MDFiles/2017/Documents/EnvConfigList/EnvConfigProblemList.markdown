### 平行环境

#### 交易模块

##### 10.8.210.99服务器

* 该服务器上部署了mdfrontserver,mdpaygate,mdtradecenter，mdtask四个交易项目的核心模块。
* 2017-08-24：
    * 胡正newwap访问mdfrontserver返回null，0字节，经查mdfrontserver的logs目录下的visit目录（/data/application/mdfrontserver/logs/product/visit）中的日志能清晰看到返回参数为null,继续追查sevice目录（/data/application/mdfrontserver/logs/product/service）中的日志，看到zookeeper错误，亦即mdtradecenter相关dubbo接口不通，finduserrebatebyuserid不通，后查该虚拟机只有2g内存，mdtradecenter重启失败，待运维张永刚解决。此前也通过查/data/application/logs/mdfrontserver/access.log也能看到返回字节为0，该字段在状态码200后就是。


### 常规环境
### 开发联调环境