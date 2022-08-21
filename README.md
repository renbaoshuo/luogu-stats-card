# Luogu Stats Card

> 注意：为了不滥用洛谷服务器流量，本项目将缓存 12 小时用户数据，即同一个用户卡片 **24 小时内最多只会向洛谷服务器请求 2 次数据**，并且只有在用户访问卡片时才会请求数据。

本项目原作者为 [wao3](https://github.com/wao3)，此 fork 对其进行了一些修改并部署到了 `luogu.api.baoshuo.dev` 上。

## 简介

`luogu-stats-card`是一个动态生成洛谷用户练习数据卡片的工具，可以展示自己的做题情况。可以用于个人主页、博客、github 等可以插入图片的地方。

## 效果预览

![宝硕的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214)

![宝硕的咕值情况](https://luogu.api.baoshuo.dev/guzhi?id=168214&scores=100,52,13,87,20)

_注：本估值信息仅作展示使用，不代表本人真实情况。_

## 如何使用

### 练习情况

练习情况可以自动获取用户的数据，但是前提是没有开启“完全隐私保护”，具体使用方法如下：

1. Markdown：复制以下内容到任意 markdown 编辑器中，并将`?id=`后面的数字更改为自己的 id 即可（id 是洛谷个人主页地址的一串数字）。

   ```markdown
   ![我的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214)
   ```

2. HTML：复制以下内容到 HTML 代码中，并将`?id=`后面的数字更改为自己的 id 即可（id 是洛谷个人主页地址的一串数字）。

   ```html
   <img alt="我的练习情况" src="https://luogu.api.baoshuo.dev/practice?id=168214">
   ```

### 咕值信息

咕值信息无法自动获取数据，如果需要必须要提供 cookie ，但是 这种方法十分不安全，并且不方便，所以获取咕值卡片需要手动输入咕值信息，具体使用方法如下。

复制以下内容到任意 markdown 编辑器中，并将 `?id=` 后面的数字更改为自己的 id，将 `scores=` 后面更换为自己的咕值信息，一共 5 个数字，用逗号分隔。

1. Markdown：复制以下内容到任意 markdown 编辑器中，并将 `?id=`后面的数字更改为自己的 id，将`scores=`后面更换为自己的咕值信息，一共 5 个数字，用逗号分隔。

   ```markdown
   ![我的咕值信息](https://luogu.api.baoshuo.dev/guzhi?id=168214&scores=100,65,45,15,0)
   ```

2. HTML：复制以下内容到 HTML 代码中，并将 `?id=`后面的数字更改为自己的 id，将`scores=`后面更换为自己的咕值信息，一共 5 个数字，用逗号分隔。

   ```html
   <img alt="我的练习情况" src="https://luogu.api.baoshuo.dev/practice?id=168214">
   ```

### 自定义选项

使用卡片时，支持设定自定义效果选项，可以组合使用。

1. **隐藏标题**，只需在链接最后带上`&hide_title=true`即可，例如：

   ```markdown
   ![宝硕的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214&hide_title=true)
   ```

   效果：

   ![宝硕的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214&hide_title=1)

2. **黑暗模式**，只需在链接最后带上`&dark_mode=true`即可，例如：

   ```markdown
   ![宝硕的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214&dark_mode=true)
   ```

   效果：

   ![宝硕的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214&dark_mode=1)
3. **自定义宽度**，默认 500，限制宽度在 500 到 1920 之间，只需在链接最后带上`&card_width=需要的宽度`即可，例如：

   ```markdown
   ![宝硕的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214&card_width=750)
   ```

   效果：

   ![宝硕的练习情况](https://luogu.api.baoshuo.dev/practice?id=168214&card_width=750)
