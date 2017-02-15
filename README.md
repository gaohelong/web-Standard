------------------------------------------------------------
◆ JAVASCRIPT.
----------------
0、注.
    
    1)、所有方法细化成单独的function来处理.

1、命名法说明.

    1)、camel命名法, 例如：thisIsAnApple
    2)、pascal命名法, 例如：ThisIsAnApple
    3)、下划线命名法, 例如：this_is_an_apple
    4)、中划线命名法, 例如：this-is-an-apple

2、命名规定.

    1)、变量名：使用驼峰(camel)命名法
    2)、参数名：使用驼峰(camel)命名法
    3)、函数名：使用驼峰(camel)命名法
    4)、方法/属性：使用驼峰(camel)命名法
    5)、私有（保护）成员：必须以下划线_开头
    6)、常量名：必须使用全部大写的下划线命名法, 如IS_DEBUG_ENABLED
    7)、类名：必须使用pascal命名法
    8)、枚举名：必须使用pascal命名法
    9)、枚举的属性：必须使用全部大写的下划线命名法
    10)、命名空间：必须使用camel命名法

3、变量.

    1)、先定义后使用.
    2)、变量赋值统一使用单引号，这个根据赋值内容而定.

4、函数、方法.

    1)、对象中定义属性、方法时冒号后加一个空格, function()后加一个空格. 例如：
        var obj = {
            attr: {
                def: 'bd'
            },
            maxVal: function() {

            }
        };

    2)、对象的最后一个属性或方法后不加逗号.
        var obj = {
            attr: {
                def: 'bd',
                cnt: 9, // 结尾不加逗号.
            },
            maxVal: function() {

            }, // 结尾不加逗号.
        };

5、注释.

    1)、单行注释时//前、后各加一个空格分隔开. 例如：
        var str = ''; // 我是注视, 我前面有一个空格.

    2)、多行注视时也需要加一个空格分隔开. 例如：
        /* 我是多行注视 */
        /* 我
        是
        多
        行
        注
        视 */

6、语句.

    1)、语句必须以分号结尾.
    2)、if语句条件的前、后各加一个空格. 例如：
        if (a == 1) {

        }
    3)、三目运算符最好不要嵌套使用会增加阅读难度可以使用if-else if-else代替.

7、其他.

    1)、缩进使用4个空格.
    2)、console.log()只能出现在调试代码中, 正式代码中去掉或者注释掉.
    3)、js使用空白类进行操作时需要加上js前缀, 例如：js-title。这些js开头的class不能写进css中.
    4)、叹号后面跟函数!function和加号后面跟函数+function 都是跟(function(){})();这个函数是一个意思, 都是告诉浏览器自动运行这个匿名函数的, 因为!+()这些符号的运算符是最高的, 所以会先运行它们后面的函数。

8、jQuery.

    1、jQuery绑定事件时先使用unbind（或off）解绑要绑定的所有事件, 然后在bind（或on）绑定要绑定的所有事件, 例如：
        $(".input").unbind('click').bind('click', function(){});
        $(".input").off('click').on('click', function(){});
    2、选择器的层级最好不要超过3级，一般就是1级就可以直接找到元素.
----------------
◆ HTML.
----------------
0、命名规范.

    1)、中划线命名法, 例如：this-is-an-apple

1、语法.

    1)、用四个空格来代替制表符（tab） -- 这是唯一能保证在所有环境下获得一致展现的方法。
    2)、嵌套元素应当缩进一次（即四个空格）。
    3)、对于属性的定义，确保全部使用双引号，绝不要使用单引号。
    4)、不要在自闭合（self-closing）元素的尾部添加斜线 -- HTML5 规范中明确说明这是可选的。
    5)、不要省略可选的结束标签（closing tag）（例如，</li> 或 </body>）。

2、HTML5 doctype.

    为每个 HTML 页面的第一行添加标准模式（standard mode）的声明，这样能够确保在每个浏览器中拥有一致的展现。
    <!DOCTYPE html>
    <html>
        <head>
        </head>
    </html>

