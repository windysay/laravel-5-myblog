###myBlog
自己为了熟悉laravel框架练手的一个博客，同时也是自己多年的愿望，一个自己写的博客，代码全部开源

博客地址：[叶落山城秋](http://iphpt.com)

博客前端页面是从 [kieran](https://github.com/SuperKieran/TKL) 处扒取修改所得，后端页面是从 源码之家 处下载所得，逻辑代码全部自己所写

######博客功能
* 目前只有文章的一些操作，分类的一些操作，标签的一些操作，还有系统设置与友链设置
* redis缓存
* 添加了任务调度,每次收集用户的IP等信息,然后利用队列在每天晚上12点进行插入数据库操作,然后如果发生错误,自动发送错误到我的邮件里

######预加
* 看是否能将及时评论同步到微信(还没碰过微信),若不行，试试封装个简单APP(朋友推荐，本人还没接触过，想尝试)

###安装
> git clone https://github.com/Yela528/laravel-5-myblog

> composer install

> 自行添加.env 文件

> .env 里 `CACHE_DRIVER` 换成 `redis`

> `php artisan key:generate`

> 数据迁移 `php artisan migrate`

<span style='color:yellow'>如果安装发现有包问题,请查看当前文件下的`api.md`文件,因为有时候会突然安装点扩展,直接把该文件里的命令一行一行的执行就行了</span>

这个博客是我没事自己对laravel框架里一些知识的探索，代码写的不是很严谨，有问题欢迎指导，也希望大牛能给我指引一下路

如果有其他问题，可以联系我QQ *2067930913*,如果原意，还可以加群[440221268](http://jq.qq.com/?_wv=1027&k=2CTYswa)一起探讨也行哦。。






#### 以下是之前开发进程

- ~~之前的iphpt，本来后台都写好了很多功能，因为不小心格了系统，数据库和原文件都没了，只剩下github上的代码了，遂，再写个玩玩吧~~

- 2016年08月02日 第一次上传代码，完成laravel 安装
- 2016年08月03日 做好数据库迁移,建立文章列表页面
- 2016年08月04日 写完文章列表页,建了文章,标签,分类的M
- 2016年08月08日 分类列表页, 分类修改页,返回提示包下载
- 2016年08月10日 写完文章相应的功能,修改后台样式(真坑啊！)
- 2016年08月13日 前台大部分功能完成,只剩评论功能
- 2016年08月23日 加了队列,异步同步到数据库,如果有错误,利用邮件系统发送邮件到我自己邮箱
- 2016年08月24日 文章添加修改加入自动推送到百度收录
- 2016年09月12日 修复后台文章编辑器的自带上传图片功能bug,现已可以上传插图

#####<a href="http://www.iphpt.com" target='_blank'>博客网址</a>



- 2016年08月11日 后台效果图 ![分类页面](http://obq9881x1.bkt.clouddn.com/%E5%88%86%E7%B1%BB%E9%A1%B5%E9%9D%A2.png)
- 后台文章的页面：![后台文章页面](http://obq9881x1.bkt.clouddn.com/%E5%90%8E%E5%8F%B0%E6%96%87%E7%AB%A0%E9%A1%B5%E9%9D%A2.png)