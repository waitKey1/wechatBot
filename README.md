
# wechatBot
wechatBot 是一个开源的微信个人号接口，使用python调用微信从未如此简单。

使用不到三十行的代码，你就可以完成一个能够处理所有信息的微信机器人。

当然，该api的使用远不止一个机器人，更多的功能等着你来发现，比如这些。
登录微信个人号，获取好友列表、群聊列表等信息。
发送文本、图片、视频、文件等消息给好友或群聊。
接收好友消息、群聊消息，并可以针对不同消息类型进行处理。
获取好友、群聊的详细信息，包括头像、地理位置等。

通过 wechatBot 的 API，你可以在微信中实现自动回复、消息转发、数据统计等功能。

wechatBot 的使用非常灵活，可以根据个人需求进行定制开发。它为开发者提供了丰富的接口，使得与微信的交互变得非常便捷。如果你想要使用 Python 来实现自动化的微信交互，itchat 是一个非常不错的选择。


该接口与公众号接口itchatmp共享类似的操作方式，学习一次掌握两个工具。

如今微信已经成为了个人社交的很大一部分，希望这个项目能够帮助你扩展你的个人的微信号、方便自己的生活。

# 安装
可以通过本命令安装itchat：

 pip install itchat
## 简单入门实例
有了wechatBot，如果你想要给文件传输助手发一条信息，只需要这样：

```python
import itchat
itchat.auto_login()

itchat.send('Hello, filehelper', toUserName='filehelper')
```

如果你想要回复发给自己的文本消息，只需要这样：

```python
import itchat

@itchat.msg_register(itchat.content.TEXT)
def text_reply(msg):
    return msg.text

itchat.auto_login()
itchat.run()
```

一些进阶应用可以在下面的开源机器人的源码和进阶应用中看到，或者你也可以阅览文档。
