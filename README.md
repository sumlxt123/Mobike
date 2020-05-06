## 数据集介绍

* 原数据集来自Udacity提供的摩拜单车上海城区2016年8月随机抽样百万条用户使用数据，共有102361条订单记录，包含起点、目的地、租赁时间、还车时间、用户ID、车辆ID、订单编号和路线轨迹信息。

* 经过清洗整理和信息提取后，新数据集增加了18个新变量，主要用于分析的变量为：total_time（骑行时长(min)）、distance（骑行始末点的直线距离(m)）、isweekend（工作日/非工作日）、ispeak（高峰时段/非高峰时段）、ring_stage（内环内/中环内/外环内/郊外）、rate（高价值用户/中等价值用户/低价值用户）这六个变量。

* 新数据集在使用过程中亦去除了少量骑行速度、距离、时长的异常记录，最终的订单记录数量为 102319 条。



## 分析结论

在数据探索过程中，发现工作日/非工作日、高峰时段/非高峰时段、骑行区域和用户价值这四个变量均会对骑行时长产生影响。当依次限定四个变量条件后，可以发现：

* 在骑行地理位置或用户价值条件相同的情况下，工作日/非工作日、高峰时段/非高峰时段对于平均骑行时长的规律明显，高峰时段和非工作日的平均骑行时长高于非高峰时段和工作日；
* 用户价值越高、平均骑行时长越长；
* 骑行区域越远离市中心、骑行时长越长，但用户价值对于骑行时长的影响远小于后者。

除分类变量对于骑行时长的影响之外，又有以下发现：

* 比较不同骑行区域和用户价值类型下，工作日和高峰时段的数据点分布特征高度类似，说明工作日和高峰时段的用车行为特征相似；
* 高价值用户更多地分布在内环范围内。

选择原因：
* 工作日/非工作日、高峰时段/非高峰时段相关的结论与实际运营过程中面对的消费行为有着高度相关性，对其分析可以更好的推出有吸引力的运营方案；
* 骑行区域、用户价值相关的结论可以指导运营时资源投放的重点，可以提高运营效率；


## 参考资料

https://blog.csdn.net/sinat_35930259/article/details/80002213
https://blog.csdn.net/weixin_42936350/article/details/104257417
https://blog.csdn.net/brucewong0516/article/details/81782312?depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1&utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1
https://www.cntofu.com/book/172/docs/35.md
https://lbs.amap.com/console/show/picker
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html
https://blog.csdn.net/blmoistawinde/article/details/85009603

