# vue3-cli-bidding
## 利用vue-cli工具升级vue2到vue3
+ 1、确保vue-cli版本 >= 4.3.1
```
vue -V
```
+ 2、用vue-cli 创建项目
```
vue create vue3-cli-bidding
```
+ 3、升级vue版本
```
vue add vue-next
```
## vue3的正确使用姿势
+ 钩子函数
```
vue2                vs              vue3
beforeCreate                        setup
created                             setup
beforeMount                         onBeforeMount
mounted                             onMounted
beforeUpdate                        onBeforeUpdate
updated                             onUpdated
beforeDestroy                       onBeforeUnmount
destroyed                           onUnmount
errorCaptured                       onErrorCaptured
```
+ 函数式API
```
createApp
reactive        // 创建响应式数据对象：对象式
ref             // 创建响应式对象：基本数据类型装箱
toRefs          // 将响应式数据转换为单一响应式数据
isRef           // 判断某值是否是引用类型
computed        // 创建计算属性
watch           // 创建watch监听
watchEffect
```
## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
