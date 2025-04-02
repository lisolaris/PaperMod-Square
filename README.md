<h1 align=center>Hugo PaperMod-Square</h1>

这是我对原版[PaperMod](https://github.com/adityatelange/hugo-PaperMod)主题的一个fork，依我个人喜好对主题做了一些修改：

+ 将文字部分宽度从原先的720px更改为1024px，与菜单栏齐平；
+ 首页的`<title>`标签变更为`站点标题 - 站点子标题`的格式，如下：

![首页标题](https://z4a.net/images/2025/03/19/QQ20250319012713.png#center)

并在`config.yaml`中加入配置参数`params.subtitleForAllPages`，设置为`true`时可使站点内的所有文章页面标题变为`文章标题 | 站点标题 - 站点子标题`的格式，设置为`false`时只显示`文章标题 | 站点标题`的格式：

![文章标题](https://z4a.net/images/2025/03/19/QQ20250319012750.png)

+ 添加额外的css，使得以Markdown语法编排的表格自动居中而不是默认的左对齐：

![表格居中](https://z4a.net/images/2025/03/19/QQ20250319013725.png)

+ 删除默认的代码块黑色背景并禁用自带代码块高亮方法，引入外部`highlight.js`并支持随主题切换更改代码高亮主题，参见主仓库中的`layouts\partials\extend_head.html`（同时还需要修改`config.yaml`禁用自带代码高亮如下）：

```yaml
markup:
  highlight:
    codeFences: false
    guessSyntax: false
    noClasses: false

params:
  useExternalHLJS: true # 自定的启用外部highlight.js标记

  assets:
    disableHLJS: true
```

名字中的Square表示这是PaperModMod，即$\rm{Paper\ {Mod}^{2}}$ （逃