3、语言属性.

    根据HTML5规范： 强烈建议为 html 根元素指定 lang 属性，从而为文档设置正确的语言。这将有助于语音合成工具确定其所应该采用的发音，有助于翻译工具确定其翻译时所应遵守的规则等等。
    <html lang="zh-cn">
        <!-- ... -->
    </html>

4、IE 兼容模式.

    IE 支持通过特定的 <meta> 标签来确定绘制当前页面所应该采用的 IE 版本。除非有强烈的特殊需求，否则最好是设置为 edge mode，从而通知 IE 采用其所支持的最新的模式。
    <meta http-equiv="X-UA-Compatible" content="IE=Edge">

5、字符编码.

    通过明确声明字符编码，能够确保浏览器快速并容易的判断页面内容的渲染方式。这样做的好处是，可以避免在 HTML 中使用字符实体标记（character entity），从而全部与文档编码一致（一般采用 UTF-8 编码）。
    <head>
        <meta charset="UTF-8">
    </head>

6、引入CSS和JavaScript文件.

    根据 HTML5 规范，在引入 CSS 和 JavaScript 文件时一般不需要指定 type 属性，因为 text/css 和 text/javascript 分别是它们的默认值。
    HTML5 spec links
    Using link
    Using style
    Using script

    <!-- External CSS -->
    <link rel="stylesheet" href="code-guide.css">

    <!-- In-document CSS -->
    <style>
      /* ... */
    </style>

    <!-- JavaScript -->
    <script src="code-guide.js"></script>

7、实用为王.

    尽量遵循 HTML 标准和语义，但是不要以牺牲实用性为代价。任何时候都要尽量使用最少的标签并保持最小的复杂度。

8、属性顺序

    HTML 属性应当按照以下给出的顺序依次排列，确保代码的易读性。
    class
    id, name
    data-*
    src, for, type, href, value
    title, alt
    role, aria-*
    class 用于标识高度可复用组件，因此应该排在首位。id 用于标识具体组件，应当谨慎使用（例如，页面内的书签），因此排在第二位。

    <a class="..." id="..." data-toggle="modal" href="#"> 1</a>
    <input class="form-control" type="text">
    <img src="..." alt="...">

9、减少标签的数量

    编写 HTML 代码时，尽量避免多余的父元素。很多时候，这需要迭代和重构来实现。请看下面的案例：
    <!-- Not so great -->
    <span class="avatar">
        <img src="...">
    </span>

    <!-- Better -->
    <img class="avatar" src="...">
----------------
◆ CSS.
----------------
0、命名规范.

    1)、中划线命名法, 例如：this-is-an-apple

1、语法.

    1)、用四个空格来代替制表符（tab） -- 这是唯一能保证在所有环境下获得一致展现的方法。
        .main {
            padding: 6px;
            font-size: 12px;
        }

    2)、为选择器分组时，将单独的选择器单独放在一行。
        .main { padding: 6px; }

    3)、为了代码的易读性，在每个声明块的左花括号前添加一个空格。
        .main { padding: 6px; }

    4)、声明块的右花括号应当单独成行。
        .main {
            padding: 6px;
            font-size: 12px;
        }

    5)、每条声明语句的: 后应该插入一个空格。
        .main { padding: 6px; }

    6)、为了获得更准确的错误报告，每条声明都应该独占一行。
        .main {
            padding: 6px;
            font-size: 12px;
        }

    7)、所有声明语句都应当以分号结尾。最后一条声明语句后面的分号是可选的，但是，如果省略这个分号，你的代码可能更易出错。

    8)、对于以逗号分隔的属性值，每个逗号后面都应该插入一个空格（例如，box-shadow）。
        .left, .right {
            padding: 6px;
            font-size: 12px;
        }

    9)、不要在 rgb()、rgba()、hsl()、hsla() 或 rect() 值的内部的逗号后面插入空格。这样利于从多个属性值（既加逗号也加空格）中区分多个颜色值（只加逗号，不加空格）。

    10)、对于属性值或颜色参数，省略小于 1 的小数前面的 0 （例如，.5 代替 0.5；-.5px 代替 -0.5px）。
        .main {
            padding: .6px;
            margin: .9px;
        }

    11)、十六进制值应该全部小写，例如，#fff。在扫描文档时，小写字符易于分辨，因为他们的形式更易于区分。

    12)、尽量使用简写形式的十六进制值，例如，用 #fff 代替 #ffffff。

    13)、为选择器中的属性添加双引号，例如，input[type="text"]。只有在某些情况下是可选的，但是，为了代码的一致性，建议都加上双引号。

    14)、避免为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;。
    ----------------
    /* Bad CSS */
    .selector, .selector-secondary, .selector[type=text] {
        padding:15px;
        margin:0px 0px 15px;
        background-color:rgba(0, 0, 0, 0.5);
        box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF
    }

    /* Good CSS */
    .selector,
    .selector-secondary,
    .selector[type="text"] {
        padding: 15px;
        margin-bottom: 15px;
        background-color: rgba(0,0,0,.5);
        box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
    }

