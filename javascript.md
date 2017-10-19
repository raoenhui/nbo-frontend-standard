
# Javascript编码

[1 前端JavaScript书写规范](#user-content-1)

[2 前端开发环境配置](#user-content-2)

[3 路由配置](#user-content-3)

[4 组件编写](#user-content-4)


## <span id="user-content-1">1 前端JavaScript书写规范</span>

JavaScript在各行各业都有着广泛的应用，JavaScript代码风格形成了一定的规范，本项目直接就参考阿里的js规范，不依次列举了。
[前端JavaScript规范]  <https://yq.aliyun.com/articles/51488>


##<span id="user-content-2">2 前端开发环境配置</span>

##### proxyAry表示需要代理的url前缀。
##### envs中设为active的则为开发环境。
示例：
```javascript
/*需要代理url*/
var proxyAry=['/verfyCode','/login','/logout','/security']

/*环境列表*/
var envs = [

  // 本地环境
  {
    // active: true,
    one: 'http://localhost:8080'
  },
  // 测试环境on3
  {
    // active: true,
    one: 'http://www.one3.newtouch.com'
  },
  // 测试环境on2
  {
    active: true,
    one: 'http://api.one2.newtouch.com'
  }
];
```
##<span id="user-content-3">3 路由配置</span>

##### e导入需要的组件，添加路由路径。
示例：
```javascript
import Project from 'src/components/platform/Project';

export default new Router({
  routes: [
     {
      path: '/project',
      name: 'project',
      component: Project
    }]
 })
``````
##<span id="user-content-4">4 组件编写</span>

##### 添加基础代码，取唯一标识的name方便调试。
示例：
```vue
<template>
  <div class="project">
       project
  </div>
</template>
<script>
  export default {
    name: 'project',
    data () {
      return {
      }
    },
    methods: {
    }
  }
</script>
<style lang="scss" scoped>
</style>
```