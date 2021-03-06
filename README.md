# DingTalkBot
![](https://travis-ci.org/LZC6244/DingTalkBot.svg?branch=master)[![codecov](https://codecov.io/gh/LZC6244/DingTalkBot/branch/master/graph/badge.svg)](https://codecov.io/gh/LZC6244/DingTalkBot)  
Python 实现钉钉群聊天机器人。  
群机器人是钉钉群的高级扩展功能。群机器人可以将第三方服务的信息聚合到群聊中，实现自动化的信息同步。

- 开发环境： `python 3.7.5`
- 使用需求：起码拥有一个钉钉群聊天机器人（获取自定义机器人webhook`Webhook`）（[如何申请](#dingtalk)）

## 安装
> pip install DingTalkBot

## 简易demo
```python
from DingTalkBot.bot import DingTalkBot

# TestBot
dt_bot = DingTalkBot(
    web_hook='your web_hook',
    secret='your secret')

content_text = '今天天气真好，是么？'
dt_bot.send_text(content_text)
```

## 消息类型及DEMO
- text 类型  
  ![](https://github.com/LZC6244/DingTalkBot/blob/master/imgs/01.png)

- link 类型  
  ![](https://github.com/LZC6244/DingTalkBot/blob/master/imgs/02.png)
  
- markdown 类型  
  ![](https://github.com/LZC6244/DingTalkBot/blob/master/imgs/03.png)
  
  **ps:** 目前只支持md语法的子集，具体支持的元素如下（钉钉限定）
    
  ```text
  标题
  # 一级标题
  ## 二级标题
  ### 三级标题
  #### 四级标题
  ##### 五级标题
  ###### 六级标题
  
  引用
  > A man who stands for nothing will fall for anything.
  
  文字加粗、斜体
  **bold**
  *italic*
  
  链接
  [this is a link](http://name.com)
  
  图片
  ![](http://name.com/pic.jpg)
  
  无序列表
  - item1
  - item2
  
  有序列表
  1. item1
  2. item2
  ```  

- 整体跳转 ActionCard 类型  
  ![](https://github.com/LZC6244/DingTalkBot/blob/master/imgs/04.png)
  
- 独立跳转 ActionCard 类型  
  ![](https://github.com/LZC6244/DingTalkBot/blob/master/imgs/05.png)
  
- FeedCard 类型  
  ![](https://github.com/LZC6244/DingTalkBot/blob/master/imgs/06.png)

# 参考链接

- <span id="dingtalk">[钉钉开发文档](https://ding-doc.dingtalk.com/doc#/serverapi2/qf2nxq)</span>