2、声明顺序.

    相关的属性声明应当归为一组，并按照下面的顺序排列：
    Positioning：定位
    Box model：盒模型
    Typographic：排版
    Visual：视觉

    由于定位（positioning）可以从正常的文档流中移除元素，并且还能覆盖盒模型（box model）相关的样式，因此排在首位。盒模型排在第二位，因为它决定了组件的尺寸和位置。 其他属性只是影响组件的内部（inside）或者是不影响前两组属性，因此排在后面。完整的属性列表及其排列顺序请参考 Recess。

    .declaration-order {
        /* Positioning */
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        z-index: 100;

        /* Box-model */
        display: block;
        float: right;
        width: 100px;
        height: 100px;

        /* Typography */
        font: normal 13px "Helvetica Neue", sans-serif;
        line-height: 1.5;
        color: #333;
        text-align: center;

        /* Visual */
        background-color: #f5f5f5;
        border: 1px solid #e5e5e5;
        border-radius: 3px;

        /* Misc */
        opacity: 1;
    }

3、不要使用@import.

    与 <link> 标签相比，@import 指令要慢很多，不光增加了额外的请求次数，还会导致不可预料的问题。替代办法有以下几种：
    1)、使用多个 <link> 元素
    2)、通过 Sass 或 Less 类似的 CSS 预处理器将多个 CSS 文件编译为一个文件
    3)、通过 Rails、Jekyll 或其他系统中提供过 CSS 文件合并功能
    请参考 Steve Souders 的文章了解更多知识。

    <!-- Use link elements -->
    <link rel="stylesheet" href="core.css">

    <!-- Avoid @imports -->
    <style>
        @import url("more.css");
    </style>

4、媒体查询（Media query）的位置.

    将媒体查询放在尽可能相关规则的附近。不要将他们打包放在一个单一样式文件中或者放在文档底部。如果你把他们分开了，将来只会被大家遗忘。下面给出一个典型的实例。

    .element { ... }
    .element-avatar { ... }
    .element-selected { ... }

    @media (min-width: 480px) {
        .element { ...}
        .element-avatar { ... }
        .element-selected { ... }
    }

5、带前缀的属性.

    当使用特定厂商的带有前缀的属性时，通过缩进的方式，让每个属性的值在垂直方向对齐，这样便于多行编辑。

    /* Prefixed properties */
    .selector {
        -webkit-box-shadow: 0 1px 2px rgba(0,0,0,.15);
                box-shadow: 0 1px 2px rgba(0,0,0,.15);
    }

6、单行规则声明.

    对于只包含一条声明的样式，为了易读性和便于快速编辑，建议将语句放在同一行。对于带有多条声明的样式，还是应当将声明分为多行。
    这样做的关键因素是为了错误检测 -- 例如，CSS 校验器指出在 183 行有语法错误。如果是单行单条声明，你就不会忽略这个错误；如果是单行多条声明的话，你就要仔细分析避免漏掉错误了。

    /* Single declarations on one line */
    .span1 { width: 60px; }
    .span2 { width: 140px; }
    .span3 { width: 220px; }

    /* Multiple declarations, one per line */
    .sprite {
        display: inline-block;
        width: 16px;
        height: 15px;
        background-image: url(../img/sprite.png);
    }

