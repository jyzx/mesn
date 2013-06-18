mesn
====

附1：《广场链接调用系统界面-相关协议》

1. 调用系统浏览器
  链接href中会包含mesn#辨识字符串, type为link, url为网页地址；示例如下：
  <a href="mesn#type=link&url=http://www.google.com/">调用系统浏览器</a>

2. 在广场内直接加载网页
  链接href中仅包含url网页地址；示例如下：
  <a href="index.html">在广场内加载网页</a>

3. 点击显示个人资料
  链接href中会包含mesn#辨识字符串, type为user, id为该用户的uid, name为该用户姓名；示例如下：
  <a href="mesn#type=user&id=2649482&name=邢丹平">邢丹平</a>

4. 点击显示某一专区动态
  链接href中会包含mesn#辨识字符串, type为zone, id为该专区的fid, name为该专区名称；示例如下：
  <a href="mesn#type=zone&id=609&name=移动学习">移动学习专区</a>

5. 点击显示某一标签动态页
  链接href中会包含mesn#辨识字符串, type为tag, id传空, name为该标签名称；示例如下：
  <a href="mesn#type=tag&id=&name=标签名称">标签名称</a>

6. 点击进入发布界面
  链接href中会包含mesn#辨识字符串
  <a href="mesn#type=post

a) 自动补全@, #, 文字
  &pre={'pre': [{'type':'user', 'id':2649482, 'name':'邢丹平'},
   {'type':'zone', 'id':1910, "name":'创新之翼'}, 
   {'type':'tag', 'id':'', 'name':'去电信化大讨论'},
   {'type':'text', 'content':'我的想法是'}]}
pre进行URL编码

b) 自动设置专区及分类
  需传fid, fname, cid, cname；
  <a href="mesn#type=post&fid=609&fname=移动学习
  &cid=2&cname=网优>点击发布</a>
  若只指定了fid, fname 则等同从专区列表/专区view进入发布界面 自动发起分类查询请求

c) a+b情形
  由于在专区下 话题不支持@, # 故此时user, zone均应只作为普通文字传输



