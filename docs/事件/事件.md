?> 事件监听器允许您在游戏内发生事件时执行特定代码。

### 监听事件
假设我们想要监听玩家进入服务器，我们需先调用`listen.onJoin()`函数，并传入一个函数作为回调，如：

```javascript
listen.onJoin((en) => {})
```

在事件被触发后会传入一个事件对象，这个对象包括很多方法，具体方法请参照具体事件对象文档。

举个例子，编写一段在玩家加入服务器后向玩家发送欢迎消息的代码：

```javascript
listen.onJoin((en) => {
	let pl = en.getPlayer()
	pl.sendMassage(`Hi，${pl.getName()}，欢迎加入服务器！`)
})
```

现在，我们进入服务器就可以看到欢迎消息了!