7、简写形式的属性声明.

    在需要显示地设置所有值的情况下，应当尽量限制使用简写形式的属性声明。常见的滥用简写属性声明的情况如下：
    1)、padding
    2)、 margin
    3)、 font
    4)、 background
    5)、 border
    6)、 border-radius
    大部分情况下，我们不需要为简写形式的属性声明指定所有值。例如，HTML 的 heading 元素只需要设置上、下边距（margin）的值，因此，在必要的时候，只需覆盖这两个值就可以。过度使用简写形式的属性声明会导致代码混乱，并且会对属性值带来不必要的覆盖从而引起意外的副作用。

    在 MDN（Mozilla Developer Network）上一篇非常好的关于shorthand properties 的文章，对于不太熟悉简写属性声明及其行为的用户很有用。

    /* Bad example */
    .element {
        margin: 0 0 10px;
        background: red;
        background: url("image.jpg");
        border-radius: 3px 3px 0 0;
    }

    /* Good example */
    .element {
        margin-bottom: 10px;
        background-color: red;
        background-image: url("image.jpg");
        border-top-left-radius: 3px;
        border-top-right-radius: 3px;
    }

8、注释.

    代码是由人编写并维护的。请确保你的代码能够自描述、注释良好并且易于他人理解。好的代码注释能够传达上下文关系和代码目的。不要简单地重申组件或 class 名称。
    对于较长的注释，务必书写完整的句子；对于一般性注解，可以书写简洁的短语。

    /* Bad example */
    /* Modal header */
    .modal-header {
        ...
    }

    /* Good example */
    /* Wrapping element for .modal-title and .modal-close */
    .modal-header {
        ...
    }

9、class 命名.

    1)、class 名称中只能出现小写字符和破折号（dashe）（不是下划线，也不是驼峰命名法）。破折号应当用于相关 class 的命名（类似于命名空间）（例如，.btn 和 .btn-danger）。
    2)、避免过度任意的简写。.btn 代表 button，但是 .s 不能表达任何意思。
    3)、class 名称应当尽可能短，并且意义明确。
    4)、使用有意义的名称。使用有组织的或目的明确的名称，不要使用表现形式（presentational）的名称。
    5)、基于最近的父 class 或基本（base） class 作为新 class 的前缀。
    6)、使用 .js-* class 来标识行为（与样式相对），并且不要将这些 class 包含到 CSS 文件中。
    ----------------
    /* Bad example */
    .t { ... }
    .red { ... }
    .header { ... }

    /* Good example */
    .tweet { ... }
    .important { ... }
    .tweet-header { ... }
----------------
◆ 常用命名.
----------------
1.对于布局，即用.g-作为前缀，通常有以下推荐的写法。

    头部： header或head
    主体： body
    尾部：footer或foot
    主栏： main
    侧栏：side
    盒容器： wrap或box
    主栏子容器：mainc
    侧栏子容器：sidec

2.对于模块，即.m-作为前缀。元件，.u-作为前缀，通常有下面推荐的写法。

    导航： nav
    子导航：subnav
    菜单：menu
    选项卡：tab
    标题区：head或title
    内容区：body或content
    列表：list
    表格：table
    表单：form
    排行：top
    热点：hot
    登录：login
    标志：logo
    广告：adervertise
    搜索：search
    幻灯：slide
    帮助：help
    新闻：news
    下载：download
    注册：register或regist
    投票：vote
    版权:copyright
    结果：result
    按钮：button
    输入：input

3.对于功能，即以.f-为前缀，通常推荐如下：

    清除浮动：clearboth
    向左浮动：floatleft
    向右浮动: floatright
    溢出隐藏：overflowhidden

4.对于颜色，即以.s-为前缀，通常推荐如下：

    字体颜色：fontcolor
    背景：background
    背景颜色：backgroundcolor
    背景图片：backgroundimage
    背景定位：backgroundposition
    边框颜色：bordercolor

5.对于状态，即以.z-为前缀，通常推荐如下：

    选中: selected
    当前：current
    显示：show
    隐藏：hide
    打开：open
    关闭: close
    出错：error
    不可用:disabled
------------------------------------------------------------
