# 公共接口文档

* url: 服务器申请后提供


### 城市列表（有PM2.5数据的城市）
| 地址 | url/api/cities|
| -- | -- |
| 方法 | GET |
| 参数 | 无 |
| 返回 | cities: 值是一个数组 |
|成功返回示例|{"cities":["鹤岗","鹰潭","黄冈",...,"齐齐哈尔","龙岩"]}|

---

### 一个城市的监测点列表
| 地址 | url/api/station_names |
| -- | -- |
| 方法 | GET |
| 参数 | city |
| 返回 |  city <br>  stations: 值是一个数组，里面的一个数组又包含了station_name和station_code  |
| 成功返回示例 | {"city":"北京","stations":[{"station_name":"万寿西宫","station_code":"1001A"},{"station_name":"定陵","station_code":"1002A"},{"station_name":"东四","station_code":"1003A"},{"station_name":"天坛","station_code":"1004A"},{"station_name":"农展馆","station_code":"1005A"},{"station_name":"官园","station_code":"1006A"},{"station_name":"海淀区万柳","station_code":"1007A"},{"station_name":"顺义新城","station_code":"1008A"},{"station_name":"怀柔镇","station_code":"1009A"},{"station_name":"昌平镇","station_code":"1010A"},{"station_name":"奥体中心","station_code":"1011A"},{"station_name":"古城","station_code":"1012A"}]}|

---

### 获取一个城市所有检测点的PM2.5数据
| 地址 | url/api/pm2_5 |
| -- | -- |
| 方法 | GET |
| 参数 | city：城市名称，必选参数<br> avg：是否返回一个城市所有监测点数据均值的标识，可选参数，默认是true，不需要均值时传这个参数并设置为false <br> stations：是否只返回一个城市均值的标识，可选参数，默认是yes，不需要监测点信息时传这个参数并设置为no |
| 返回 | 一个数组，每一项是一个监测点的数据 |
| 成功返回示例 | 暂无 |

---

### 获取一个检测点详细数据
| 地址 | url/api/all_by_station |
| -- | -- |
| 方法 | GET |
| 参数 | station_code |
| 返回 | 一个数组，包含所有指标数据 |
| 成功返回示例 | 暂无 |




