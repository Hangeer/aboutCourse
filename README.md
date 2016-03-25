#### 上课准备

+   想一想讲点啥先
    
    +   作业评讲
        
        +   先看看效果,是不是都用了事件委托啥的,用 for 的有没有遇到闭包问题
        +   event window.event 是啥,window.event.target 是啥
        +   布局的时候简单讲一下 flex?
        +   能不能将 click 事件变成其他事件?鼠标悬停啊鼠标离开啥的
        
    +   问一下, 事件还需不需要讲
        
        +   如果要讲的话讲讲事件流,冒泡,捕获,默认事件的解绑 on 和 事件监听的区别
        +   原型懂没有 = = prototype 和 constructor 还需要讲不
    
    +   切图的 bfc（细讲）
        +   其实这个概念不是第一次接触了（上学期应该是讲过的,但是理解了吗?）
        +   block formating context
            +   block 块级元素（块级元素有哪些?块级元素的特点?）特点:默认不加修饰的情况下块级元素并不会收缩包裹其内容,其宽度会充斥父元素,高度由自身撑开.块级元素即使设置了宽度,不占满父级元素,自己也会占满一行,不让其后元素与自己并行
            +   formating context 格式化上下文,拥有一套渲染规则,对内来约束其内块级元素的布局,对外控制外部元素布局
            +   注意:触发 bfc 之后并不是使得非块级元素像块级元素一样布局,但确实会给触发 bfc 区域的元素带来这样的副作用.为触发 bfc 的元素定制一套约束其内块级盒子布局与对外部元素布局的影响,并不是改变自己的 display 模式
        +   bfc 渲染规则
            +   内部的块级 box 会在垂直方向,一个接一个放置
            +   每个元素的 margin box 的左边,与包含块的左边相接触,即使存在浮动也是如此
            +   box 垂直方向由 margin 决定属于同一个 bfc 的两个相邻的 box 的 margin 会发生重叠
            +   bfc 的区域不会与 float box 发生重叠
            +   bfc 也边上的一个独立容器,容器里面的子元素不会影响到外面的元素,反之也如此
            +   计算 bfc 的高度的时候,浮动元素也参与计算
        +   触发 bfc 的条件
            +   根元素（html）
                +   html 文档建立,就会触发跟元素的 bfc ,根元素内写几个 div 元素,会发现内部 div 垂直排列,本身没有兄弟元素,所以相邻 margin 会重叠
            +   float 属性不为 none
                +   当一个元素被设置为 float: left || right 会触发这个元素,生成 bfc 区域,使他不仅有 bfc 的渲染规则,而且会给自身带来副作用
            +   position 为 abs 或 fixed 
            +   display 为 inline-block table-cell
            +   overflow 不为 visible 
                +   overflow: hidden 通常是对父元素比较有效的
        +   bfc (Block formatting context) 块级格式化上下文,是一个独立渲染区域,只需要考虑内部的元素如何布局
            +   应用: 自适应两栏布局
            +   清除内部浮动
            +   防止 margin 重叠
        +   切图的时候不要写得太死,仅仅为了还原页面是不好的,还要考虑后端的感受,以及在动态生成一些 DOM 的时候怎么做更方便
    
    +   一些 js 函数啊方法啥的加深熟悉
        +   做点简单的题提升下兴趣？（codewars）
            Array.prototype.*
            String.prototype.*
            通过这个讲下返回值, arguments对象, 回调函数, 通过 call 改变上下文的使用,是如何改变的
            bind 方法
            bind 和 call apply 的不同
                +   返回值
                +   传空值的时候
                +   应用情景
            <!--currying 柯里化-->