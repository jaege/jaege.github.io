---
layout: post
title: 新年第一天
---

新年第一天，尝试使用 [Jekyll](http://jekyllrb.com) 和 [GitHub Pages](https://pages.github.com) 搭个静态网站。目前基本框架已经差不多了，剩下的细节慢慢完善。

计划增加的功能：

- 归档汇总页 `archive.html`
- 标签汇总页 `tags.html`
- 分类汇总页 `categories.html`
- DISQUS 留言托管模板（`_include`）
- 简历页
- RSS/Atom 订阅页
- Google Analytics 统计模板（`<head>`， `_include`）
- 为 SEO 添加 `sitemap.xml`
- 申请自定义域名

最后试试代码高亮，和图片显示的小功能：

```cpp
#include <iostream>

int main() {
  std::cout << "Happy Chinese new year!" << std::endl;
}
```
不居中用 Markdown 语法：

![Happy Chinese new year]({{ site.url | append: site.baseurl }}/public/images/2016-monkey.jpg)

居中还是得用 `<img>` 标签：

<div align="center"><img alt="Happy Chinese new year" src="{{ site.url | append: site.baseurl }}/public/images/2016-monkey.jpg" /></div>
