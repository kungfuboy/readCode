# Note

## 整体架构

### 为什么要传入window对象？

* 传入后就不需要将作用域莲退回到顶层，可能更快地访问window对象
* 压缩时可以被更替为单个字母

### 为什么要传入参数undefined？

* undefined是window的属性，在某些浏览器下，是可以被修改的
* 压缩优化

## 构造函数jQuery()

### 有7种用法

* jQuery( selector [, context] ) 接受一个CSS选择器表达式和可选的选择器上下文，返回一个包含了匹配的DOM元素的jQuery对象
* jQuery( html [, ownerDocument] )、jQuery( html, props ) 用提供的HTML代码创建DOM元素, props是个对象。
* jQuery( element )、jQuery( elementArray ) 封装DOM元素为jQuery对象
* jQuery( object ) 封装普通对象为jQuery对象
* jQuery( callback ) 绑定ready事件监听函数，当DOM结构加载完成时执行
* jQuery( jQuery object )接受一个jQuery对象，返回该jQuery对象的拷贝副本
* jQuery() 创建一个空jQuery对象

ready事件是DOMContentLoaded事件、onreadystatechange事件和函数doScrollCheck()的统称
