package.json->/config/index.js(vue默认)
devWebpackConfig->HtmlWebpackPlugin->index.html


3:在src下新建文件‘app.vue’；
4）要想办法，让app.vue组件在浏览器中运行、显示：
操作：新建文件‘webpack.config.js’（webpack的作用：打包前端资源；要以js文件为入口，此处申明入口）
操作：在src文件夹下新建‘index.js’，作为入口文件。vue组件通过js入口文件，挂载到html页面中；
在index.js中实现挂载操作：
index.js 实现挂载 在html页面中展示vue组件的内容



vue的入口文件：
原理：
如果你是用vue.js官网提供的脚手架工具并沿用默认配置的话，你执行npm run dev的时候会出来页面，
是因为你根目录下的package.json文件里script配置了"dev": "node build/dev-server.js"，也就是其实执行的是dev-server.js这个文件，
里面有定义var webpackConfig = require('./webpack.dev.conf');
因为我们这个脚手架工具里是用webpack来打包项目文件的，依赖的webpack.dev.conf文件里又定义了var baseWebpackConfig = require('./webpack.base.conf');
在这个依赖webpack.base.conf文件里面entry入口文件就配置了app: './src/main.js'，
所以当你运行npm run dev的时候就从main.js这个入口文件开始执行了

也可以修改入口文件main的文件名：
方法：在文件里webpack.base.conf.js
找到：
entry: {
    app:["babel-polyfill", "./src/main.js"]
  },

