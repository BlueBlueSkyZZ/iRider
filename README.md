# iRider
## 项目说明
本系统基于phonegap(现依托于apache基金会，名为cordova)，进行移动Web APP开发。    

## 前端介绍
前端框架主要采用jQuery Mobile，页面简洁，但是缺点是响应速率较慢，进行JS加载时需要禁用jQuery Mobile自身的ajax请求来处理ajax跨域问题。  
jQuery Mobile的官网http://jquerymobile.com/   
引用代码    
`<link rel="stylesheet" href="js/jquery.mobile-1.4.5/jquery.mobile-1.4.5.min.css">`   
`<script type="text/javascript" src="js/jquery-1.12.0.min.js"></script>`   
`<script type="text/javascript" src="js/jquery.mobile-1.4.5/jquery.mobile-1.4.5.min.js"></script>`    
禁用自动ajax代码如下    
`$.mobile.ajaxEnabled = false;//取消jquerymobile的自动ajax请求`

## 功能介绍
此项目有地图、天气、相机、朋友圈、基础信息设置五大页面。

### 地图&天气
地图调用高德地图API，可以帮助规划骑行路线。    
天气同样使用高德地图API，可以查询精确到区的天气

### 相机
监听音量增、音量减键，直接打开相机或摄像。
音量增：直接打开相机，再次按下音量键即可拍照，并显示在APP前端。    
音量减：直接打开摄像机，再次按下音量键开始录像，第三次按下音量键停止录像。    

### 朋友圈
v1.0 处于未完成状态。    
仿微信朋友圈，图片通过插件可以进行放大操作

### 基础信息设置
显示用户名，用户基本信息，蓝牙设置和罗盘。

## 安装方式
配置好cordova环境，输入以下命令     
安卓版：
`cordova run android`    
其他版本尚未添加组件

## 版本说明
### v1.0   
1.完成简单的前端页面（地图、天气、罗盘、相机等可以使用）。   
2.可以进行蓝牙扫描但连接出现问题，初步判断可能是API仅支持蓝牙4.0的原因。  
3.朋友圈与后台交互尚未完成。
