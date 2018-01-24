## 前言
最近微信小游戏跳一跳大热，从网上找了一个python外挂，测试后通常只能得几十分，
最多也只能到100多分，而且adb经常出错。无奈只好自己debug，最后可以到一千多分。

## update - Jan24-2018
腾讯显然更新了跳一跳，原程序已经无法使用，发现时jump函数不起作用，待后续fix

## 程序来源
原程序来自 https://github.com/moneyDboat/wechat_jump_jump
由于刚开始玩GitHub没有直接fork，望见谅。
本程序地址https://github.com/Michael2Tang/wx-jump.git


## 主要使用的Python库及对应版本：
python 2.7  
opencv-python 3.1.0  
numpy 1.13.3  

## Opencv  
首先介绍下opencv，是一个计算机视觉库，本文将用到opencv里的模板匹配和边缘检测功能。  

### 模板匹配
模板匹配是在一幅图像中寻找一个特定目标的方法之一。这种方法的原理非常简单，遍历图像中的每一个可能的位置，比较各处与模板是否“相似”，当相似度足够高时，就认为找到了我们的目标。  
例如提供小人的模板图片
