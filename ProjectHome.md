<h1>Javascript/CSS 多文件代码合并、安全压缩、优化(PHP版)</h1>


.
现在大量网站为了追求用户体验，使用了大量使用CSS和JS文件。
而网页加载的时间大部分是消耗在资源请求部分。通过 Chrome自带调试工具，或者 Firebug 可观察到：
资源加载的等待时间经常占到总时间的 50%以上。
再比如，IE6默认只有2个下载线程！也就是说，同时只能进行2个资源请求、无论你网速有多快。
所以网页前端速度优化的一个重要项目就是：减小资源请求数。


---

事实上，业界有很有名气的js，css合并压缩开源程序：minify。
但悲剧的 minify 在 php5.3 , php 5.4 环境下无法使用，于是逼的我只好自己丰衣足食。

minify 比较重量级，很臃肿。它采用了将合并文件写入硬盘的方式。
本程序只是合并、压缩，直接讲合并结果发送客户端，并采用修改过期时间优化效率，最大限度减小服务器压力。
这样做法的效率就非常非常接近于 minify。

本程序碎玉压缩合并的功能俱全，但是整体及其轻量级，很容易更新、维护，二次开发。


### 本程序压缩后的大小大约为压缩前的 15% - 30% 左右（平均值）。推荐使用 YSlow 进行另外方面的优化。 ###


如果您在使用中，发现任何 Bug ，请给我反馈，谢谢。



&lt;hr&gt;



### 压缩前 ###
<img src='http://julying.com/lab/compress-js-css/images/fiddler_before.png'>


<h3>压缩后</h3>
<img src='http://julying.com/lab/compress-js-css/images/fiddler_after.png'>

<br>
<br>
<hr><br>
<br>
<br>
<br>
/<br>
<ul><li>Javascript 代码压缩<br>
</li><li>
</li><li>网址 : <a href='http://julying.com/lab/compress-js-css/'>http://julying.com/lab/compress-js-css/</a>
</li><li>类型： 原创脚本<br>
</li><li>作者： 王子墨<br>
</li><li>邮箱 : i@julying.com<br>
</li><li>发布 : 2012-06-10 22:28<br>
</li><li>更新 : 2012-07-22 12:50</li></ul>

<ul><li>版权所有 2012 | julying.com<br>
</li><li>此插件遵循 MIT、GPL2、GNU 许可.<br>
</li><li>版权:Copyright (c) julying 版权所有，本程序为开源程序(开放源代码)。<br>
</li><li><a href='http://julying.com/code/license/'>http://julying.com/code/license/</a>
</li><li>
</li><li>此程序会自动去除 注释，并且会对文件名进行安全检测、去重复、存在判定等操作，只允许 .js/.css 文件，并且不允许包含远程文件。<br>
</li><li><b></li><li>环境要求： >= PHP 5<br>
</li><li>
</li><li>压缩多个 js 方法：</li></ul></b>

<br>
<br>
<script type="text/javascript" src="http://julying.com/lab/compress-js-css/file=/lab/coffee/js/jQuery.js,/lab/coffee/js/jquery.coffee.js"><br>
<br>
<br>
<br>
</script><br>
<br>
<br>
<br>
<ul><li>
</li><li>压缩多个 CSS 方法：<br>
<br>
<br>
<link rel="stylesheet" media="all" href="http://julying.com/lab/compress-js-css/file=/lab/coffee/layerImages/layer.css,/lab/coffee/css/main.css" /><br>
<br>
</li></ul>

<b>/</b>



建议查看可看 <a href='http://developer.yahoo.com/performance/rules.html'>《Yahoo工程师的前端优化建议--英文原版》</a>.<br>
<br>
<br>
如果英文阅读不是很流畅，请查看翻译版本：<br>
《Yahoo工程师的前端优化建议-- 中文翻译版》<br>
<a href='http://translate.google.com.hk/translate?hl=zh-CN&sl=en&u=http://developer.yahoo.com/performance/rules.html/&prev=/search%3Fq%3Dhttp://developer.yahoo.com/performance/rules.html%26hl%3Dzh-CN%26newwindow%3D1%26safe%3Dstrict%26prmd%3Dimvns&sa=X&ei=i0gZULPVJcS3rAex_YCwDQ&ved=0CFcQ7gEwAA'>《Yahoo工程师的前端优化建议-- 中文翻译版》</a>