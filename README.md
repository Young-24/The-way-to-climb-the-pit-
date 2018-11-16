#react 装饰者模式
@withRouter  装饰器模式的写法写高阶函数  
高阶函数：return 的是一个 component
当 babel 版本 <7时
使用 @withRouter 会报错  
**当 babel 版本 <7时**
需要配置 `babel-plugin-transform-decorators-legacy` 插件
- `$ npm install  babel-plugin-transform-decorators-legacy -D`
- 在 .babelrc  里面配置 
    ```
    {
        "plugins": ["transform-decorators-legacy"]
    }
    ```
**当  babel  版本 > 7 时  需要配置**
- `npm install --save-dev @babel/plugin-proposal-decorators`  此时如果使用 powershell 安装会报错  要使用 cmd 命令行安装
- 将以下行添加到.babelrc文件中： 
    ```
    "plugins": [
        ["@babel/plugin-proposal-decorators", { "legacy": true }],
    ]
    ```