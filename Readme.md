qiqi
====

> `[实验性质]` 基于`动态编译`和`线下打包`的 component 前端解决方案，尝试通过线下手段达到Polymer的变成体验

![i](https://cloud.githubusercontent.com/assets/2239584/5889955/d24e8814-a47b-11e4-9a6e-0b2abf03b14c.gif)

[大图](https://cloud.githubusercontent.com/assets/2239584/5889906/bf180eac-a479-11e4-9564-0a9d8da22793.gif)

试一试
------

* 安装依赖

> npm install

* 运行本地服务器

> node app

* 浏览DEMO

打开浏览器，打开页面：http://localhost:3000/index.html


解决核心问题
------------

* 如何解决css 没有 namespace 的问题？
> 基于`BEM`的伪namespace方案，书写代码时候使用占位符`$__`，会自动替换成该component名，例如component名叫helloworld，源码中的class为$__text，替换后变成helloworld__text。

* 如何解决自定义元素，类似我们自定义一个<helloworld></helloworld>元素？
> 基于`编译`解决，通过替换自定义元素模拟。


思想
----

* component -> 自定义DOM元素
* template -> 页面基础结构，布局信息
* particular -> 页面独有的自定义样式和脚本
* page -> 将components填充template，并加上particular
