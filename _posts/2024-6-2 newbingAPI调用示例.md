---
layout:     post
title:      newbingAPI调用示例
subtitle:   为newbing发电
date:       2024-5-4
author:     张涵哲
header-img: img/post-bg-github-cup.jpg
catalog: true
tags:
    - python
---
# 前传    

> 本文主要是教大家如何调用newbing的API制作一个python聊天程序（没有gui）

# 正文
## 1.安装依赖
我们需要安装open ai库，版本是0.28.0    
如果你的下载速度不够，你可以用清华的镜像源，将下方代码粘贴至你的cmd      
```bash
python -m pip install -i https://pypi.tuna.tsinghua.edu.cn/simple --upgrade pip
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```    
运行完成后，openai库算是安装完成了。
## 2.代码 
将以下代码粘贴在你的python文件中，就可以运行了。
```python
llama = ""
import openai
openai.api_key = "dummy"
openai.api_base = "https://gq86p6-3000.csb.app/" # 这里可以改为你自己部署的服务，bingo 服务版本需要 >= 0.9.0
print("openai-api-key:dummy")
print("api_base:https://gq86p6-3000.csb.app/")
print("1.Creative")
print("2.Balanced")
print("3.Precise")
print("4.gpt-4")#这里对应着newbing的三种模式+gpt4
que = input("请选择模型（填序号）：")
if que == 1:
    llama = "Creative"
elif que == 2:
    llama = "Balanced"
elif que == 3:
    llama = "Precise"
else:
    llama = "gpt-4"
while True:
    a = input("请输入问题:")
    chat_completion = openai.ChatCompletion.create(model=llama, messages=[{"role": "user", "content": a}])
    print(chat_completion.choices[0].message.content)
```
## 镜像站
在代码中你要填写newbing镜像，你可以看一看作者的镜像    
1.https://gq86p6-3000.csb.app/     
2.https://qc3z4q-3000.csb.app/    
3.https://njxfw7-3000.csb.app/     
4.https://r52st6-3000.csb.app/    
