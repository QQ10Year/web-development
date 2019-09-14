package.json->/config/index.js(vue默认)
devWebpackConfig->HtmlWebpackPlugin->index.html


3:在src下新建文件‘app.vue’；
4）要想办法，让app.vue组件在浏览器中运行、显示：
操作：新建文件‘webpack.config.js’（webpack的作用：打包前端资源；要以js文件为入口，此处申明入口）
操作：在src文件夹下新建‘index.js’，作为入口文件。vue组件通过js入口文件，挂载到html页面中；
在index.js中实现挂载操作：
index.js 实现挂载 在html页面中展示vue组件的内容
