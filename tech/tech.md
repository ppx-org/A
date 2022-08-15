
# 存储了一段时期内的测量序列
* 时间序列数据是随着时间收集的任何类型的数据，并由一个或多个不变参数唯一标识，
这些不变参数通常又称为是数据源的元数据

* 天气 温度 传感器标识，地理位置
作用: 提交了查询效率，减少了时序数据和次级索引(secondary index)的磁盘存储空间


```
{
  "metadata": {"sensorId": 5578, "type": "temperature"},
  "timestamp": ISODate("2021-05-19T16:00.00.000Z"),
  "temp":" 17
}


db.weather.findOne({
  "timestamp": ISODate("2021-05-19T16:00.00.000Z")
})

```
MongoDB将时间序列集合视为内部集合的可写非物化视图,
在插入时自动将时间序列数据组织成优化的存储格式。

*  TTL(Set up Automatic Removal )








 




