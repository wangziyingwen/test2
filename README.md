### 项目说明 ###
* 利用github action实现定时自动运行api调用，保持E5开发活跃。
* 免费，不需要额外设备/服务器，部署完不用管啦。

### 特别说明/Thanks ###
* 原教程博主-黑幕（酷安id-Paran）：https://blog.432100.xyz/index.php/archives/50/
* 本项目地址：https://github.com/wangziyingwen/Autoapi-test

--------------------------------------------------------------

### 步骤 ###
* 登录/注册一个github账号，新建一个repository/项目
  ![image](https://github.com/wangziyingwen/Autoapi-test/blob/master/images/新建仓库.png)

* 下载本项目文件里的1.py , 根据原文教程修改1.py、1.txt ，上传并复制代码地址

  ![image](https://github.com/wangziyingwen/Autoapi-test/blob/master/images/代码地址.png)
  
* 点击右上角fork本项目的代码到到你自己的仓库（相当于新建repository并复制本项目代码），

  ![image](https://github.com/wangziyingwen/Autoapi-test/blob/master/images/fork.png)
  
  然后修改文件 .github\workflows\autoapi.yml 中的代码地址为你自己的地址
  
  ![image](https://github.com/wangziyingwen/Autoapi-test/blob/master/images/修改地方.png)
  
* 搞定，接下来就不用管了。我设定的每12小时自动运行一次，每次调用3轮（点击右上角星星/star也可以立马调用一次），你们自行斟酌修改（我也不知道活跃要调用多少、多久）：

   · 定时自动启动修改地方：（在autoapi.yml里，自行百度cron定时任务格式）
   
   ![image](https://github.com/wangziyingwen/Autoapi-test/blob/master/images/定时.png)
   
   · 每次轮数修改地方：（在1.py最后面）
   
   ![image](https://github.com/wangziyingwen/Autoapi-test/blob/master/images/次数.png)
   
   · 点击上面的Action就能看到每次的运行日志（都看下，api有没有调用到位）
   
   ![image](https://github.com/wangziyingwen/Autoapi-test/blob/master/images/日志.png)

------------------------------------------------------------
### 题外话 ###
> Api调用
  你们可以自己去graph浏览器看一下，学着自己修改要调用什么api(最重要的是调用outlook、onedrive)
  https://developer.microsoft.com/zh-CN/graph/graph-explorer/preview

### GithubAction介绍 ###
提供的虚拟环境：

· 2-core CPU
· 7 GB RAM 内存
· 14 GB SSD 硬盘空间

使用限制：
* 每个仓库只能同时支持20个 workflow 并行。
* 每小时可以调用1000次 GitHub API 。
* 每个 job 最多可以执行6个小时。
* 免费版的用户最大支持20个 job 并发执行，macOS 最大只支持5个。
* 私有仓库每月累计使用时间为2000分钟，超过后$ 0.008/分钟，公共仓库则无限制。

（我们这里用的公共仓库，按理，你们可以设定无限循环调用，然后6小时启动一次，保证24小时全天候调用）

### 最后 ###
  教程很直白了，应该都会弄吧。有空更新一下怎样网页获取refresh_token（不再需要rclone？）！所以不用电脑应该可以都搞定！

  我是代码小白，我实在不会把两个项目合并啊，只能分开弄两个项目，一个原代码，一个action流程，请各位多多包涵。有没有大佬能修改一下代码呀，十分欢迎！
  
  这个项目都是我根据以往看过的代码整合的，ORZ。
  
  有修改建议可以发邮件给我:
  wz.lxh@outlook.com
  
  基安id-卷腿毛菌
