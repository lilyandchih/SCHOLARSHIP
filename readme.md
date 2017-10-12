# Mgit 服务端设计

标签（空格分隔）： 系统类图和序列图设计


----------


> 服务端功能

 1. 查看仓库分支信息
 2. 获取当前分支
 3. 查看commit log信息
 4. 文件或目录查看

    

> 服务端类图设计

![未命名文件 (6).png-124.6kB][1]
Service:主要负责对外提供服务
Repository:仓库的映射
ObjectDatabase:objects目录的映射
RefDatabase:refs目录的映射
CommitWalk:遍历Commit对象
TreeWalk:遍历Tree对象
RepositoryBuilder:负责构建仓库对象

> 服务端时序图设计

 - 查看分支操作
![commithttp (5).png-18.1kB][2]
 - 获取commit log操作
![commithttp (4).png-32.9kB][3]
 - 读取文件操作
![commithttp (6).png-41kB][4]

---


  [1]: http://static.zybuluo.com/ZF2016/ryzrtv7e8n6sipslns08am2b/%E6%9C%AA%E5%91%BD%E5%90%8D%E6%96%87%E4%BB%B6%20%286%29.png
  [2]: http://static.zybuluo.com/ZF2016/67cqqutobkulswbrvu3xh62f/commithttp%20%285%29.png
  [3]: http://static.zybuluo.com/ZF2016/t0by328day1056dcmaqyjqng/commithttp%20%284%29.png
  [4]: http://static.zybuluo.com/ZF2016/726wobqir8fkm97k3fak25v4/commithttp%20%286%29.png