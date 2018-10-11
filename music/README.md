# music

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Mint Ui  vue移动框架

``` home.vue 导航
    引入 import { Navbar, TabItem } from 'mint-ui';

    写法：
        v-model="selected"
        value	返回当前选中的 tab-item 的 id
        改变 selected 的值，与 <tab-container-item> 的 id 一致即显示对应页面。

        在data中写入
            data(){
                return{
                    selected:"tab-item 的 id"
                }
            };


 ## 引入less
    1.安装less依赖
       npm install less less-loader --save

    2.修改webpack.base.conf.js文件
        配置loader加载依赖，让其支持外部的less,在原来的代码上添加

        {
        test: /\.less$/,
        loader: "style-loader!css-loader!less-loader",
        },

    3.使用less
        内部自己使用
        <style lang="less">
        .step-list {
                padding-top: 13px;
                li {
                    float: left;
                    .arrow-r {}
                }
        }
        </style>

        外部引入
          <style lang="less">
             @import './songList.less'
          </style>

