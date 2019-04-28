# html-module
常见HTML模块
## <a href="https://github.com/daifuyang/html-module/tree/master/history">html-history</a>
浏览器返回上一页保持页面数据不变</br>
#### 问题描述
我们在的列表页通常是异步获取的。当我们手动翻了好几页之后，点到详情页面里面去在返回列表页后整个页面就被刷新了。
这样用户就又需要重新从头开始选择。造成的用户体验非常不友好！
#### 解决思路
通过相关的资料和思路分析，决定利用sessionStorage来解决此问题。
+ 第一步：获取页面的滚动高度 scrollTop并保存在sessionStorage
+ 第二步：保存分页的总数据和分页页数同样保存在sessionStorage
+ 第三步：初始化页面获取数据。如果页面存在缓存数据直接赋值缓存数据。
