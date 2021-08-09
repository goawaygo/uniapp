### 介绍
> 基于uni-app，colorUI，封装了《自定义TabBar》《上传图片》《全局自定义loading》等功能 主要适配 微信小程序、APP、H5。

#### 第一步 npm install 

#### 全局自定义loading

```
	// 已在 main.js 注册全局组件，在每个页面中 添加<cu-loading>即可 页面中添加即可，其他组件无需添加。（页面就是在pages.json 中注册了的）

	<cu-loading></cu-loading>
	// 具体
	// 是否显示 半透明背景
	// 是否点击 半透明背景 关闭loading
	// 在 /components/loading/loading.vue 中自行修改
	
```

#### 自定义TabBar
- 这次做成了引入外部配置文件  uni-setting.json 请求在 App.vue 中的 onLaunch 里  H5注意需要服务端允许跨域
- 几乎所有配置及数据 也在 vuex中统一管理 /store/index.js
- 注意：tabbar 所能切换的页面 必须以组件的形式 已经加载进 home.vue（根页面）。
- 详见 示例代码
#### 上传图片
- 普通上传文件直接通过 官方的API 上传到业务服务器 ，我就没写。
- 上传至七牛云存储 （支持 微信小程序 APP H5 其他未测，未兼容 ）
- 上传至阿里OSS （阿里OSS不支持直接上传base64）

#### 主题色
- 项目用到颜色的地方全部使用 vuex 中的 配置数据。
- 开发注意写法  有一键切换主题色的需求可以试试



