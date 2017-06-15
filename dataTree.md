# DataTree组件

> 用清晰的层级结构展示信息，可展开或折叠。

**参数**

| 参数 | 说明 | 类型 | 默认值 |
| ---- | ---- | ---- | :----: |
| data           | 展示数据                             | Array  |       [] |
|current-node-key| 当前选中节点的 key，只写属性         | String, Number |- |
| empty-text     | 展示数据为空的默认文本               | String | 暂无数据 |
| expand-all     | 是否默认展开所有节点                 | Boolean | false   |
| expand-keys    | 默认展开的节点的 key 的数组          | Array   |    []   |
| expand-on-click-node    | 是否在点击节点的时候展开或者收缩节点， 默认值为 true，如果为 false，则只有点箭头图标的时候才会展开或者收缩节点        | Boolean | true   |
| hide-icon      | 是否隐藏所有节点图标                 | Boolean | false   |
| highlight-current | 是否高亮当前选中节点          | Boolean     | false   |
| icon-classnames   | 配置节点icon为图片方式            | Object   | {}     |
| indent   | 相邻级节点间的水平缩进，单位为像素         | Number    | 23    |

**props**

| 参数 | 说明 | 类型 | 默认值 |
| ---- | ---- | ---- | :----: |
| key      | 指定节点key为节点对象的某个属性值          | String  | id       |
| label    | 指定节点标签为节点对象的某个属性值         | String  | label    |
| children | 指定子树为节点对象的某个属性值             | String  | children |
| total    | 指定节点的数据记录数为节点对象的某个属性值（注意：不指定total属性，则不显示数据记录数目） | String  | total    |

**event**

| 事件名称 | 说明 | 回调参数 |
| ----     | ---- | ----     |
| node-click      | 节点被点击时的触发的事件    | 两个参数，依次是节点数据和event对象 |
| node-expand     | 节点被展开时触发的事件      | 两个参数，依次是节点数据和event对象 |
| node-collapse   | 节点被关闭时触发的事件      | 两个参数，依次是节点数据和event对象 |

**关于icon-classnames**
```
// template
<case-judgment-tree :data="treeData" :icon-classnames="iconClassnames"></case-judgment-tree>
```

```
// script
// 其中1和2为数据中的key(也可以为string类型)， 'ico-all'为classname
data() {
    return {
        iconClassnames: {
            1: 'ico-all',
            2: 'ico-tool'
        }
    };
}
```

```
//style
.tree-tag {
    .ico-all {
        background-image: url(...);
    }
    .ico-tool {
        background-image: url(...);
    }
    &:hover,
    &.current {
        .ico-all {
            background-image: url(...);
        }
        .ico-tool {
            background-image: url(...);
        }
    }
}
```
---
**未设置的节点以字体图标形式展示**
> ![image-icon-tree](http://7xkvpt.com1.z0.glb.clouddn.com/icon-tree.png)

**不传值或者值为空对象，则以默认形式显示**
> ![default-tree](http://7xkvpt.com1.z0.glb.clouddn.com/tree.png)
