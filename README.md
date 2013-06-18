mesn
====

《广场链接调用系统界面-相关协议》

<ol>
  <li><strong>调用系统浏览器</strong> <br />
    链接href中会包含mesn#辨识字符串, type为link,  url为网页地址；示例如下： <br />
    &lt;a href=&quot;mesn#type=link&amp;url=<a href="http://www.google.com/">http://www.google.com/</a>&quot;&gt;调用系统浏览器&lt;/a&gt; <br /><br /></li>
  <li><strong> 在广场内直接加载网页</strong> <br />
    链接href中仅包含url网页地址；示例如下： <br />
    &lt;a href=&quot;index.html&quot;&gt;在广场内加载网页&lt;/a&gt; <br /><br /></li>
  <li><strong>点击显示个人资料</strong> <br />
    链接href中会包含mesn#辨识字符串, type为user,  id为该用户的uid, name为该用户姓名；示例如下： <br />
    &lt;a  href=&quot;mesn#type=user&amp;id=2649482&amp;name=邢丹平&quot;&gt;邢丹平&lt;/a&gt; <br /><br /></li>
  <li><strong> 点击显示某一专区动态</strong> <br />
    链接href中会包含mesn#辨识字符串, type为zone,  id为该专区的fid, name为该专区名称；示例如下： <br />
    &lt;a  href=&quot;mesn#type=zone&amp;id=609&amp;name=移动学习&quot;&gt;移动学习专区&lt;/a&gt; <br /><br /></li>
  <li><strong> 点击显示某一标签动态页</strong> <br />
    链接href中会包含mesn#辨识字符串, type为tag,  id传空, name为该标签名称；示例如下： <br />
    &lt;a  href=&quot;mesn#type=tag&amp;id=&amp;name=标签名称&quot;&gt;标签名称&lt;/a&gt; <br /><br /></li>
  <li><strong>点击进入发布界面</strong> <br />
    链接href中会包含mesn#辨识字符串 <br />
  &lt;a href=&quot;mesn#type=post <br /><br />
  <ul type="disc">
    <li> 自动补全@, #, 文字 <br />
      &amp;pre={'pre': [{'type':'user',  'id':2649482, 'name':'邢丹平'}, <br />
      {'type':'zone', 'id':1910,  &quot;name&quot;:'创新之翼'},&nbsp; <br />
      {'type':'tag', 'id':'', 'name':'去电信化大讨论'}, <br />
      {'type':'text', 'content':'我的想法是'}]} <br />
      <strong>pre进行URL编码</strong> <br /><br /></li>
    <li>自动设置专区及分类 <br />
      需传fid,  fname, cid, cname； <br />
      &lt;a  href=&quot;mesn#type=post&amp;fid=609&amp;fname=移动学习&amp;cid=2&amp;cname=网优&gt;点击发布&lt;/a&gt; <br />
      若只指定了fid, fname  则等同从专区列表/专区view进入发布界面  自动发起分类查询请求 <br /><br /></li>
    <li> a+b情形 <br />
      由于在专区下 话题不支持@, # 故此时user, zone均应只作为普通文字传输 <br /><br /></li>
  </ul>
   </li>
</ol>

