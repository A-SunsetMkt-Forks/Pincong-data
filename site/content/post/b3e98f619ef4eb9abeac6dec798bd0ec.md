---
layout: default
Lastmod: 2020-06-17T09:42:08.212001+00:00
date: 2019-11-21T00:00:00.000Z
title: "我闲着没事爬了一下胡锡进的推特账号（更新3：胡总生活习惯讨论）"
author: "Anarch1st"
tags: [胡锡进,Twitter,社會工程]
---

对，我确实闲着没事。  
胡主编在twitter十分活跃，其实我没有关注他，但每天都能看到别人转发或者reply他的信息。我进去瞄了一眼他的账号，1500多tweet，于是我决定爬一爬分析一下图个乐呵。  
爬虫：tweepy  
目标账号：@HuXijin\_GT （胡锡进的英语twitter账号）  
爬取结果：1505条记录（去重后，共1496条tweet），时间跨度：2014-08-29 （胡主编twitter玩的挺早）到 2019-11-19  
  
结果和分析：  
  
**推特频率时间线（以月为单位）**  
![https://images.weserv.nl/?url=https://i.imgur.com/lIDsKGC.jpg](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FlIDsKGC.jpg)  
从上图中我们明显看到胡总编最近这段时间加强了外宣工作（嘻嘻）。x轴代表时间（月），y轴代表tweet数量。  
**  
情感分析（sentiment analysis）**  
**![https://images.weserv.nl/?url=https://i.imgur.com/qQ2Ik03.jpg](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FqQ2Ik03.jpg)**  
图1 表示胡主编所有tweet的情感分析，NEG=NEGATIVE 消极（负面）情感, POS=POSITIVE 积极（正面）情感。  
x轴有5个单位 None表示无情感，Slight表示有轻微情感，Moderate表示有中度情感，Strong表示有强烈情感，V.Strong表示有特别强烈的情感。y轴是tweets条目总数（因为一条tweet里面可能会包含既正面又负面的情感，e.g. I like apple but I hate banana. 所以所有的条目总数加起来一定大于collected dataset）。  
所以重点是从slight以后越来越强烈的情感，none的bar自动忽略。  
根据统计结果推测：胡主编在推特上面，总体而言负面情绪强烈压制正面情绪。（一点都不正能量）  
  
**六月以来的情感分析图**  
**![https://images.weserv.nl/?url=https://i.imgur.com/abNg6sT.jpg](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FabNg6sT.jpg)**  
图3很垃圾，但是我懒得把它弄好看点了  
x axis = date.  
y axis = value = sentiment score.  
这张图是胡主编2019年6月以来的sentiment line chart，亮点是在近半年的时间里面，胡主编的强烈positive tweet屈指可数 （value = 4）。自从六月以来，看来胡主编受了不少气吧。lol  
注：sentiment analysis based on SentiStrength (University of Wolverhampton)图3很垃圾，但是我懒得把它弄好看点了  
x axis = date.  
y axis = value = sentiment score.  
这张图是胡主编2019年6月以来的sentiment line chart，亮点是在近半年的时间里面，胡主编的强烈positive tweet屈指可数 （value = 4）。自从六月以来，看来胡主编受了不少气吧。lol  
注：sentiment analysis based on SentiStrength (University of Wolverhampton)  
  
**Word Cloud**  
![https://images.weserv.nl/?url=https://i.imgur.com/Iq9XlPW.jpg](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FIq9XlPW.jpg)  
图4是胡主编所有数据的图云。(大写的中国和中国人lol，和小写的川普和hk，哈哈哈哈)  
  
**在tweets中最常用的词**  
  
稍微清理一下数据之后，然后提取了一下词干，统计了一下胡主编所有tweet最常用的词（使用次数多余100次的）（图5）![https://images.weserv.nl/?url=https://i.imgur.com/o0mP6sR.jpg](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2Fo0mP6sR.jpg)  
presid = president/etc.., polit = politics/political, peopl = people, chines = chinese. beij = beijing.  
**  
Topic modeling (LDA)**  
  
这个内容主要指胡主编的所有tweet讨论的主题  
我共分成了5大主题  
  
![https://images.weserv.nl/?url=https://i.imgur.com/aEWO0y1.png](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FaEWO0y1.png)  
  
仁者见仁，智者见智吧。  
  
如果要是我说的话，胡总最爱讲的主题是：川普的政策，china no1，（批评）西方媒体对hk事件的宣传，和贸易战，关贸协定。  
  
**Sentiment analysis on Topics about HK**  
![https://images.weserv.nl/?url=https://i.imgur.com/OcVzrwX.jpg](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FOcVzrwX.jpg)  
  
在这个sentiment analysis中我没有继续用SentiStrength 而是换成了NRC lexicon (有时间再跑机器学习吧)  
  
但是胡主编你怎么这么多fear word啊? 你在害怕什么呀？  
  
能力有限，懒得写字，看图说话吧。  
（结果是只用了半天时间瞎撸出来的，很原始，仅供参考。）  
  
\------------------------------------------update-----------------------------------------  
  
有朋友问我说胡总最喜欢的发推时间  
  
我使用了网站：https://accountanalysis.app 来看了一眼胡总编的时间热点图  
  
![https://images.weserv.nl/?url=https://i.imgur.com/QyZX9e7.png](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FQyZX9e7.png)  
由图可见，胡锡近最喜欢的发推时间是19点左右，周二与周四13点发的也不少。  
但是本图显示的是西欧时间（GMT+1），如果换成北京时间的话。胡飞盘最喜欢的发推时间应该是北京时间凌晨1点左右（胡总真的很勤劳啊，大半夜不睡觉也要外宣）  
  
并且有一点结论可以从本图看到，胡总偏爱在工作日的业余时间发推。  
双休日他的发推频率不高，工作日的工作时间也没有业余时间高（毕竟还要写长文痛斥自由民主呢）。所以胡总无论是工作中还是业余生活上都是一个极其忠心的飞盘党党魁。  
  
还有一个结论可以得出来：21：00-02：00的胡总基本不发推，他的作息时间比较规律，北京时间是凌晨3点到早上8点左右，扣去洗漱时间和早上吃早餐的时间，胡总每天的平均睡眠时间大概在4-5小时之后。看来叼飞盘也是一项体力活啊。  
  
**\---------------------------------------------------------------update2-----------------------------------------------------**  
  
**胡总的生活习惯**  
  
我又深挖了一下胡总的数据。  
  
下图是胡总所有tweet用过的设备  
![https://images.weserv.nl/?url=https://i.imgur.com/fXHO7Q9.png](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FfXHO7Q9.png)  
  
我们来看看里面具体有什么，如果我过滤一下数据，只是网页端推特的话，那么胡总的tweet热点图是下面这样的  
胡总用网页端发推的时间基本都是在工作时间，有两点时间可以确定，  
1 胡总的电脑里肯定装了vpn，或者说，环球时报内部有vpn。  
2  胡总的工作时间大概是北京时间中午12点到晚上23点左右。  
![https://images.weserv.nl/?url=https://i.imgur.com/aQsciu0.png](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FaQsciu0.png)  
  
如果我们比较一下ios 和 安卓的发推时间线，我们可以得到另外两个结论  
  
下图是推特iphone客户端发推时间线  
![https://images.weserv.nl/?url=https://i.imgur.com/aGM3Ais.png](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FaGM3Ais.png)  
  
  
下图是安卓twitter客户端发推时间线  
![https://images.weserv.nl/?url=https://i.imgur.com/Rot9ejy.png](https://images.weserv.nl/?url=https%3A%2F%2Fi.imgur.com%2FRot9ejy.png)  
  
通过这两张图的对比，我们可以发现胡总似乎在五月中下旬（大概在5.20）左右换了手机，从iphone 换成了 安卓机。也有可能他有两部手机，不过iphone的vpn不好用了换成安卓了也有可能，但是我更偏向前一种说法，因为5月份的时候正是贸易战打得正火热的时候。美国商业部在5月份把华为加入了实体清单。  
也就是说，胡总很有可能因为爱党之心，在当时抛弃了iphone换成了华为的安卓机。  
（言行合一的胡总编）

            
### 品葱用户 **Anarch1st 
孫笑川秘書** 评论于 2019-11-22
        
> 這種分析只能做玩具吧，在實業界用得多嗎，真的有用嗎？

  
  
这种分析主要提供给商业公司（e.g. 大家在网上对某新产品怎么看啊之类的，或者大家对某个政党怎么看啊）确实有使用的，具体数量我不知道。  
还有我只是自己闲着没事给自己找点事情做，我的水平肯定比不上专业的商业化公司，只是业余时间玩一玩。
        


            
### 品葱用户 **Anarch1st 
kcyx2184** 评论于 2019-11-22
        
> 2017-6到2018-5中間是發生了甚麼嗎？

  
  
如果你仔细观察的话，2017-6到2017-12之间是没有tweet发出的，具体是2017.12-2018.5之间爆炸，这段时间里面有几个事件发生，比如比如包皇终身制，金和川普的会面新闻etc
        


            
### 品葱用户 **巴斯克维尔柴犬** 评论于 2019-11-22
        
给老哥这种技术帖子点赞，胡主编把正能量留在墙内，负能量当然要留给这些境外反动势力啊
        


            
### 品葱用户 **Anarch1st 
electron8964** 评论于 2019-11-22
        
> 胡编每天发推的时间是什么时候呢？

  
我抽空update一下
        


            
### 品葱用户 **华国锋 
孫笑川秘書** 评论于 2019-11-22
        
> 這種分析只能做玩具吧，在實業界用得多嗎，真的有用嗎？

  
  
其他人介绍了主要用途，我来说一下技术的优势。  
  
假如人工阅读一千条推，并加以记录和分类，假设处理一条需要两分钟，那么单是录入就需要16.7小时，也就是两天的工作量。假如月薪四千，这就是四百块钱。  
  
而当数据量增大到千倍万倍，人工支出会按比例增加，但机器处理时间近似相等。这样就是节省百万千万的支出了。  
  
这就是技术的优势。
        


            
### 品葱用户 **勃列日涅夫** 评论于 2019-11-23
        
iPhone换华为的时候他还发了个微博
        


            
### 品葱用户 **Anarch1st 
孫笑川秘書** 评论于 2019-11-21
        
> Sentiment analysis 這個功能準確度如何？

  
  
sentiment analysis 有不同的approach，比如lexicon或者machine learning  
在我手上这个只是用的lexicon approach，如果是机器学习的话，准度会更高。  
但是也分软件或者词库的质量，我觉得我使用的准度还可以。
        


            
### 品葱用户 **Anarch1st 
孫笑川秘書** 评论于 2019-11-22
        
> 如果這種很準的話，就厲害了

  
要相信科技发展的力量，用客观和科技的手段揭开共产党的罪恶面纱。
        


            
### 品葱用户 **孫笑川秘書 
Anarch1st** 评论于 2019-11-22
        
> 要相信科技发展的力量，用客观和科技的手段揭开共产党的罪恶面纱。

  
關心技術在商業中的運用，中共的罪惡，地球上50%的人都知道。
        


            
### 品葱用户 **Anarch1st 
巴斯克维尔柴犬** 评论于 2019-11-21
        
> 给老哥这种技术帖子点赞，胡主编把正能量留在墙内，负能量当然要留给这些境外反动势力啊

  
  
胡主编文化战狼
        


            
### 品葱用户 **electron8964** 评论于 2019-11-21
        
胡编每天发推的时间是什么时候呢？
        


            
### 品葱用户 **kcyx2184** 评论于 2019-11-22
        
2017-6到2018-5中間是發生了甚麼嗎？
        


            
### 品葱用户 **Password** 评论于 2020-04-11
        
太棒了！ 美国很多ngo在social media上做counter terrorism 的项目把恐怖组织用来招募年轻人的账号和关联账号做数据分析，分享在kaggle等开源数据分享网站上。  
楼主很有心啊。应该可以machine learning帮忙detect大外宣还有分析他们的话术用于以后counter ccp propoganda。利国利民  
亲自给你点赞👍
        


            
### 品葱用户 **叼盘侠 
巴斯克维尔柴犬** 评论于 2020-05-12
        
[

> 给老哥这种技术帖子点赞，胡主编把正能量留在墙内，负能量当然要留给这些境外反动势力啊

](https://pincong.rocks/article/item_id-125461# "https://pincong.rocks/article/item_id-125461#")  
俺老胡覺得還是很佩服的，居然算出了俺從iphone換成華為手機的時間節點。神機妙算。
        


            
### 品葱用户 **孫笑川秘書 
Anarch1st** 评论于 2019-11-22
        
> 这种分析主要提供给商业公司（e.g. 大家在网上对某新产品怎么看啊之类的，或者大家对某个政党怎么看啊...

  
Sentiment analysis 這個功能準確度如何？
        


            
### 品葱用户 **孫笑川秘書 
Anarch1st** 评论于 2019-11-22
        
> sentiment analysis 有不同的approach，比如lexicon或者machine...

  
如果這種很準的話，就厲害了
        


            
### 品葱用户 **魔幻社会主义** 评论于 2019-11-21
        
~已删除~
        


            
### 品葱用户 **荆棘之心** 评论于 2019-11-22
        
太强了。
        


            
### 品葱用户 **balibali** 评论于 2019-11-22
        
這個數據有意思，謝謝您的分享！  
這個胡，整天以為自己是代表中共發聲的，很喜歡扮演“中鍋民主派人物”的角色，他是自封的口交部長嗎？  
為撒他都可以隨便上推，而絕大多數中國人都不可以？shame！
        


            
### 品葱用户 **Anarch1st 
balibali** 评论于 2019-11-23
        
> 這個數據有意思，謝謝您的分享！這個胡，整天以為自己是代表中共發聲的，很喜歡扮演“民主人物”的角色，他...

  
  
对 你说的没错 口交部长是要有特权的。
        


            
### 品葱用户 **Anarch1st 
balibali** 评论于 2019-11-22
        
> 這個數據有意思，謝謝您的分享！這個胡，整天以為自己是代表中共發聲的，很喜歡扮演“中鍋民主派人物”的角...

  
你看我新更新的内容 口交部长也很累的
        


            
### 品葱用户 **sundayinvited** 评论于 2019-11-23
        
满篇China will, China can  
  
典型的情绪化、主观化，言之无物。不仅如此，俨然以China自居，仿佛“吾便国家”。小人得志。
        


            
### 品葱用户 **Anarch1st 
sundayinvited** 评论于 2019-11-22
        
> 满篇China will, China can典型的情绪化、主观化，言之无物。不仅如此，俨然以Chi...

  
你说的没错 飞盘党妄图代表国家，座等一个正义的铁锤。
        


            
### 品葱用户 **Anarch1st 
勃列日涅夫** 评论于 2019-11-23
        
> iPhone换华为的时候他还发了个微博

  
对 我似乎有印象。。但是刚才没想起来。
        


            
### 品葱用户 **清茶i** 评论于 2019-12-07
        
在国内使用安卓机有种被随时监控的感觉
        


            
### 品葱用户 **Anarch1st 
清茶i** 评论于 2019-12-11
        
> 在国内使用安卓机有种被随时监控的感觉

  
确实。我反正是不敢用安卓。而且各种被装插件。
        


            
### 品葱用户 **AAPLTSLA** 评论于 2020-02-19
        
看你topic modeling里面的截图，应该是用的R吧。那就比较依赖于package开发者的语言分析水平了。
        


            
### 品葱用户 **琉璃光 
华国锋** 评论于 2020-02-19
        
> 其他人介绍了主要用途，我来说一下技术的优势。假如人工阅读一千条推，并加以记录和分类，假设处理一条需要...

  
人做人事，機做機事（以前是牲做牲事）。人爭不過機械式重複，機械也做不到舉一反三、把握靈機。叫人做機械，是以人為物。
        


            
### 品葱用户 **konami** 评论于 2020-02-19
        
不可能是胡自己寫的吧，多半有員工幫他發推。可見老胡你的公司多麼血汗，小編經常忙到半夜。
        


            
### 品葱用户 **愿黄老爷早日体面** 评论于 2020-02-19
        
社工好可怕
        


            
### 品葱用户 **明泽女帝千古** 评论于 2020-02-20
        
我一直觉得胡主编与那些只想赚五毛糊口的庸人不同，果然，人家是个真正有理想的人，就像戈培尔一样。
        


            
### 品葱用户 **遠古邪惡水楓** 评论于 2020-02-19
        
可以试试用LDAvis包对topic modelling的结果做一下可视化
        


            
### 品葱用户 **HoKaiChina** 评论于 2020-02-19
        
数据可视化是一个系统工程，你单一做一个图做不到多种图交互性强基本卖不了钱的。也就图个洗乐，不过这种已经成熟快七八年了，市场也没得做了。
        


            
### 品葱用户 **门门 
Anarch1st** 评论于 2020-02-19
        
> 要相信科技发展的力量，用客观和科技的手段揭开共产党的罪恶面纱。

  
其实使用最多的恰恰就是中共。
        


            
### 品葱用户 **Anarch1st 
Password** 评论于 2020-05-31
        
[

> 太棒了！ 美国很多ngo在social media上做counter terrorism 的项目把恐...

]( "/article/item_id-340667#")  
  
谢谢你的夸奖，不过这个帖子里面我这就是一拍脑门随便瞎分析了一下。有机会的话我希望做一个小粉红话术分析。
        


            
### 品葱用户 **孫笑川秘書** 评论于 2019-11-21
        
這種分析只能做玩具吧，在實業界用得多嗎，真的有用嗎？
        


            
### 品葱用户 **Anarch1st 
遠古邪惡水楓** 评论于 2020-05-31
        
~已删除~
        






> [点击品葱原文参与讨论](https://pincong.rocks/article/id-9105__sort_key-agree_count__sort-DESC)

