楼主身为一个非计算机专业的大四学生,目前在学校附近的公司实习,利用工作之余做的第一个redux项目,也是刚刚接触redux 1个月,从最开始的看不懂到现在的能稍微写点东西出来了,希望各位大神觉得哪里做的不好,不足的地方,还请各位批评指正,非常感谢.同时也是求star!!!!
# 项目介绍
基于webpack + react + react-router + redux + less + ant + es6 的cnode社区
非常感谢cnode提供的api以及react china社区的各位大神,真的提供了很多的帮助,里面也有很多的例子,都值得去学习
## 运行项目（nodejs 6.0+）
```
  git clone https://github.com/zhangfan6644777/Redux-cnode.git
  cd Redux-cnode
  npm install 
  npm run dev (开发版本访问：http://localhost:8088/)
```

## 功能
```
  1.登录退出
  2.列表分页，下拉自动加载
  3.发帖，回复帖子,点赞
  4.查看消息
  5.个人中心
  6.查看别人的资料
```
## 项目总结

1.```基本思路```就是每个页面对应一个reducer

- ```Topic```主要是主页的列表信息,上拉加载
- ```Article```对应文章内容页面,点赞,评论,关注的逻辑都在这里
- ```PublishTopic```对应发布文章页面,
- ```Message```对应账号的消息页面,包括已读消息和未读消息
- ```Login```对应账号的登录信息
- ```UserInfo```个人信息,还有发布,收藏,参与的话题
- ```OtherInfo```对应账号的信息,还有发布,收藏,参与的话题

2.代码结构我是模仿[实例讲解基于 React+Redux 的前端开发流程](https://segmentfault.com/a/1190000005356568)去构建的,他的这篇文章我觉得写得非常好,通俗易懂.尤其是对于我这样的小白来说,代码的结构也很容易理解,非常感谢这篇文章带我入门redux,然后这个是我根据这个文章写的demo [Redux-PickApple](https://github.com/zhangfan6644777/Redux-PickApple),欢迎star!!

3.引用了蚂蚁金服的移动端Antd,样式挺好看的,不用再自己造轮子,ui一部分是模仿[大神的cnode](http://react-china.org/t/webpack-react-react-router-redux-less-flex-css-es6-react-cnode/6332)去做的

4.redux听起来确实很高大上,主要是对我开发思维的一个改变,但是有时候我觉得实施起来确实有点复杂,可能是我刚接触redux,还不是特别理解。

5.react配合redux非常需要注意性能，一定要尽可能减少渲染的次数,逻辑处理的不好,会导致多次的渲染,所以要好好利用shouldComponentUpdate来提升性能(需要改进的地方)

6.对react有了进一步的了解

- setState()是异步的 this.setState()会调用render方法，但并不会立即改变state的值，state是在render方法中赋值的。所以执行this.setState()后立即获取state的值是不变的。同样的直接赋值state并不会出发更新，因为没有调用render函数。
- 在组件里面最好不要写自己的state,应该放在根state统一进行管理,但是有些时候我觉得放在本身组件内代码写着会简单一点(TTTTTTTTTTTT)。

7.react-router

- 可以使用下面代码优雅的传递复杂的参数

  ```
  <Link to={{pathname:link,state:data}}>
  ```

8.对es6有了进一步的了解,推荐阮大神的书籍[ECMAScript 6 入门](http://es6.ruanyifeng.com/) 

- class写法 如果使用es6的class类继承react的component组件，constructor中必须调用super，因为子类需要用super继承component的this，否则实例化的时候会报错。
- 方法要绑定bind(this)才可以使用,与es5的React.createClass不同,es5的方式是自动绑定到this上的。
- 其中箭头函数 扩展运算符和变量解构赋值真的帮助很大,极大的提升效率。

9.目前还没有解决的问题(正在改进中)

- 评论的时候滚动条
- 在消息页面点击被删除的帖子会出错
### 截图

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/1.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/2.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/3.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/4.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/5.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/6.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/7.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/8.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/9.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/10.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/11.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/12.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/13.png)

![截图](https://github.com/zhangfan6644777/Redux-cnode/blob/master/show/14.png)

