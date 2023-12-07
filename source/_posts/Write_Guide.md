---
title: 博客写作指南
date: 2023-10-24 00:00:00
categories: Guide
tags:
- Build
- 2023
---

## 注意
本指南仅适用于 GDG Zhengzhou 官方博客的更新写作，博客基于 Hexo 搭建，并使用了 Icarus 作为主题。

## 文章结构
文章主要由两部分组成，即 Front-matter 和正文部分，其中 Front-matter 主要用于文章标题、书写日期、类型、摘要、标签等的声明，正文部分为文章主体部分。

<!-- more -->

## Front-matter

**Front-matter** 是指每篇 Hexo 博客内MD格式文档头部的一串配置代码，他以`---`开头、结尾。

### 日常文章
一篇典型的日常文章 Front-matter 如下：
```Markdown
---
title: 文章标题
date: 2018-06-06 17:32:11
description: 文章摘要
categories: 文章分类
tags:
  - 标签1
  - 标签2
---
```
上述片段中涉及的 Hexo Front-matter 具体有以下用途:
代码 | 用途
---- | ---
title | 文章标题
date | 编写时间（如不声明，可自动生成）
description | 文章摘要，作用于主页与RSS
categories | 文章分类，含此配置会被"分类"页面收录至相关分类，每篇文章仅允许一个分类
tags | 文章标签，含此配置会被"标签"页面收录至相关分类，每篇文章允许多个标签

### 内部文章
内部文章用于满足志愿者工作、活动策划及实施等特定场景下的需求，通常会被隐藏并加密，一个典型的内部文章 Front-matter 如下：
```Markdown
---
title: 文章标题
date: 1970-01-01 00:00:00
sage: true
password: 文章密码
abstract: 提示信息
message: 提示信息
---
```
上述片段中涉及的 Hexo Front-matter 具体有以下用途:
代码 | 用途
---- | ---
title | 文章标题
date | 编写时间（请不要修改日期，固定填写为 1970-01-01 00:00:00）
sage | 是否隐藏文章
password | 文章的密码
abstract | 密码提示信息
message | 密码提示信息

## 正文书写
正文部分的书写为严格匹配的 Markdown 格式，其基本语法如下：
```Markdown
# 一级标题
## 二级标题
### 三级标题
#### 四级标题

- 无序列表1
- 无序列表2
- 无序列表3

1. 有序列表1
2. 有序列表2
3. 有序列表3

![图片](http://图片地址 "图片描述")

[链接](http://链接地址 "悬停显示")

> 引用

`文本高亮`

**文本加粗**

*斜体*

~~删除线~~
```
更多更详细的语法说明请参见 [Markdown 基本语法](https://github.com/younghz/Markdown)

## 文稿书写&发布101

1. 创建本地文件，命名为XXX.md，XXX必须为英文，除了较为广泛使用的缩写(WTM etc.)，尽量使用全拼，如有多个单词，请使用`_`作为连接符号，避免使用空格或其他符号。
2. 根据文章的性质(日常文章/内部文章)，复制相应的 `Front-matter` 到 md 文件头部。
3. 严格遵守 Markdown 语法，完成正文部分的书写并保存。
4. 上传文件至 GitHub 项目的 `\source\_posts` 处，完成发布。

 **注意** 
- 上传文件可以使用 Github 网页拖拽、Git 提交等方法完成，不限方法，选择你喜欢的即可。
- 文件上传后，需要等待45秒左右，等待 CI 完成编译方会在博客内看到新文章，编译时间最长不超过2分钟，如果长时间没有看到更新，请联系 [技术支持](mailto:icemberry@gmail.com)

