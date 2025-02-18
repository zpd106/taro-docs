---
title: PageMeta
sidebar_label: PageMeta
---

:::info
在 Taro 中使用此组件，需要配合 [tarojs-plugin-platform-miniprogram 插件](https://github.com/baranwang/tarojs-plugin-platform-miniprogram)。
相关讨论：[#6092](https://github.com/NervJS/taro/issues/6092)
:::

页面属性配置节点，用于指定页面的一些属性、监听页面事件。只能是页面内的第一个节点。可以配合 navigation-bar 组件一同使用。
通过这个节点可以获得类似于调用 Taro.setBackgroundTextStyle Taro.setBackgroundColor 等接口调用的效果。

支持情况：<img title="微信小程序" src={require('@site/static/img/platform/weapp.png').default} className="icon_platform" width="25px"/> <img title="H5" src={require('@site/static/img/platform/h5.png').default} className="icon_platform icon_platform--not-support" width="25px"/> <img title="React Native" src={require('@site/static/img/platform/rn.png').default} className="icon_platform icon_platform--not-support" width="25px"/> <img title="Harmony" src={require('@site/static/img/platform/harmony.png').default} className="icon_platform icon_platform--not-support" width="25px"/>

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/component/page-meta.html)

## 类型

```tsx
ComponentType<PageMetaProps>
```

## PageMetaProps

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | :---: | :---: | --- |
| backgroundTextStyle | `string` |  | 否 | 下拉背景字体、loading 图的样式，仅支持 dark 和 light |
| backgroundColor | `string` |  | 否 | 窗口的背景色，必须为十六进制颜色值 |
| backgroundColorTop | `string` |  | 否 | 顶部窗口的背景色，必须为十六进制颜色值，仅 iOS 支持 |
| backgroundColorBottom | `string` |  | 否 | 底部窗口的背景色，必须为十六进制颜色值，仅 iOS 支持 |
| scrollTop | `string` | `""` | 否 | 滚动位置，可以使用 px 或者 rpx 为单位，在被设置时，页面会滚动到对应位置 |
| scrollDuration | `number` | `300` | 否 | 滚动动画时长 |
| pageStyle | `string` | `""` | 否 | 页面根节点样式，页面根节点是所有页面节点的祖先节点，相当于 HTML 中的 body 节点 |
| rootFontSize | `string` | `""` | 否 | 页面的根字体大小，页面中的所有 rem 单位，将使用这个字体大小作为参考值，即 1rem 等于这个字体大小 |
| onResize | `CommonEventFunction<onResizeEventDetail>` |  | 否 | 页面尺寸变化时会触发 resize 事件 |
| onScroll | `CommonEventFunction<onScrollEventDetail>` |  | 否 | 页面滚动时会触发 scroll 事件 |
| onScrollDone | `CommonEventFunction` |  | 否 | 如果通过改变 scroll-top 属性来使页面滚动，页面滚动结束后会触发 scrolldone 事件 |
| rootBackgroundColor | `string` |  | 否 | 页面内容的背景色，用于页面中的空白部分和页面大小变化 resize 动画期间的临时空闲区域 |
| pageFontSize | `string` |  | 否 | 页面 page 的字体大小，可以设置为 system ，表示使用当前用户设置的微信字体大小 |
| pageOrientation | `string` |  | 否 | 页面的方向，可为 auto portrait 或 landscape |

### API 支持度

| API | 微信小程序 | 支付宝小程序 | H5 | React Native | Harmony |
| :---: | :---: | :---: | :---: | :---: | :---: |
| PageMetaProps.backgroundTextStyle | ✔️ |  |  |  |  |
| PageMetaProps.backgroundColor | ✔️ | ✔️ |  |  |  |
| PageMetaProps.backgroundColorTop | ✔️ | ✔️ |  |  |  |
| PageMetaProps.backgroundColorBottom | ✔️ | ✔️ |  |  |  |
| PageMetaProps.scrollTop | ✔️ | ✔️ |  |  |  |
| PageMetaProps.scrollDuration | ✔️ | ✔️ |  |  |  |
| PageMetaProps.pageStyle | ✔️ | ✔️ |  |  |  |
| PageMetaProps.rootFontSize | ✔️ | ✔️ |  |  |  |
| PageMetaProps.onResize | ✔️ |  |  |  |  |
| PageMetaProps.onScroll | ✔️ | ✔️ |  |  |  |
| PageMetaProps.onScrollDone | ✔️ |  |  |  |  |
| PageMetaProps.rootBackgroundColor | ✔️ | ✔️ |  |  |  |
| PageMetaProps.pageFontSize | ✔️ | ✔️ |  |  |  |
| PageMetaProps.pageOrientation | ✔️ |  |  |  |  |

### onResizeEventDetail

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| size | `resizeType` | 窗口尺寸 |

### resizeType

窗口尺寸类型

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| windowWidth | `number` | 窗口宽度 |
| windowHeight | `number` | 窗口高度 |

### onScrollEventDetail

| 参数 | 类型 |
| --- | --- |
| scrollTop | `number` |
