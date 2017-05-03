# HTML&CSS

参考[Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)（[中文版本](http://www.runoob.com/w3cnote/htmlcssguide.html)）

如果要选一种CSS预编译语言就选SCSS吧:
[SCSS vs LESS](http://ourjs.com/detail/52e096ce4534c0d806000003)。
[Boostrap v4](https://github.com/twbs/bootstrap/tree/v4-dev/scss)源码使用scss书写

# JavaScript

使用[JavaScript Standard Style（代码规范）](https://github.com/feross/standard/blob/master/docs/README-zhcn.md)和
[JSDoc（注释规范）](http://usejsdoc.org/about-getting-started.html)

## JavaScript Standard Style

阅读上述链接的时候可以忽略提到的检查工具

写代码的时候严格遵循[细则](https://github.com/feross/standard/blob/master/docs/README-zhcn.md#细则)，
一共就10点，很好学会；一开始可能会经常按着自己以前的风格写，慢慢注意就会完全改正过来，
因为你会发现这种风格写出来是最优雅的

示例： [express的代码](https://github.com/expressjs/body-parser/blob/master/index.js)
你会爱上这样的代码，你也能写出这样的代码

## JSDoc

一般分为两种注释：块状注释和行内注释

- 块状注释：用于文件顶头的功能、版权等说明；用函数定义说明

    ```
    /*!
     * Book component
     * Copyright(c) 2014-2015 Someone called God
     * MIT Licensed
     */

    'use strict'

    /**
     * Represents a book.
     * @constructor
     * @param {string} title - The title of the book.
     * @param {string} author - The author of the book.
     */

    function Book (title, author) {
    }
    ```
    注意：块状注释一般会上下各留一行空行，来保持美观

- 行内注释：用于注释代码逻辑中需要思考才明白过来的逻辑，加上注释读者就不需要用脑子去思考代码逻辑

   ```
   // get image url from then given string
   var reg = /<img\s*src=['"]([^<>'"]+)['"].*>/i;
   var str = 'Happy because you <img src="/path/to/smile.jpg" alt="smile" />';
   var url = str.match(reg)[1];
   ```


工具推荐：如果你使用webstorm，内置了JavaScript Standard Style风格，在函数定义的前面输入`/**`按回车会自动进入JSDoc定义的注释模式