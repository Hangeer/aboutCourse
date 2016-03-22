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
    
    +   切图的 bfc
        +   bfc (Block formatting context) 块级格式化上下文,是一个独立渲染区域,只需要考虑内部的元素如何布局
            +   应用: 自适应两栏布局
            +   清除内部浮动
            +   防止 margin 重叠
    
    +   一些 js 函数啊方法啥的加深熟悉
        +   做点简单的题提升下兴趣？（codewars）
            Array.prototype.*
            String.prototype.*
            通过这个讲下返回值,arguments对象,回调函数,通过 call 改变上下文的使用,是如何改变的
            bind 方法
            bind 和 call apply 的不同
                +   返回值
                +   传空值的时候
                +   应用情景
            <!--currying 柯里化-->