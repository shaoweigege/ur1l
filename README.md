# ur1l
A open short URL service.     
*in developing.*

-------------
### 一期开发已完工，待优化。
由于前期并发性能要求不大，暂且以php+Redis架构开发。   
以后可能会用JAVA+Redis（+MySQL）架构开发。

-----------
## 功能简介
### 本短网址服务用于应对以下问题：   
1.由于有时候需要和好友面对面分享一个url，但是苦于url太长（无法手动输入），或设备间进行一个简单的文本共享又太过于繁琐（使用即时通讯软件）。   
2.自己的网站，某些服务，生成的请求url太长（带了一大串get参数）——美观性差，邮件中包含长url容易被标记为垃圾邮件，等等——需要对url进行缩短。
3.……    

### 安全性：    
1.添加了单IP请求数限制，防止恶意请求。   
2.添加了Google recaptcha的人机验证，防止机器人请求。    

---------------
### API/config.php
此文件在项目中不可见。需要自行添加。。。

|--变量--|--说明--|
|--|--|
|$recaptcha_key|Google-recaptcha的服务器端token|   
|$min_score|人机验证的最小通过值（0-1）|   
|$redis_host|redis的ip|   
|$redis_port|redis的端口|   
|$base|生成hash字符取值|   

文档还待继续补充。。。
