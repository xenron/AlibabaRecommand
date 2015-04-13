##版本

##更改
筛选条件：look_times + store_times + cart_times <= 7 and buy_times==0 and int(lru) <= 21 and buy_flag == False
这样31天购买的不删除，作为前30天的label。但数据只从1540213 增加到 1540295。31th可以作为label的数据是990+82=1072个。

原因是：user_look user_store user_cart user_buy采用左连接，有一部分人没有look，store，cart，buy就已经买了。

筛选过的数据已经放入了feature.txt，但还没有导入pure_data数据库。

用之前的pure_data数据库，先测试特征工程。

扩张到19D特征
