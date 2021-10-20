# Vue 轻量级后台管理系统基础模板

> 参考`vue-element-admin`的实现思路

#### 标签栏

- 点击标签切换页面
- 刷新当前标签页
- 关闭其他标签/关闭所有标签

**注意：** 组件的名称和路由的名称一定要一致，例如 `Home.vue` 组件名称 `name: home`，则在路由文件中也要给它设置为 `name: home`，否则页面内容不能缓存

```js
// 在router文件中
{
    path: 'home',
    name: 'home',
    component: () => import('../views/Home.vue')
}

// 在Home.vue中
export default {
    name: 'home'
}
```

#### 侧边栏

- 伸展/收缩
- 页面宽度过小自动收缩
- 多级菜单（利用 iView 组件）

#### 用户相关

- 消息通知
- 用户头像
- 基本资料

#### 动态菜单栏

- 根据数据动态生成菜单
- 在菜单项上添加`hidden`属性可以隐藏该菜单项，但还是可以正常访问页面，具体请看 DEMO 及其相关代码

#### 页面标题 `document.title`

在 `src/utils/index` 下可设置默认的 `title`，在每个路由配置项上可设置对应的 `title`，具体示例请看代码

#### 其它

- 利用`axios`拦截器 实现了`ajax`请求前展示`loading` 请求结束关闭`loading`

`Index`组件一般情况下只需要传数据就行 其他不用关注

主要是为了实现动态菜单路由和相关（权限）的`Demo`
UI 库使用的是`iView` 有大量的组件可用

### 使用

#### 安装依赖

```
npm i
```

#### 开发

```
npm run serve
```

#### 打包

```
npm run build
```
