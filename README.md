# MeiTuan
仿美团WebApp。
### 架构
&ensp;&ensp;React + Router + Redux + KOA + Webpack
### 实现
前端：<br>
&ensp;&ensp;1.用 React 组件化实现界面。<br>
&ensp;&ensp;2.用 Router 配置 App 路由，使用 hashHistory,让 react-router 自己根据 url 去 render 相应的模块，不需要server端支持。<br>
&ensp;&ensp;3.用 Redux 存储用户信息，账户与所在地等。<br>
后端：<br>
&ensp;&ensp;用 KOA 框架搭建服务端，读取json数据，并暴露给前台。<br>
其他：<br>
&ensp;&ensp;引用了 react-swipe 插件，实现轮播图。<br>
### 难点
1.前台如何获取后端数据？<br>
&ensp;&ensp;fetch。<br>
2.获取数据时如何解决跨域问题？<br>
&ensp;&ensp;使用webpack-dev-server代理处理跨域，将前台向后端的请求都代理到后台端口3000上。<br>
3.实现下拉刷新时，滚屏scroll短时间内频繁触发的事件的性能优化？<br>
&ensp;&ensp;利用函数节流。<br>
4.智能组件和木偶组件？<br>
&ensp;&ensp;智能组件：涉及数据处理的组件。一般为页面。<br>
&ensp;&ensp;木偶组件：只用来显示的组件。<br>
5.约束性组件和非约束性组件？<br>
&ensp;&ensp;非约束性组件：事件驱动的组件。<br>
&ensp;&ensp;约束性组件：数据驱动的组件。<br>
### 运行
1.加载项目相关依赖。<br>
```javascript
npm install
```
2.启动后台<br>
```javascript
npm run mock
```
3.启动前台<br>
```javascript
npm start
```
### 项目截图
![首页](https://github.com/Best921/MeiTuan/blob/master/AppShowImg/首页.jpg)
![选择城市](https://github.com/Best921/MeiTuan/blob/master/AppShowImg/选择城市.jpg)
![登录](https://github.com/Best921/MeiTuan/blob/master/AppShowImg/登录.jpg)
![用户中心](https://github.com/Best921/MeiTuan/blob/master/AppShowImg/用户中心.jpg)
![商户详情](https://github.com/Best921/MeiTuan/blob/master/AppShowImg/商户详情.jpg)