# Note

## 整体架构

### 为什么要传入window对象？

* 传入后就不需要将作用域莲退回到顶层，可能更快地访问window对象
* 压缩时可以被更替为单个字母

### 为什么要传入参数undefined？

* undefined是window的属性，在某些浏览器下，是可以被修改的
* 压缩优化