title: 多说评论框集成到HEXO
categories: [Technology, Hexo]
tags: [hexo, 中文]

---
Hexo是使用node.js技术开发的一个纯静态博客系统，Hexo默认使用的评论插件是Disqus，为了方便广大国内用户使用多说来替换Disqus，特推出此教程。使用步骤如下：

在_config.yml中添加多说的配置：

  duoshuo_shortname: 你站点的short_name
修改themes\landscape\layout\_partial\article.ejs模板

把
``` javascript
  <% if (!index && post.comments && config.disqus_shortname){ %>
  <section id="comments">
    <div id="disqus_thread">
      <noscript>Please enable JavaScript to view the <a href="//disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
    </div>
  </section>
  <% } %>
```

改为
![ScreenShot](\2015\04\duoshuo\duoshuo.JPG)

http://dev.duoshuo.com/threads/541d3b2b40b5abcd2e4df0e9