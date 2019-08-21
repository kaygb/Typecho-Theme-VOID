# Typecho Theme VOID 3.2.0

> ✏ 一款简洁优雅的 Typecho 主题

作为计算机术语时，VOID 的意思是「无类型」。

![](https://raw.githubusercontent.com/AlanDecode/Typecho-Theme-VOID/master/screenshot.png)

[![build status](https://img.shields.io/travis/AlanDecode/Typecho-Theme-VOID/source.svg?style=flat-square)](https://travis-ci.org/AlanDecode/Typecho-Theme-VOID) [![downloads](https://img.shields.io/github/downloads/AlanDecode/Typecho-Theme-VOID/total.svg?style=flat-square)](https://github.com/AlanDecode/Typecho-Theme-VOID/releases) [![](https://img.shields.io/github/release/AlanDecode/Typecho-Theme-VOID.svg?style=flat-square)](https://github.com/AlanDecode/Typecho-Theme-VOID/releases) ![](https://img.shields.io/github/license/AlanDecode/Typecho-Theme-VOID.svg?style=flat-square)

## 特性

> 演示站点：[熊猫小A的博客](https://blog.imalan.cn)，介绍文章：[VOID：现在可以公开的情报](https://blog.imalan.cn/archives/247/)。

* 响应式设计
* PJAX 无刷新体验
* AJAX 评论
* 前台管理评论（删除、待审、标为垃圾）
* 前台无跳转登陆（兼容 PJAX）
* 自动夜间模式
* 优秀的可读性
* 衬线、非衬线两种文字风格
* 代码高亮（浅色暗色两种风格，随主题切换）
* 站点样式设置面板（日夜转换、字体、字号）
* Mac 风格代码块（可开启或关闭）
* 代码行号（可分别针对桌面或移动端设置开启或关闭）
* MathJax 公式
* 表情解析（文章、评论可用）
* 图片排版（可用作相册）
* 灵活的头图设置
* 文章目录解析
* 完整的结构化数据支持
* 够用的后台设置与丰富的高级设置

结合附带的配套专用插件，还有更多功能：

* 浏览量统计
* 文章点赞
* 文章字数统计

以及其他很多细节，总之用起来还算舒服。我建立了一个示例页面，在这里你可以看到 VOID 对常用写作元素的支持以及一些特色功能演示：[示例页面](https://blog.imalan.cn/archives/194/)。

## 开始使用

1. 下载主题：[发布版](https://github.com/AlanDecode/Typecho-Theme-VOID/releases)
2. 解压
3. 将**主题文件夹下**的 VOID 文件夹上传至站点 /usr/themes 目录下
4. 后台启用主题
5. 将**配套插件文件夹下**的 VOID 文件夹上传至站点 /usr/plugins 目录下
6. 后台启用插件

* 可选：将主题 `assets` 文件夹下的 `VOIDCacheRule.js` 复制一份到站点根目录，并在主题设置中启用 Service Worker 缓存。
* 可选：主题文件夹下 advanceSetting.sample.json 中有一些高级设置，可以看看。

开发版主题可以在这里获取：[开发版](https://github.com/AlanDecode/Typecho-Theme-VOID/archive/nightly.zip)。注意，不保证开发版有更新更多的功能。而且开发版变动频繁，若无必要请使用发布版主题。

## **常见问题（请务必仔细阅读）**

<details><summary>如何开启文章点赞？</summa修复错误的 `<br>` 标签高度
* 其它细节调整

文章点赞功能依赖配套插件，请上传至插件目录并启用。插件一般会随主题包发布，开发版主题请前往 https://github.com/AlanDecode/VOID-Plugin 获取。

</details>

<details><summary>如何开启文章浏览量统计？</summary><br>

文章浏览量统计功能依赖配套插件，请上传至插件目录并启用。插件一般会随主题包发布，开发版主题请前往 https://github.com/AlanDecode/VOID-Plugin 获取。

</details>

<details><summary>如何开启文章字数统计？</summary><br>

文章字数统计功能依赖配套插件，请上传至插件目录并启用。插件一般会随主题包发布，开发版主题请前往 https://github.com/AlanDecode/VOID-Plugin 获取。

</details>

<details><summary>下载安装后样式不对？</summary><br>

仓库中的是未压缩的源代码，包含大量实际使用中不需要的文件，并且可能无法直接使用。请一定通过这两个链接下载主题：[发布版](https://github.com/AlanDecode/Typecho-Theme-VOID/releases) | [开发版](https://github.com/AlanDecode/Typecho-Theme-VOID/archive/nightly.zip)

</details>

<details><summary>添加归档页面</summary><br>

新建独立页面，自定义模板选择 `Archives`，内容留空。

</details>

<details><summary>添加友情链接</summary><br>

新建独立页面，然后如此书写：

```
[links]
[熊猫小A](https://www.imalan.cn)+(https://secure.gravatar.com/avatar/1741a6eef5c824899e347e4afcbaa75d?s=200&r=G&d=)
[熊猫小A的博客](https://blog.imalan.cn)+(https://secure.gravatar.com/avatar/1741a6eef5c824899e347e4afcbaa75d?s=64&r=G&d=)
[/links]
```

文章中、独立页面中都可以通过该语法插入类似的展示块。在某些 Typecho 版本中 HTML 会被转义后输出，请使用 `!!!` 包裹以上代码，例如：

```
!!!
[links]
···
[/links]
!!!
```

`!!!` 需要单独占一行。

</details>

<details><summary>图片排版</summary><br>

在文章中，使用 `[photos][/photos]` 包起来的图片可显示在同一行。例如：

```
[photos]
![](https://cdn.imalan.cn/img/post/2018-10-26/IMG_0073.jpeg)
![](https://cdn.imalan.cn/img/post/2018-10-26/IMG_0053.jpeg)
[/photos]

[photos]
![](https://cdn.imalan.cn/img/post/2018-10-26/IMG_0039.jpeg)
![](https://cdn.imalan.cn/img/post/2018-10-26/IMG_0051.jpeg)
![](https://cdn.imalan.cn/img/post/2018-10-26/IMG_0005.jpeg)
[/photos]
```

在某些 Typecho 版本中 HTML 会被转义后输出，请使用 `!!!` 包裹以上代码，例如：

```
!!!
[photos]
···
[/photos]
!!!
```

`!!!` 需要单独占一行。

</details>

<details><summary>增强的 Markdown 语法</summary><br>

* 注音语法：`{{文本:zhu yin}}`，会渲染为：<ruby>文本<rp> (</rp><rt>zhu yin</rt><rp>)</rp></ruby>
* notice 提示块：`[notice]提示内容[/notice]`

</details>

<details><summary>页面空白</summary><br>

* 首先检查是否有插件重复引入了 JQuery，若有，在插件设置页面关闭。
* 另外，推荐使用 PHP 7.0 及以上版本搭配 MySQL 数据库。PHP 5.6 或者更低版本可能出现未知问题（并且我不会去修复）。

</details>

## 更新

同[开始使用](#开始使用)，区别是你可以直接覆盖主题文件，不禁用主题，这样你的主题设置就不会丢失。

## 开发与自定义

**首先注意：我不保证提供任何自定义修改相关的指导与帮助。You are on your own.**

<details><summary>展开详情</summary><br>

如果你有不错的想法，可以定制自己的版本。首先你需要准备好 NodeJS 环境，然后 clone 这个 repo：

```bash
git clone https://github.com/AlanDecode/Typecho-Theme-VOID ./VOID && cd ./VOID
```

安装依赖：

```bash
npm install -g gulp
npm install
```

用以下命令打包依赖的 JS 和 CSS：

```bash
gulp dev
```

主题的样式是用 SCSS 写的，你可以使用自己喜欢的方式编译 SCSS，或者使用：

```bash
gulp sass
```

监听 SCSS 更改然后实时编译。尽请添加自己想要的功能，满意后就提交代码。然后：

```bash
gulp build
```

构建你的主题，生成的主题位于 `./build` 目录下。如果你对自己的更改很满意，**欢迎提出 Pull Request**。

</details>

## 更新日志

**🍰 2019-08-21 Version 3.2.0**

* 新增：首页可设置为单栏模式
* 新增：在受支持的浏览器中导航栏采用毛玻璃效果
* 新增：[高级设置]分别针对移动端与桌面端设置导航栏模式
* 新增：[高级设置]是否解析图题
* 优化：添加 apple-mobile-web-app 支持
* 优化：图片灯箱中可显示图题
* 优化：友链页面排版
* 修复：分类页面下文章列表样式与设置不一致
* 修复：错误的结构化数据
* 修复：图片灯箱开关导致页面抖动
* 修复：修复错误的 `<br>` 标签高度
* 其它细节调整

注意，3.2.0 版本主题依赖 1.00 及以上版本插件。若之前已经成功安装启用插件（1.00 版）则不用处理，若之前安装插件出现问题可以尝试使用新版（1.01）插件。

从 2.2 版本起，主题部分功能需要配套插件支持，例如文章点赞、浏览量统计、字数统计等。**请先卸载**原来的 Likes、TePostViews 插件，否则数据会出现错误！TePostViews 插件卸载前请设置为**卸载后保留数据**，以防丢失浏览数据。

更多：[change-log.md](https://github.com/AlanDecode/Typecho-Theme-VOID/blob/master/change-log.md)

## 鸣谢

### 开源项目

[JQuery](https://github.com/jquery/jquery) | [HighlightJS](https://highlightjs.org/) | [MathJax](https://www.mathjax.org/) | [fancyBox](http://fancyapps.com/fancybox/3/) | [bigfoot.js](http://www.bigfootjs.com/) | [OwO](https://github.com/DIYgod/OwO) | [pjax](https://github.com/defunkt/jquery-pjax) | [yue.css](https://github.com/lepture/yue.css) | [tocbot](https://tscanlin.github.io/tocbot/) | [pangu.js](https://github.com/vinta/pangu.js) | [social](https://github.com/lepture/social) | [Headroom.js](http://wicky.nillia.ms/headroom.js/) | [jquery.scrollTo](https://github.com/flesler/jquery.scrollTo) | [hypher](https://github.com/bramstein/hypher)

### 其他

[RAW](https://github.com/AlanDecode/Typecho-Theme-RAW) | [Mirages](https://get233.com/archives/mirages-intro.html) | [handsome](https://www.ihewro.com/archives/489/) | [Card](https://blog.shuiba.co/bitcron-theme-card) | [Casper](https://github.com/TryGhost/Casper) | [Typlog](https://typlog.com/)

## 捐助

**如果本项目对你有所帮助，请考虑捐助我**

![谢谢支持](https://wx1.sinaimg.cn/large/0060lm7Tly1g0c4cbi71lj30sc0iv453.jpg)

## License

MIT © [AlanDecode](https://github.com/AlanDecode)