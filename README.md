# 使用 Github pages + Hexo 建立个人博客网站

## 前提准备
- 想在github上搭建自己的个人博客之前需要准备好这些工作
- 注册一个github账号（网上有很多教程）
- 创建一个仓库，仓库名格式一定是**你github上账号用户名.github.io**
![1569487055_1_.jpg](https://i.loli.net/2019/09/26/TOsfRaVkr8IJH5U.png)<br />
这里因为这个仓库我已经创建好了，所以他会提示报错。<br />
![1569487357_1_.jpg](https://i.loli.net/2019/09/26/HdyjpbcBuQDI7XE.png)<br/>
点击绿色按钮，就可以创建成功。
- 这时github识别到你建立了名为 “你的用户名”.github.io 的仓库<br />
它会默认开启该仓库的GitHub Pages功能
![68747470733a2f2f692e6c6f6c692e6e65742f323031392f30322f32332f356337306665643961353166342e6a7067.jpg](https://i.loli.net/2019/09/26/zwLGfDr7d5Kgqtn.jpg)
- 这时你就可以在浏览器上输入https://你的用户名.github.io/
- 但你访问到的页面，是空白的，因为仓库里并没有页面可以显示

## 在搭建博客Hexo之前要安装好这些
- [git安装链接](https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496)
- [node.js安装链接](https://nodejs.org/zh-cn/download/)

## 在上面都完成后，再进行安装Hexo
- 在桌面新建一个空的文件夹，然后在编译器打开控制台或者在电脑按win+r输入cmd+回车；<br />
- 在控制台运行如下的命令:<br />

```php
cd hexo/                  这是切到你刚刚新建的空文件目录
然后执行下面的命令:
npm install hexo-cli -g   在全局安装 hexo-cli 包
cd blog/                  初始化 hexo 博客，blog 为创建的博客名称,转到当前的博客文件夹
npm install               根据 package.json安装所有依赖的包
hexo server               开启 hexo 服务
```
- 默认的启动端口是http://localhost:4000/<br />
- 将链接在浏览器打开后，你可以看到hexo为搭建的博客
![12.jpg](https://i.loli.net/2019/09/26/F96cEQWnCZ3LIap.jpg)<br />
- 这是hexo默认的主题<br />
- 如果你不喜欢这个主题，你可以去Hexo的官网上找你喜欢的模板主题

## Hexo的官网
- http://hexo.io/themes/ 
- 在这里面你可以去找你喜欢的模板<br />
![1569499487_1_.jpg](https://i.loli.net/2019/09/26/apdnsmUwXKvVzqy.png)

- 比如你看中了上面喜欢的模板点击进入模板后点击红圈的图标
![321.jpg](https://i.loli.net/2019/09/26/TkoNvl9tKRjSFu8.png)

- 进入到模板的github，选中你模板的仓库
![1569500545(1).jpg](https://i.loli.net/2019/09/26/PBwrXsajxDEv65h.png)
- 接下来就按照你模板github上的README.md文件上的说明来安装并使用该模板

- 按照里面的说明安装成功后，在本地控制台输入hexo server<br /> 
然后访问 http://localhost:4000 可以看到你要的模板在浏览器中能显示出来了。<br />
这样基本就成功了。

## 如何部署到github上？用 '你的用户名'.github.io访问
- 首先你可以在控制台执行下面的命令
```php
npm install hexo-cli -g
hexo clean                 清除缓存文件 db.json 和已生成的静态文件 public
hexo g                     会生成一个名为public的文件夹
```
- 在你安装模板文件的目录你会看到生成了一个public文件夹<br />
- 这时你回到你github上，clone你刚刚创建的仓库到本地<br />
![1569502199_1_.jpg](https://i.loli.net/2019/09/26/dRNDtUaoLZMnTS7.png)
- 这里推荐大家安装GitHub DeskTop软件，方便部署（这里我用的就是GitHub DeskTop）
  点击 open in desktop ，这时GitHub DeskTop弹出请求框，如果你没有安装，它会先帮你安装。<br />
  ![1569502467_1_.jpg](https://i.loli.net/2019/09/26/g7R65GDSjKXd4k9.png)<br />
  将这个clone到你的本地
- local path可以设置该仓库存放的位置（一定要记住）<br />
  之后将**public文件夹中的文件**全部复制到该仓库存放的文件夹下<br />
  这时 GitHub DeskTop 会有文件更改的提示:<br />
  ![1569503123_1_.jpg](https://i.loli.net/2019/09/26/YWsR35HSbnfUxDF.png)<br />
  在上面两个红框中填写修改原因或随便写一些东西，然后点击蓝色按钮，<br />这时它会将文件提交到缓存库<br />
  ![456.jpg](https://i.loli.net/2019/09/26/9xmsbwGiqnuLapv.jpg)<br />
  这是上方会出现Push origin的选项，点击就可以将更改部署到github上了<br>
  打开https://你的用户名.github.io/
  就可以看到完成的博客咯！
  
## 接下来就是，写博客
- 写博客文件是放在你下载模板的文件里面，博客是用md文件写的<br />
![1569503649_1_.jpg](https://i.loli.net/2019/09/26/Is43M1tbZFpK8am.png)<br />
 - 写完之后，在控制台中切到你的文件目录执行下面命令
 - npm install hexo-cli -g
 - hexo clean    会删除掉之前的public文件
 - hexo g       重新生成public文件
 - 最后将生成的public里面的文件都复制，这里只要复制public文件里面的所有文件
 - 去粘贴到github上clone下来的文件里面，然后使用GitHub DeskTop，pull到github上面。
 - 最后你在浏览器中访问 https://‘你的用户名’.github.io就可以看到你的博客了
### 注意
- 你每次写博客，都要在本地生成public文件，然后将public里面的文件复制,粘贴到<br />
你github上clone下来的文件里里面，将之前的public文件替换掉，然后再用GitHub DeskTop<br />
将代码pull上github.