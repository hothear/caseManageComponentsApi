# Widget容器组件

> 将信息聚合在卡片容器中展示。

**参数**

| 参数 | 说明 | 类型 | 默认值 |
| ---- | ---- | ---- | :----: |
| content-height | 内容区域的高度                       | Number |       - |
| content-style  | 内容区域的样式   | Object | {padding: '0 20px 8px 20px'} |
| empty-text     | 内容区域为空的默认文本               | String | 暂无内容 |
| float          | 卡片是否浮动显示                     | Boolean | false   |
| hide-title     | 是否隐藏标题区域                     | Boolean | false   |
| hide-border    | 是否隐藏卡片边框                     | Boolean | false   |
| hide-BoxShadow | 是否隐藏卡片阴影                     | Boolean | false   |
| margin         | 卡片的margin（规则同css）            | Array     | [8]   |
| title          | 标题文本                             | String    | -     |
| title-height   | 标题区域高度                         | Number    | 40    |
| width          | 卡片的宽度（例如可传入50%或50）      | String, Number | - |

**关于Slot**

* 标题插槽

```
<widget>
    <div slot="header">通过“slot="header"”导入</div>
</widget>
```

* 内容插槽

```
<widget>
    <div>我是内容，不需要指定slot</div>
</widget>
```

**案例**

> ![](http://7xkvpt.com1.z0.glb.clouddn.com/widget.png)