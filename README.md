# dva-problems

### 主要是总结使用dva出现的一些问题

### 使用history模式下，嵌套路由，控制台报错: ```Uncaught SyntaxError: Unexpected token '<'```

index.html

```javascript
- <script src="index.js"></script>
+ <script src="/index.js"></script>
```

### 设置别名

 把.webpackrc重命名为.webpackrc.js
 具体如下

 ```js
const path = require("path"); // 引入path
module.exports = { // 导出
  alias: { // 设置别名
    "@": path.resolve("src"), // 别名： 路径
  }
};
 ```



### 使用history模式 控制台报一个警告： 

```shell
Warning: Please use `require("history").createBrowserHistory` instead of 
`require("history/createBrowserHistory")`. 
Support for the latter will be removed in the next major release.
```

解决方式：修改引入history依赖方式

```javascript
- import createHistory from "history/createBrowserHistory"
+ import { createBrowserHistory as createHistory } from "history"
```



