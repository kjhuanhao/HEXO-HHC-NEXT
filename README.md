# 前言

本教程来自[NexT官网](http://theme-next.iissnan.com/)

二次开发者：[HuanHaoCode](https://www.huanhao.xyz/)

在 Hexo 中有两份主要的配置文件，其名称都是 `_config.yml`。 其中，一份位于站点根目录下，主要包含 Hexo 本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。

为了描述方便，在以下说明中，将前者称为 **站点配置文件**， 后者称为 **主题配置文件**。

## HEXO-HHC-NEXT亮点

此主题为NexT的二次开发，为新手提供便利

此主题已经按照官网文档的基础上，全部配置完毕，因为已经基础功能已经全部开启，所以只需要阅读本文档即可知道如何去关闭一些功能，以及开启或更改一些功能。

## 安装 NexT

Hexo 安装主题的方式非常简单，只需要将主题文件拷贝至站点目录的 `themes` 目录下， 然后修改下配置文件即可。具体到 NexT 来说，安装步骤如下：

### 下载主题

如果你熟悉 [Git](http://git-scm.com/)， 建议你使用 克隆最新版本 的方式

在终端窗口下，定位到 Hexo 站点目录下。使用 `Git` checkout 代码：

```
git clone  https://github.com/kjhuanhao/HEXO-HHC-NEXT themes/next
```

***

### 启用主题

与所有 Hexo 主题启用的模式一样。 当 克隆/下载 完成后，打开 **站点配置文件**， 找到 `theme` 字段，并将其值更改为 `next`。

启用 NexT 主题

```
theme: HEXO-HHC-NEXT
```

到此，HEXO-HHC-NexT 主题安装完成。下一步我们将验证主题是否正确启用。在切换主题之后、验证之前， 我们最好使用 `hexo clean` 来清除 Hexo 的缓存。

***

### 验证主题

首先启动 Hexo 本地站点，并开启调试模式（即加上 `--debug`），整个命令是 `hexo s --debug`。 在服务启动的过程，注意观察命令行输出是否有任何异常信息，如果你碰到问题，这些信息将帮助他人更好的定位错误。 当命令行输出中提示出：

```
INFO  Hexo is running at http://0.0.0.0:4000/. Press Ctrl+C to stop.
```

此时即可使用浏览器访问 `http://localhost:4000`，检查站点是否正确运行。

当你看到站点的外观与下图所示类似时即说明你已成功安装 HHC-NexT 主题。这是 HHC-NexT 默认的主题样式

![](https://hbimg.huabanimg.com/2d99344b7772486b458d9db00b27b4d15fad0002bd90c-xOF6rz_fw658)



现在，你已经成功安装并启用了 NexT 主题。下一步我们将要更改一些主题的设定，包括个性化以及集成第三方服务。

## 主题设定

### 选择 Scheme

Scheme 是 NexT 提供的一种特性，借助于 Scheme，NexT 为你提供多种不同的外观。同时，几乎所有的配置都可以 在 Scheme 之间共用。目前 NexT 支持三种 Scheme，他们是：

- Muse - 默认 Scheme，这是 NexT 最初的版本，黑白主调，大量留白
- Mist - Muse 的紧凑版本，整洁有序的单栏外观
- Pisces - 双栏 Scheme，小家碧玉似的清新

Scheme 的切换通过更改 **主题配置文件**，搜索 scheme 关键字。 你会看到有三行 scheme 的配置，将你需用启用的 scheme 前面注释 `#` 去除即可。

选择 Pisces Scheme

```
#scheme: Muse
#scheme: Mist
scheme: Pisces
```

> 在HHC-NEXT中已经为你开启Pisces，您无需再次配置或您可以尝试其他样式

***

### 设置 语言

编辑 **站点配置文件**， 将 `language` 设置成你所需要的语言。建议明确设置你所需要的语言，例如选用简体中文，配置如下：

```
language: zh-Hans
```

目前 NexT 支持的语言如以下表格所示：

| 语言         | 代码                 | 设定示例                            |
| :----------- | :------------------- | :---------------------------------- |
| English      | `en`                 | `language: en`                      |
| 简体中文     | `zh-Hans`            | `language: zh-Hans`                 |
| Français     | `fr-FR`              | `language: fr-FR`                   |
| Português    | `pt`                 | `language: pt` or `language: pt-BR` |
| 繁體中文     | `zh-hk` 或者 `zh-tw` | `language: zh-hk`                   |
| Русский язык | `ru`                 | `language: ru`                      |
| Deutsch      | `de`                 | `language: de`                      |
| 日本語       | `ja`                 | `language: ja`                      |
| Indonesian   | `id`                 | `language: id`                      |
| Korean       | `ko`                 | `language: ko`                      |

> 本主题默认中文，您可以无需修改或者修改其他语言

***

### 设置 菜单

菜单配置包括三个部分，第一是菜单项（名称和链接），第二是菜单项的显示文本，第三是菜单项对应的图标。 NexT 使用的是 [Font Awesome](http://fontawesome.io/) 提供的图标， Font Awesome 提供了 600+ 的图标，可以满足绝大的多数的场景，同时无须担心在 Retina 屏幕下 图标模糊的问题。

编辑 **主题配置文件**，修改以下内容：

* 设定菜单内容，对应的字段是 `菜单设置`。 菜单内容的设置格式是：`item name: link`。其中 `item name `是一个名称，这个名称并不直接显示在页面上，她将用于匹配图标以及翻译。

菜单示例配置

```
menu:
  home: /
  archives: /archives
  #about: /about
  #categories: /categories
  tags: /tags
  #commonweal: /404.html
```

> 若你的站点运行在子目录中，请将链接前缀的 `/` 去掉（建议不要修改站点运行目录）

NexT 默认的菜单项有（标注  的项表示需要手动创建这个页面）：

| 键值       | 设定值                    | 显示文本（简体中文） |
| :--------- | :------------------------ | :------------------- |
| home       | `home: /`                 | 主页                 |
| archives   | `archives: /archives`     | 归档页               |
| categories | `categories: /categories` | 分类页               |
| tags       | `tags: /tags`             | 标签页               |
| about      | `about: /about`           | 关于页面             |
| commonweal | `commonweal: /404.html`   | 公益 404             |

***

* 设置菜单项的显示文本。在第一步中设置的菜单的名称并不直接用于界面上的展示。Hexo 在生成的时候将使用 这个名称查找对应的语言翻译，并提取显示文本。这些翻译文本放置在 NexT 主题目录下的 `languages/{language}.yml`（`{language}` 为你所使用的语言）。

  以简体中文为例，若你需要添加一个菜单项，比如 `something`。那么就需要修改简体中文对应的翻译文件`languages/zh-Hans.yml`，在 `menu` 字段下添加一项：

  ```
  menu:
    home: 首页
    archives: 归档
    categories: 分类
    tags: 标签
    about: 关于
    search: 搜索
    commonweal: 公益404
    something: 有料
  ```

设定菜单项的图标，对应的字段是 `menu_icons`。 此设定格式是 `item name: icon name`，其中 `item name` 与上一步所配置的菜单名字对应，`icon name` 是 Font Awesome 图标的 名字。而 `enable` 可用于控制是否显示图标，你可以设置成 `false` 来去掉图标。

***

* 菜单图标配置示例

```
menu_icons:
  enable: true
  # Icon Mapping.
  home: home
  about: user
  categories: th
  tags: tags
  archives: archive
  commonweal: heartbeat
```

> 在菜单图标开启的情况下，如果菜单项与菜单未匹配（没有设置或者无效的 Font Awesome 图标名字） 的情况下，NexT 将会使用  作为图标。
>
> 请注意键值（如 `home`）的大小写要严格匹配
>
> 设置菜单部分只是告诉您如何添加您想要的页面，如果没有需求可以跳过

***

### 设置 侧栏

默认情况下，侧栏仅在文章页面（拥有目录列表）时才显示，并放置于右侧位置。 可以通过修改 **主题配置文件** 中的 `侧栏设置` 字段来控制侧栏的行为。侧栏的设置包括两个部分，其一是侧栏的位置， 其二是侧栏显示的时机。

1. 设置侧栏的位置，修改 `sidebar.position` 的值，支持的选项有：

   - left - 靠左放置
   - right - 靠右放置

   ```
   sidebar:
     position: left
   ```

2. 设置侧栏显示的时机，修改 `sidebar.display` 的值，支持的选项有：

   - `post` - 默认行为，在文章页面（拥有目录列表）时显示
   - `always` - 在所有页面中都显示
   - `hide` - 在所有页面中都隐藏（可以手动展开）
   - `remove` - 完全移除

   ```
   sidebar:
     display: post
   ```

   ***

   ### 设置 头像

   编辑 **主题配置文件**， 修改字段 `头像设置`， 值设置成头像的链接地址。其中，头像的链接地址可以是：

   | 地址             | 值                                                           |
   | :--------------- | :----------------------------------------------------------- |
   | 完整的互联网 URI | `http://example.com/avatar.png`                              |
   | 站点内的地址     | 将头像放置主题目录下的 `source/uploads/` （新建 uploads 目录若不存在）  配置为：`avatar: /uploads/avatar.png`或者 放置在 `source/images/` 目录下  配置为：`avatar: /images/avatar.png` |

   头像设置示例

   ```
   avatar: 这里放你的头像地址
   ```

> 主题默认是我自己的头像，请自行更改

***

### 设置 作者昵称

编辑 **站点配置文件**， 设置 `author` 为你的昵称。

### 站点描述

编辑 **站点配置文件**， 设置 `description` 字段为你的站点描述。站点描述可以是你喜欢的一句签名:)

***

### 百度统计

注意： baidu_analytics 不是你的百度 id 或者 百度统计 id

1. 登录 [百度统计](http://tongji.baidu.com/)， 定位到站点的代码获取页面

2. 复制 `hm.js?` 后面那串统计脚本 id，如：

   ![](https://hbimg.huabanimg.com/3dd22872919bbe242052fbd415f530dd30dbf8513f6a-nLgydi_fw658)

​    3.编辑 **主题配置文件**， 修改字段 `baidu_analytics` 字段，值设置成你的百度统计脚本 id。

***

### 设置 RSS

NexT 中 RSS 有三个设置选项，满足特定的使用场景。 更改 **主题配置文件**，设定 `rss` 字段的值：

- `false`：禁用 RSS，不在页面上显示 RSS 连接。
- 留空：使用 Hexo 生成的 Feed 链接。 你可以需要先安装 [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed) 插件。
- 具体的链接地址：适用于已经烧制过 Feed 的情形。

***

### 设置代码高亮主题

NexT 使用 [Tomorrow Theme](https://github.com/chriskempson/tomorrow-theme) 作为代码高亮，共有5款主题供你选择。 NexT 默认使用的是 白色的 `normal` 主题，可选的值有 `normal`，`night`， `night blue`， `night bright`， `night eighties`：

| ![img](http://theme-next.iissnan.com/assets/img/tomorrow.png) | ![img](http://theme-next.iissnan.com/assets/img/tomorrow-night.png) | ![img](http://theme-next.iissnan.com/assets/img/tomorrow-night-blue.png) | ![img](http://theme-next.iissnan.com/assets/img/tomorrow-night-bright.png) | ![img](http://theme-next.iissnan.com/assets/img/tomorrow-night-eighties.png) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |

更改 `代码高亮` 字段，将其值设定成你所喜爱的高亮主题，例如：

高亮主题设置示例

```
# Code Highlight theme
# Available value: normal | night | night eighties | night blue | night bright
# https://github.com/chriskempson/tomorrow-theme
highlight_theme: night bright
```

> 本主题默认使用night bright

***

### 侧边栏社交链接

侧栏社交链接的修改包含两个部分，第一是链接，第二是链接图标。 两者配置均在 **主题配置文件** 中。

1. 链接放置在 `侧边社交设置` 字段下，一行一个链接。其键值格式是 `显示文本: 链接地址`。

   配置示例

   ```
   # Social links
   social:
     GitHub: https://github.com/your-user-name   ||这里放你的图标名称，具体看下面
     Twitter: https://twitter.com/your-user-name
     微博: http://weibo.com/your-user-name
     豆瓣: http://douban.com/people/your-user-name
     知乎: http://www.zhihu.com/people/your-user-name
     # 等等
   ```

2. 设定链接的图标，对应的字段是 `social_icons`。其键值格式是 `匹配键: Font Awesome 图标名称`， `匹配键` 与上一步所配置的链接的 `显示文本` 相同（大小写严格匹配），`图标名称` 是 Font Awesome 图标的名字（不必带 `fa-` 前缀）。`enable` 选项用于控制是否显示图标，你可以设置成 `false` 来去掉图标。

   配置示例

   ```
   # Social Icons
   social_icons:
     enable: true
     # Icon Mappings
     GitHub: github
     Twitter: twitter
     微博: weibo
   ```

***

### 开启打赏功能 由 [habren](https://github.com/iissnan/hexo-theme-next/pull/687) 贡献

越来越多的平台（微信公众平台，新浪微博，简书，百度打赏等）支持打赏功能，付费阅读时代越来越近，特此增加了打赏功能，支持微信打赏和支付宝打赏。 只需要 **主题配置文件** 中填入 微信 和 支付宝 收款二维码图片地址 即可开启该功能。

打赏功能配置示例

请在**主题配置文件中的**`打赏设置`处设置

```
reward_comment: 坚持原创技术分享，您的支持将鼓励我继续创作！
wechatpay: 微信付款图片地址
alipay: 微信付款图片地址
```

***

### 友情链接 由 [iamwent](https://github.com/iissnan/hexo-theme-next/pull/250) 贡献

编辑 **主题配置文件** 添加：

友情链接配置示例

```
links:
  MacTalk: http://macshuo.com/
  Title: http://example.com/
  名称:网址
```

***

### 腾讯公益404页面 由 [xirong](https://github.com/iissnan/hexo-theme-next/pull/126) 贡献

腾讯公益404页面，寻找丢失儿童，让大家一起关注此项公益事业！效果如下 <http://www.ixirong.com/404.html>

如果您需要关闭，在**主题配置目录下**找到`菜单设置`

在 commonweal: /404.html || heartbeat前加上`#`号即可

```
 #commonweal: /404.html || heartbeat
 
```

> 本主题默认开启

***

### 站点建立时间

这个时间将在站点的底部显示，例如 `© 2013 - 2015`。 编辑 **主题配置文件**，找到字段 `时间设置`。

配置示例

```
since: 2019
```

***

### 订阅微信公众号 由 [huiwang](https://github.com/iissnan/hexo-theme-next/pull/788) 贡献

**注意：** 此特性在版本 **5.0.1** 中引入，要使用此功能请确保所使用的 NexT 版本在此之后

在每篇文章的末尾显示微信公众号二维码，扫一扫，轻松订阅博客。

在微信公众号平台下载您的二维码，并将它存放于博客`source/uploads/`目录下。

然后编辑 **主题配置文件**，如下：

找到`微信公众号设置`

配置示例

```
# Wechat Subscriber
wechat_subscriber:
  enabled: true
  qcode: /uploads/wechat-qcode.jpg
  description: 欢迎您扫一扫上面的微信公众号，订阅我的博客！
```

> 本主题暂未配置微信公众号功能，如有需要请自行配置

***

### 设置「背景动画」

NexT 自带两种背景动画效果

编辑 **主题配置文件**， 搜索 `canvas_nest` 或 `three_waves`，根据您的需求设置值为 `true` 或者 `false` 即可：

**注意：** `three_waves` 在版本 **5.1.1** 中引入。只能同时开启一种背景动画效果。

`canvas_nest` 配置示例

```
# canvas_nest
canvas_nest: true //开启动画
canvas_nest: false //关闭动画
```

`three_waves` 配置示例

```
# three_waves
three_waves: true //开启动画
three_waves: false //关闭动画
```

> 本主题已经自动开启，如果需要关闭，请自行修改

背景图片

> 在themes\hexo-theme-next\source\css\_custom\custom.styl

更改url后括号内的链接即可

***

### 评论设置

本主题默认使用valine评论，其他的评论设置你可以查看next的官方文档

> <http://theme-next.iissnan.com/third-party-services.html>

在HEXO-HHC-NEXT中，Valine使用的评论是公共的，所有使用本主题的人都可以看见

如果你需要自己设置一个评论，不被别人看见

你可以注册一个Valine的账号

> 官网：<https://leancloud.cn/>

然后创建一个新的项目

在**主题配置文件**中搜索Valine评论设置

修改如下：

```
valine:
  enable: true
  appid: 你的 leancloud application appid
  appkey:  你的 leancloud application appkey
  notify: false #邮箱验证 , https://github.com/xCss/Valine/wiki
  verify: true # 验证码
  placeholder: 在这里留下你的看法或者疑问 # 显示信息
  avatar: mm # 头像样式
  guest_info: nick,mail # 输入的信息
  pageSize: 10 # pagination size
```

> 在项目的设置里，可以找到应用key，查看appid和appkey
>
> 具体j教程可以看作者提供的文档：<https://deserts.io/diy-a-comment-system/>

***

### Local Search 由 [flashlab](https://github.com/iissnan/hexo-theme-next/pull/694) 贡献

添加百度/谷歌/本地 自定义站点内容搜索

1. 安装 `hexo-generator-searchdb`，在站点的根目录下执行以下命令：

   ```
   $ npm install hexo-generator-searchdb --save
   ```

2. 编辑 **站点配置文件**，新增以下内容到任意位置：

   ```
   search:
     path: search.xml
     field: post
     format: html
     limit: 10000
   ```

3. 编辑 **主题配置文件**，启用本地搜索功能：

   ```
   # Local search
   local_search:
     enable: true
   ```

***

# 常见问题

你可以在HEXO-HHC-NEXT的wiki中查看[常见问题文档](https://github.com/kjhuanhao/HEXO-HHC-NEXT/wiki/HEXO-HHC-NEXT-problem)

如果你使用过程中有问题或者疑问可以查看[提问区](https://github.com/kjhuanhao/HEXO-HHC-NEXT/issues/1)

