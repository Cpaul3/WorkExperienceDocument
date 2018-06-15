# WorkExperienceDocument
工作经验文档

gitHub反应太慢

艺术字体在线生成器：http://www.qt86.com/

各种插件npm搜索并下载地址：https://www.npmjs.com/

ES6学习地址：http://es6.ruanyifeng.com/

ES6箭头函数：https://segmentfault.com/p/1210000009243551/read

Flexbox布局：https://blog.csdn.net/hai_qing_xu_kong/article/details/72672404

如何利用 Chrome 浏览器实现滚动截屏?https://www.imooc.com/article/30185

React组件生命周期详解：https://juejin.im/post/5b077f04f265da0dc073caa6?utm_medium=hao.caibaojian.com&utm_source=hao.caibaojian.com

三元运算符： x ? : y 相当于 x ? x : y 判断x是否有值

经常用windows的dos命令行，下面我将列举常用命令行
    
    where node ->查看node的安装位置
    D: -> 切换到D盘
    dir -> 查看d盘下所有目录
    cd A -> 切换到d盘的A文件夹下

win10安装node等msi软件时报2503,2502错误，怎么解决？
选中win键,单击鼠标右键,选中“命令提示符（管理员）”，在dos命令行中键入“msiexec /package msi文件路径”，如“msiexec /package D:\00\NodeJS\node-v10.3.0-x64.msi”

clearTimeout：一直觉得没必要用这个，反正一次执行就失效了嘛，但是在使用setTimeout时和setInterval一样，也要clear,假如有个函数一开始想要在30秒后执行，然后，在还没有30秒的时候，由于用户做了其他操作，需要取消那个30秒后的操作，你怎么办？当然是清掉她啊，所以clearTimeout不是必须的，但却是安全保障。当然比如0秒后执行，clear就没必要了

如何判断两个数组是否相等？直接===是不行的,用(JSON.stringify(arr1) == JSON.stringify(arr2))或者（arr1.sort().toString() === arr2.sort().toString()）来判断

一、angular重要知识：文档：http://docs.ngnice.com/guide/scope


angular的Directive指令详解：https://juejin.im/post/5b06a73cf265da0de34fa506

    &可以从指令内部controller触发外部controller,但是不能通过他从外部不能触发内部函数，
    此时=就派上用场了,=可以双向传递字符串，参数，和方法;
    @：只能单向传递字符串，从外部向指令内部传递字符串;
    &、@ -> 是单向绑定，&从里到外，@从外到里;
    =  -> 是双向绑定，双向传递;


angular遍历map：ng-repeat = "(key,value) in dataList"

简谈angular的双向绑定机制:脏检查

angular的$eval：$eval是为了让$parse在scope中使用更方便的语法糖

谈谈对angular中的$parse的理解-以demo为例 参考链接：https://www.cnblogs.com/HeJason/p/5493357.html
    $parse 服务 该服务即可用来根据作用域计算AngularJS表达式的值,又可以在某个作用域上设置值,
    
    
    var obj = {user:{name:'angular1'}};
    
    //如何获取obj对象中的'angular1'?
    //方法一、（低级用法）
    console.log(obj.user.name);//angular1
    //方法二、（高级用法）
    var getter = $parse('user.name');
    var a = getter(obj);
    console.log(a);//angular1


    //如何改变obj对象中的'angular1'为'jquery'?

    //方法一、（低级用法）
    obj.user.name = 'jquery';
    console.log(obj.user.name);//jquery
    //方法二、（高级用法）
    var setter = $parse('user.name').assign;
    var b = setter(obj,'jquery');
    console.log(b);//jquery


    //替换功能
    var obj2 = {user:{name:'local'}};

    var getter2 = $parse('user.name');
    var c = getter2(obj,obj2);
    console.log(c);//local
    
谈谈angularjs的$compile用法，参考链接：https://blog.csdn.net/bluesheaven/article/details/53729694

    //angular中的$compile 作用：解析一段html代码，将死模板变成活模板
    $scope.vo.myName = 'zxj';
    // 创建编译函数
    var compileFn = $compile('<div>{{vo.name}}</div>');
    // 传入scope，得到编译好的dom对象(已封装为jqlite对象)
    // 也可以用$scope.$new()创建继承的作用域
    var $dom = compileFn($scope);
    // 添加到文档中
    $dom.appendTo('body');
    
    
    
    
    
微信小程序：
微信小程序做到后面时，功能越来越多，页面越来越复杂，此时，不免会用到自定义组件，提取公用的代码出来，此时，可能涉及到父子组件之间的一些事件交互
组件之间的通信：https://developers.weixin.qq.com/miniprogram/dev/framework/custom-component/events.html
    
