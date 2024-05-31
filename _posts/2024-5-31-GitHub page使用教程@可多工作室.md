---
layout:     post
title:      GitHub page使用教程
subtitle:   可多工作室的教程
date:       2024-05-31
author:     张涵哲
header-img: img/post-bg-ios9-web.jpg
catalog:    true
tags:
    - Github
---

github page是github（全球最大开源社区）的一项免费托管网站的服务，我会手把手教你怎么使用。
# 正文
## 1.注册账号
注册方法十分简单前提是能访问到github，见下方
### 网络加速
你可以下载Watt Toolkit   
Watt Toolkit官网 [Watt Toolkit](https://steampp.net/ "GitHub加速")。   
下载完成后打开，在左边侧边栏选择`网络加速`,然后在中间下拉，找到`github加速`，勾选，再点击窗口右上角的`一键加速`  见下图
![这是图片](/img/github-steam++.png "Magic Gardens")
### 开始注册
十分简单，具体百度，或者翻github的官方文档（中文）  
[官方文档](https://docs.github.com/zh/get-started/start-your-journey/creating-an-account-on-github)。
对了，注册时要用邮箱，不过实测国内qq邮箱就可以用。
QQ邮箱注册十分简单，你有qq就有一个qq邮箱    
地址是`QQ号@qq.com`
## 开始部署
### 新建仓库
你需要新建一个github仓库,登陆后访问以下网址
[新建仓库](https://github.com/new)。
在`Repository name`一栏中填`你的github用户名.github.io`  
比如我的github用户名是`zhanghanzhe666`,那就填`zhanghanzhe666.github.io`   

勾选`Add a README file`,总体配置见下图    
![这是图片](/img/new.png "Magic Gardens")     
图中的红色警告是我的github仓库有重名，因为我的博客仓库就是`zhanghanzhe666.github.io`，不过正常情况不会报错。   
接下来拉到网页底部，点击绿色的`Create repository`按钮。   
接下来，你会跳转到你的仓库网址。
### 上传文件
**以下的所有操作请将网页（浏览器）调至最大化**   
点击`Add file`,在弹出的窗口中选择`Upload files`,跳转到上传文件界面。具体见下图     
![这是图片](/img/file.png "Magic Gardens")   
然后将文件拖入方框（在下图用蓝色方框和箭头指示的部分）中**先看下面的注意事项**  
***********
**注意事项**      
**这里推荐将HTML文件单独上传，不要带文件夹！！！，主页直接上传index.html,当然，素材文件可以直接拖文件夹上传，HTML文件请从文件夹中分离出来，单个上传，上传完成后也不要集合在一个文件夹中，放在仓库根目录，不然配置文件要改很多次。**   
**由于github pages会自动将index.html当成主页文件自动部署，所以将你的工作室主页html文件命名为index.html**     
***********
接着等进度条走完消失，**注意一定要等到进度条消失，不然会上传失败**，然后点击绿色按钮`Commit changes`提交更改。具体见下图
![这是图片](/img/up.png "Magic Gardens")   
### 修改配置
第一步，点击显示仓库名称上方的栏中的`Settings`选项，你可以看下图     
![这是图片](/img/pages1.png "Magic Gardens")   
点击`Settings`按钮后跳转到设置界面。
然后点击侧边栏中的`pages`选项。    
接着将`None`选项展开勾选成`main`,更改完后点`Save`,如果顶部出现蓝色横幅，显示`GitHub Pages source saved.`那就是配置更改成功了，刚刚的所有步骤你可以在下图找到。    
![这是图片](/img/page2.png "Magic Gardens") 
## 部署完成
接着等待1~5分钟，如果右侧侧边栏出现`Deployments`的选项，就代表部署成功，你可以在浏览器中输入你的仓库名称就可以访问你的网站了，你也可以在Deployments中找到你的网站网址。
![这是图片](/img/Deployments.png "Magic Gardens") 
## 扩展
如果你要更新你的网站，你可以直接在GitHub更新，进入仓库主页，点击要更新的文件名，见下图         
![这是图片](/img/upfile4.png "Magic Gardens")     
然后会跳转到文件的代码预览，点击`🖊`进入编辑器模式（紫色方框），见下图。        
![这是图片](/img/upfile.png "Magic Gardens")      
进入之后开始编辑文件，完成后点击绿色按钮`Commit changes...`（红色方框），见下图。     
![这是图片](/img/upfile2.png "Magic Gardens")      
最后在弹出的窗口中点击绿色按钮`Commit changes`提交更改。见下图     
![这是图片](/img/upfile3.png "Magic Gardens")       
GitHub会自动重新部署，你的代码会很快更新。    
# 结尾
整体的教程就是这样，我做了两天，也不知道你看没看懂...... 
# 工作室官网示例代码 
对了，可多工作室，你不是想做官网吗？我花五分钟写了一个主页代码示例，你可以修改，参考一下
```
<!DOCTYPE html>
<html lang="zh">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>我的编程工作室</title>
<style>
  body { font-family: 'Arial', sans-serif; margin: 0; padding: 0; }
  .header { display: flex; justify-content: space-between; align-items: center; padding: 10px 50px; }
  .logo { font-size: 24px; font-weight: bold; }
  .nav { list-style: none; }
  .nav li { display: inline; margin-left: 20px; }
  .nav a { text-decoration: none; color: #333; }
  
  .carousel { max-width: 100%; margin-top: 20px; position: relative; }
  .carousel img { width: 100%; border-radius: 15px; }
  .work, .member { border-radius: 15px; transition: transform 0.3s; margin: 20px; padding: 10px; }
  .work:hover, .member:hover { box-shadow: 0 4px 8px rgba(0,0,0,0.5); transform: translateY(-5px); }
  .work img, .member img { border-radius: 15px; width: 100%; }
  .team { display: flex; flex-wrap: wrap; justify-content: space-around; }
  .member { text-align: center; }
  .member img { border-radius: 50%; }
</style>
</head>
<body>
<div class="header">
  <div class="logo">LOGO+名称</div>
  <ul class="nav">
    <li><a href="#home">首页</a></li>
    <li><a href="#works">作品</a></li>
    <li><a href="#team">团队</a></li>
    <li><a href="#contact">联系我们</a></li>
  </ul>
</div>
<div class="carousel" id="carousel">
  <!-- 轮播图图片 -->
  <a href = 'https://www.baidu.com'><img src="image1.jpg" alt="轮播图1"></a>
  <a href = 'https://www.baidu.com'><img src="image2.jpg" alt="轮播图2"></a>
  <a href = 'https://www.baidu.com'><img src="image3.jpg" alt="轮播图3"></a>
  <a href = 'https://www.baidu.com'><img src="image4.jpg" alt="轮播图4"></a>
  <a href = 'https://www.baidu.com'><img src="image5.jpg" alt="轮播图5"></a>
</div>
<div class="works">
  <!-- 作品展示模块 -->
  <a href = 'https://www.baidu.com'><div class="work">
    <img src="work-image.jpg" alt="作品图片">
    <h3>作品标题</h3>
    <p>作品简介...</p>
  </div>
</div></a>
<div class="team">
  <!-- 团队成员展示模块 -->
  <a href = 'https://www.baidu.com'><div class="member">
    <img src="member-photo.jpg" alt="成员照片">
    <h3>职位名称</h3>
    <p>成员简介...</p>
  </div>
</div></a>
<script>
// 轮播图JavaScript逻辑
let currentSlide = 0;
const slides = document.querySelectorAll('#carousel img');
const nextSlide = () => {
  slides[currentSlide].style.display = 'none';
  currentSlide = (currentSlide + 1) % slides.length;
  slides[currentSlide].style.display = 'block';
}
setInterval(nextSlide, 3000);
</script>
</body>
</html>
```
