# mqtt 对接遥测塔示例

本示例主要演示从 mqtt 订阅消息，并将传感器上报的遥测数据经过数据转化后，写到遥测塔实时数据库中进行存储。

具体可以参见文档[esp8266接入遥测塔.md](https://github.com/telemetrytower/iot-demos/blob/main/esp8266%E6%8E%A5%E5%85%A5%E9%81%A5%E6%B5%8B%E5%A1%94/%E6%8E%A5%E5%85%A5%E6%96%87%E6%A1%A3.md)

## 代码运行

- 修改以下代码，替换为自己的 emqx broker 和账号信息：

```
opts.AddBroker("emqx.broker.host")
opts.SetUsername("emqx.user.name")
opts.SetPassword("emqx.user.password")
```

- 运行代码：

```
go run mqttclient.go
```