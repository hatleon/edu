[toc]

### 与博客有关的应聘回忆

博客作为个人平时知识总结的空间，不仅帮助我们记录一些学到的知识内容，也能同时创建一个自己所为的品牌，让更多人认识你，这一点在你应聘的时候可是一份底牌哦！

> 记得从第一家公司跳槽面试时，一面的HR上来就问我：
>
> “作为软件从业者，平时有在CSDN上写博客的习惯吗？”
>
> 我的回答是：“没有，CSDN上满篇的广告。”
>
> 然而没等我说出下一句，我一直在简书上写文章，HR已经微微一笑要清场了...我想一定是我的清扬洗发水不小心买成了清场，才造成了这一次令我终身难忘的面试回忆...

### 博客的选择

当前互联网上的博客平台数不胜数，博客园、CSDN、简书、掘金、OSCHINA、豆瓣、知乎、Github(也算吧...) 等等，之前比较喜欢博客园，但由于维护能力跟不上，app等太过简陋就放弃了，之后辗转csdn、oschina，都因为铺天盖地的广告让人觉得索然无味。刚好在2013年，简书平台成立了，那时候的简书简直堪称外貌协会的心意之所。不管是暖暖的配色设计，还是优秀的手机app使用效果，都堪称当时经典。于是果断入坑，但因为17年换手机，导致历史账号丢失，被迫新起账号重头再来。

### 博客平台的致命弊端

> 之前在群里听过这么一个笑话，一个大佬的知乎文章被别人剽窃，然后他申诉举报该用户 。然后第二天，他和那个人的账号都被封停了，因为举报提供的原文链接中有自己公众号的二维码，多么反转的一个故事。。。

其实很早就开始关注一些大佬们自己搭建博客写文章的操作，但一直觉得简书当前挺好，也就没太关注，直到今年10月简书开始了和其他平台一样的大清洗，所有在文章中粘贴有二维码，引导链接的文章全部封停，一瞬间锁定了我50多篇的文章，虽然这一举动在其他平台早有规定，但无通知的突然锁定，还是让人心寒。自己搭建个人博客的想法也就此展开。

