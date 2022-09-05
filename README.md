uniapp 移动端悬浮按钮组件,扇形展开关闭，触摸移动可控制，展开可控制，图标可自定义

Props

| 参数名 |类型  |默认值  | 说明
| --- | --- | --- | --- |
|top | String, Number  | '70%' |组件距离窗口顶部距离，支持百分比，数字，数字带单位，例如10%或30或'30px'，默认单位rpx  |
| left| String, Number |  '85%'|组件距离窗口左边距离，支持百分比，数字，数字带单位，默认单位 |
| size| String, Number |80  |悬浮按钮尺寸（长==宽），默认单位rpx  |
|bgColor| String | rgb(235, 155, 50)| 悬浮按钮底板背景色 |
| move| Boolean| true|按钮是否可移动，false:禁止移动固定位置  |
| turn| Boolean| true |点击中心按钮是否展开扇形子菜单，false:禁止展开  |
| opacity| Number |0.8  |中心按钮透明度 |
| centerIcon| String | |中心按钮图标链接，本地图片或网络url  |
| topIcon| String | |扇形菜单上方按钮图标链接  |
| leftIcon| String | |扇形菜单左边按钮图标链接  |
| bottomIcon| String | |扇形菜单底部按钮图标链接  |
| iconSize| Number, String |‘100%’ |悬浮按钮图标尺寸，支持百分比，数字，数字带单位，默认单位rpx  |
| zindex| Number |999|组件显示层级 |


Event

| 事件名 |作用  |
| --- | --- |
| @close |关闭扇形悬浮按钮触发  
| @open | 打开扇形悬浮按钮 触发 |
| @click | 禁止展开扇形菜单情况下点击中心按钮触发 |
| @top| 点击 扇形菜单上方按钮触发 |
|@left | 点击 扇形菜单左边按钮触发 |
|@bottom | 点击 扇形菜单底部按钮触发 |




Slot
| name |说明  |
| --- | --- |
| center |中心按钮内容
| top| 上方按钮内容 |
| left |左边按钮内容 |
| bottom| 底部按钮内容 |




示例 1、默认样式

```html
<suspenButton></suspenButton>
```

2.禁止展开

```html
 <suspenButton top="10%" size="100" :turn="false">
    <view slot="center">到顶部</view>
</suspenButton>
```
3.禁止移动

```html
<suspenButton bgColor="red" top="80%" left="50" size="90" :move="false" >
    <view slot="center">移不动</view>
</suspenButton>
```
4.自定义图标

```html
<suspenButton top="50%" left="40%" topIcon="/static/logo.png">
</suspenButton>
```

