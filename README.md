# dva-problems

# 主要是总结使用dva出现的一些问题

### 使用history模式下，嵌套路由，控制台报错: ```Uncaught SyntaxError: Unexpected token '<'```

  解决方式：index.html 里面 
  ``` <script src="index.js"></script> ```
 改为
   ``` <script src="/index.js"></script> ```

### 设置别名
 把.webpackrc重命名为.webpackrc.js
 具体如下
 
 ```
const path = require("path"); // 引入path

module.exports = { // 导出
  alias: { // 设置别名
    "@": path.resolve("src"), // 别名： 路径
  }
};
 ```
 