![文章被锁定](https://upload-images.jianshu.io/upload_images/5847426-00e191420386f54c.gif?imageMogr2/auto-orient/strip)

### 个人博客工具选型

既然决定搭建个人博客，那么我们该用什么工具来实现呢？在此之前，我们首先需要了解博客的分类。

**博客在广义上其实可以分为两类，源码搭建博客和静态配置博客。**

前者我们需要自己开发，或者从网上找一个开源的博客项目，之后购买一台服务器，搭建自己的博客项目。

而后者，则是使用一些前端工具，将你的文章生成一个个人博客。

源码搭建博客，这个你不仅要考虑网站的代码逻辑与安全性，还涉及后期大量时间的维护，费时费力，对于我这种懒人是不会考虑的。

那么，搭建静态博客的工具，我们该如何选择呢？

- Hexo 
- Sphinx
- Docsify
- Jekyll
- ... ...

hexo、sphinx、Docsify在使用时需要依赖Nodejs，而Jekyll则依赖Ruby，作为爱国青年(其实是懒得接触)，Ruby我是肯定不会考虑的，难么剩下的三种工具该如何选择呢？Hexo和Sphinx有一个问题，我们每次部署前需要将写好的markdown编译成html后再进行发布，而Docsify无需编译，只要自己简单创建简单的路由，即可支持markdown直接发布网站，那么该怎么选择，你懂了吧....

### Docsify的安装

刚才说到Docsify需要依赖Nodejs，那么我们的电脑首先需要安装它。这个网上教程就太多了，进入nodejs中文官网下载：

[http://nodejs.cn/download/](http://nodejs.cn/download/)

安装好后，简单确认即可：

![安装Nodejs](https://upload-images.jianshu.io/upload_images/5847426-d0c6e1045201943a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

接下来我们就可以通过Nodejs下的npm命令安装Docsify了，但再次之前，你需要配置一下npm的淘宝仓库地址，不然下载超时是没跑的。

```bash
# 使用淘宝镜像
npm config set registry https://registry.npm.taobao.org
# 验证是否ok
npm config get registry
```

下来，我们使用 `npm i docsify-cli -g`命令完成安装即可。

安装完成后，输入`docsify -v` 来查看是否安装ok

![Docsify安装验证](https://upload-images.jianshu.io/upload_images/5847426-a390eaf1be7371b1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 创建博客仓库

安装好Docsify后，我们就可以开始搭建自己的博客项目了，NONONO，请先创建一个Git仓库，用于一会儿发布你的博客。个人推荐使用**码云**，而非Github。不仅访问速度，还牵扯搭建与认证方式。我已经吧github上的代码全部迁移到码云了，之后github可能就不怎么使用了，网络实在是不给力，与其辛苦翻墙，为啥不用更方便的仓库呢？

![我的码云](https://upload-images.jianshu.io/upload_images/5847426-f0f6c11cf37d1d40.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

1. 注册/登录码云： [https://gitee.com/](https://gitee.com/)

   

2. 然后创建自己的项目

   ![新建仓库](https://upload-images.jianshu.io/upload_images/5847426-d56c68530deff797.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3. Clone 并完成首次提交

   ```bash
   mkdir BlogTest
   cd BlogTest
   git init
   touch README.md
   echo # BreezePython >> README.md
   git add README.md
   git commit -m "first commit"
   git remote add origin https://gitee.com/BreezePython/BlogTest.git
   git push -u origin master
   ```

![首次提交](https://upload-images.jianshu.io/upload_images/5847426-e872ed47e767cf6c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 初始化博客项目

刚才我们的命令已经创建并进入了BlogTest目录，下来就可以创建静态博客项目了：

1. 在博客目录下执行初始化操作

   `docsify init  .`  然后输入y 进行确认，此时我们就创建好了初始目录

   ![Docsify初始目录](https://upload-images.jianshu.io/upload_images/5847426-4ce4eabd1948a836.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

   我们初始化后的目录内会存在一个**.nojekyll**的空文件，这个文件的作用是，在你提交代码到git仓库后，可以避免仓库忽略_开头的文件，因为Docsify的很多文件都是以_开头的。

   另外一个**index.html**文件，就是Docsify唯一的配置文件。我们只需要维护这个入口html文件，即可完成所有的博客搭建操作。

2. 下来我们启动本地服务，查看下效果：

   ```
   # 输入本地启动命令
   docsify serve .
   
   Serving D:\BlogTest now.
   Listening at http://localhost:3000
   ```

   访问 [ http://localhost:3000](http://localhost:3000) 查看

   ![启动博客](https://upload-images.jianshu.io/upload_images/5847426-f973f6c2a78a2dde.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

   如果显示如上表示我们初始化博客的工作已经完成，BreezePython是我们在初始化仓库的时候往README.md中插入的内容，下面的工作就该丰满它了。

### 丰满博客配置

让我们打开index.html文件简单看下相关的文件配置说明，在**window.$docsify**中追加的内容，基本都是用来配置页面相关信息的，而在第二个红框后，我们可以追加美化的js插件。

![配置文件简单说明](https://upload-images.jianshu.io/upload_images/5847426-4e3ebf9748b6855c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

如果时间充裕，大家可以看下Docsify的中文网站：

[https://docsify.js.org/#/zh-cn/](https://docsify.js.org/#/zh-cn/)

当然，直接看我为大家整理好的内容， 可以帮你更快速的完成博客搭建。

#### 主题配置

个人整理了8种docsify的主题样式，大家可以一 一替换查看效果：

```
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/vue.css">
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/buble.css">
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/dark.css">
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/pure.css">
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/dolphin.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-defaults.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-defaults.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-simple-dark.css">
```

#### window.$docsify总结

这里为大家整理好了页面有关的配置，修改内容后，即可使用。

```js
<script>
    window.$docsify = {
        // 侧边栏支持，默认加载的是项目根目录下的_sidebar.md文件
        loadSidebar: true,
        // 导航栏支持，默认加载的是项目根目录下的_navbar.md文件
        loadNavbar: true,
        // 最大支持渲染的标题层级
        maxLevel: 4,
        // 自定义侧边栏后默认不会再生成目录，设置生成目录的最大层级，建议配置为1或者2
        subMaxLevel: 4,
        // 外链表达式
        externalLinkTarget: '_blank',

        // auto2top: true,
        search: {
            maxAge: 86400000,
            paths: 'auto',
            placeholder: {
                '/': '搜索'
            },
            noData: {
                '/': '找不到结果'
            },
            depth: 4,
        },
        'flexible-alerts': {
            style: 'flat'
        },
        formatUpdated: '{YYYY}/{MM}/{DD} {HH}:{mm}:{ss}',
        // autoHeader: true,
        // relativePath: true,
        coverpage: true,
        homepage: 'README.md',
        disqus: 'shortname',
        alias: {
            '/.*/_navbar.md': '/_navbar.md',
            '/.*/_sidebar.md': '/_sidebar.md',
        },
        logo: 'images/breezepython.png',
        name: '清风Python',
        repo: 'https://github.com/breezepython',
        footer: {
            copy: '<span>公众号：清风Python &copy; 2020. </span>',
            auth: 'All rights reserved',
            pre: '<hr/>',
            style: 'text-align: right;',
            class: 'className',
            
        },
    }
</script>
```

这里简单说明下几个关键内容：

- coverpage: true  homepage: 'README.md' 展示封面内容

- repo: 'https://github.com/breezepython' 即可在封面右上角 添加一个git

- 创建一个**_coverpage.md**的文件，写入的内容可以在封面进行展示，比如添加如下内容：

  ```
  ![logo](images/breezepython.png ':size=260x260')
  
  > 让学习变得简单有趣  
  > 安儿
  > 清风Python的藏经阁
  
  [简书](https://www.jianshu.com/u/d23fd5012bed)
  [CSDN](https://blog.csdn.net/BreezePython)
  [GitHub](https://github.com/breezepython)
  ```

  ![修改后的页面](https://upload-images.jianshu.io/upload_images/5847426-501cd8d15a99438b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

  ![主页内容](https://upload-images.jianshu.io/upload_images/5847426-d4af89c9ee6f710e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- loadNavbar: true,  看标签名字就知道，如果要设置顶部标签，就启用
- loadSidebar: true, 侧边连是否要显示

### Docsify插件总结

```js
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/disqus.min.js"></script>
<!-- docsify的js依赖 -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
<!-- emoji表情支持 -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>
<!-- 图片放大缩小支持 -->
<!--<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/zoom-image.min.js"></script>-->
<!-- 搜索功能支持 -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>
<!--在所有的代码块上添加一个简单的Click to copy按钮来允许用户从你的文档中轻易地复制代码-->
<script src="//cdn.jsdelivr.net/npm/docsify-copy-code"></script>
<!--分页导航插件-->
<script src="//cdn.jsdelivr.net/npm/docsify-pagination/dist/docsify-pagination.min.js"></script>
<!-- 侧边栏折叠 -->
<script src="//cdn.jsdelivr.net/npm/docsify-sidebar-collapse/dist/docsify-sidebar-collapse.min.js"></script>
<!-- 面包屑提示 -->
<script src="static/docsify-plugin-flexible-alerts.min.js"></script>
<!-- 添加版权信息 -->
<script src="static/docsify-footer-enh.min.js"></script>
<!--语法高亮添加-->
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-bash.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-python.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-java.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-yaml.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-json.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-sql.min.js"></script>

<!--docsify的分页导航插件-->
<script src="//cdn.jsdelivr.net/npm/docsify-pagination/dist/docsify-pagination.min.js"></script>
<!-- mouse click heart sign -->
<script src="//cdn.jsdelivr.net/gh/jerryc127/butterfly_cdn@2.1.0/js/click_heart.js"></script>

<!-- alert 样式 -->
<link rel="stylesheet" href="https://cdn.bootcss.com/sweetalert/1.1.3/sweetalert.min.css" type='text/css' media='all' />

<!-- 复制提醒 -->
<script src="https://cdn.bootcss.com/sweetalert/1.1.3/sweetalert.min.js"></script>
<script>
  document.body.oncopy = function () {
    swal("复制成功 🎉",
            "转载或引用请务必保留原文链接，并申明来源。\n欢迎关注我的微信公众号：清风Python 😊",
            "success"); };
</script>

<!-- 访问量统计 -->
<script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script>

<script src="https://eqcn.ajz.miesnfu.com/wp-content/plugins/wp-3d-pony/live2dw/lib/L2Dwidget.min.js"></script>
<script>
  L2Dwidget.init({
    "model": {
      //jsonpath控制显示那个小萝莉模型，
      //(切换模型需要改动)
      jsonPath: "https://unpkg.com/live2d-widget-model-koharu@1.0.5/assets/koharu.model.json",
      "scale": 1
    },
    "display": {
      "position": "right", //看板娘的表现位置
      "width": 80,  //小萝莉的宽度
      "height": 150, //小萝莉的高度
      "hOffset": -15,
      "vOffset": -20
    },
    "mobile": {
      "show": true,
      "scale": 0.5
    },
    "react": {
      "opacityDefault": 0.7,
      "opacityOnHover": 0.2
    }
  });
</script>


运行时间统计
<script language=javascript>
  function siteTime() {
    window.setTimeout("siteTime()", 1000);
    var seconds = 1000;
    var minutes = seconds * 60;
    var hours = minutes * 60;
    var days = hours * 24;
    var years = days * 365;
    var today = new Date();
    var todayYear = today.getFullYear();
    var todayMonth = today.getMonth() + 1;
    var todayDate = today.getDate();
    var todayHour = today.getHours();
    var todayMinute = today.getMinutes();
    var todaySecond = today.getSeconds();
    /* Date.UTC() -- 返回date对象距世界标准时间(UTC)1970年1月1日午夜之间的毫秒数(时间戳)
    year - 作为date对象的年份，为4位年份值
    month - 0-11之间的整数，做为date对象的月份
    day - 1-31之间的整数，做为date对象的天数
    hours - 0(午夜24点)-23之间的整数，做为date对象的小时数
    minutes - 0-59之间的整数，做为date对象的分钟数
    seconds - 0-59之间的整数，做为date对象的秒数
    microseconds - 0-999之间的整数，做为date对象的毫秒数 */
    var t1 = Date.UTC(2020, 12, 13, 00, 00, 00); //北京时间2020-02-10 00:00:00
    var t2 = Date.UTC(todayYear, todayMonth, todayDate, todayHour, todayMinute, todaySecond);
    var diff = t2 - t1;
    var diffYears = Math.floor(diff / years);
    var diffDays = Math.floor((diff / days) - diffYears * 365);
    var diffHours = Math.floor((diff - (diffYears * 365 + diffDays) * days) / hours);
    var diffMinutes = Math.floor((diff - (diffYears * 365 + diffDays) * days - diffHours * hours) / minutes);
    var diffSeconds = Math.floor((diff - (diffYears * 365 + diffDays) * days - diffHours * hours - diffMinutes * minutes) / seconds);
    document.getElementById("sitetime").innerHTML = " 🎮已运行 " + diffDays + " 天 " + diffHours + " 小时 " + diffMinutes + " 分钟 ";
  }
  siteTime();
</script>
<!-- Gitalk 评论系统 -->
<link rel="stylesheet" href="https://wugenqiang.gitee.io/notebook/plugin/gitalk.css">
<!-- Gitalk 评论系统 -->
<script src="https://wugenqiang.gitee.io/notebook/plugin/gitalk.js"></script>
<script src="https://wugenqiang.gitee.io/notebook/plugin/gitalk.min.js"></script>
<script src="https://wugenqiang.gitee.io/notebook/plugin/md5.min.js"></script>
<script>
  // title_id需要初始化
  window.title_id = window.location.hash.match(/#(.*?)([?]|$)/) ? window.location.hash.match(/#(.*?)([?]|$)/)[1] : '/';
  const gitalk = new Gitalk({
    clientID: '2e7cb0ea4c6183ef4d5f',
    clientSecret: 'd0e257ab5e9589a205875ca3e585186bf8cd5500',
    repo: 'Blog',
    owner: 'BreezePython',
    admin: ['BreezePython'],
    title: decodeURI(window.title_id),
    distractionFreeMode: false,	// 是否添加全屏遮罩
    id: md5(window.location.hash),	// 页面的唯一标识，gitalk 会根据这个标识自动创建的issue的标签,我们使用页面的相对路径作为标识
    enableHotKey: true,	// 提交评论快捷键(cmd/ctrl + enter)
  })
  // 监听URL中hash的变化，如果发现换了一个MD文件，那么刷新页面，解决整个网站使用一个gitalk评论issues的问题。
  window.onhashchange = function (event) {
    if (event.newURL.split('?')[0] !== event.oldURL.split('?')[0]) {
      location.reload()
    }
  }
</script>
```

 找了几十个网站，总结出上面最全的插件集合，注释给大家都写了。直接粘到网站上就好了。

### 侧边栏路由设置

> 这里重点说下_sidebar.md，这是Docsify中唯一比较麻烦的点。

如果你是一篇文章涵盖古今中外一口气写到底，比如docsify官网那样的，那么_sidebar.md对你无用，Docsify会根据你文章的标题，自动显示侧边栏目录。

但如果你是编程大牛，同时学习Java、Python、C++等等，每个编程语言下又区分了很多的知识点，那么_sidebar.md是必须的。

_sidebar.md总体有两种模式：

- 通篇只使用根目录下这一个_sidebar.md，拿我的目录来说，因为文章和目录太多了，所以我使用一个统一路由完成所有目录及文章的跳转，如下面的例子：

  ![我的文章目录](https://upload-images.jianshu.io/upload_images/5847426-206da32fd490f969.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

  这里要注意几点：

  1. 针对目录的跳转，在尾部需要添加一个/
  2. 每个目录下需要存在一个README.md文件，否则跳转到这个目录会显示404
  3. 路径的地址需要严格按照路径设置，但是可以重新改名下。

- 另外一种比较细致的方式是， 主节点使用一个_sidebar.md进行目录的跳转，在目录目录下单独设置_sidebar.md ,这种二级路由的方式，会比较直观，但存在一个问题，跳转到子_sidebar.md后，就没有返回主目录的入口了...此时我们可以通过顶部设置_navbar.md提供用户跳转到其他目录的操作。

### 最终效果展示

我们整理好上面的内容，并且把自己之前写好的markdown文件放到自己创建的markdown文件夹下，网站基本就已经搭建完成了。来看看效果吧：

![效果展示](https://upload-images.jianshu.io/upload_images/5847426-488f4242d8607a70.gif?imageMogr2/auto-orient/strip)

### 部署到码云Pages

由于我双十一的时候买了一个域名和服务器，刚好拿来部署我的博客，但很多朋友们，可能只是想部署下玩玩，没有这些资源那该如何操作呢？这就是为什么之前让大家在码云申请一个仓库的作用了，虽然github也有相关操作，但是操作是在太卡了，还是码云使用起来方便些，3分钟搭建好自己的博客：

- 首先，我们应该把刚才创建的目录提交仓库，简单的git push即可。

- 进入Gitee Pages

  ![Gitee Pages](https://upload-images.jianshu.io/upload_images/5847426-ea8ee4a837e3a95e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 开始部署(正常第一次进来是部署，不熟过一次就是更新了)

  ![image-20201220212128381](D:\文章文档\博客搭建\${images}\image-20201220212128381.png)

- 等待部署完成后，会显示你的Gitee Pages域名地址：

  [https://breezepython.gitee.io/blogtest](https://breezepython.gitee.io/blogtest)

  ![image-20201220212247216](D:\文章文档\博客搭建\${images}\image-20201220212247216.png)

  现在，让我们去访问下部署好的静态博客吧。

  ![Gitee Pages博客展示](https://upload-images.jianshu.io/upload_images/5847426-edbfe4f81d9d9c40.gif?imageMogr2/auto-orient/strip)

