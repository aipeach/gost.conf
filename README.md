# Gost 配置文件

## 服务端配置文件
### config-server.json
> https://github.com/aipeach/gost.conf/blob/main/config-server.json

## 客户端配置文件
### config-client-1.json
一个客户端对应一个服务端
> https://github.com/aipeach/gost.conf/blob/main/client/config-client-1.json

### config-client-2.json
一个客户端对应多个服务端
> https://github.com/aipeach/gost.conf/blob/main/client/config-client-2.json

### config-client-3.json
一个客户端对应多个服务端 **负载均衡**

> https://github.com/aipeach/gost.conf/blob/main/client/config-client-3.json
> https://github.com/aipeach/gost.conf/blob/main/client/peer.txt

参数说明:

`strategy` -  指定节点选择策略，`round` - 轮询，`random` - 随机, `fifo` - 自上而下。

`max_fails` -  指定节点连接的最大失败次数，当与一个节点建立连接失败次数超过此设定值时，此节点会被标记为死亡节点(Dead)，死亡节点不会被选择使用。默认值为1。

`fail_timeout` -  指定死亡节点的超时时间，当一个节点被标记为死亡节点后，在此设定的时间间隔内不会被选择使用，超过此设定时间间隔后，会再次参与节点选择。默认为30秒。

`reload` - 配置文件热更新。此选项用来指定文件检查周期,默认为10秒。

`peer` - 指定节点列表。
