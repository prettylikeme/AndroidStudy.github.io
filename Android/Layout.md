# Android中的几大布局管理器

> 注意：
> - 一个`XML`布局文件中最多只能有一个根布局管理器
> - 根布局管理器必须包含`xmlns`属性
> - 布局管理器不要嵌套太深，容易影响性能

## RelativeLayout

相对布局管理器

#### 布局管理器属性

- `gravity`：设置布局管理器中各子组件的摆放方式，可为多个值，使用`|`分隔
- `ignoreGravity`：指定哪个组件不受`gravity`影响

#### `RelativeLayout.LayoutParams`设置在布局管理器内的组件属性中

- 设置组件位于指定组件的对应方位
    - `layout_above`
    - `layout_below`
    - `layout_toLeftOf`
    - `layout_toRightOf`
- 设置组件与布局管理器对应的边对齐
    - `layout_alignParentBottom`
    - `layout_alignParentLeft`
    - `layout_alignParentRight`
    - `layout_alignParentTop`
- 设置组件与指定组件对应的边界的对齐方式
    - `layout_alignBottom`
    - `layout_alignLeft`
    - `layout_alignRight`
    - `layout_alignTop`
- 设置组件位于布局管理器中的位置
    - `layout_centerHorizontal`
    - `layout_centerInParent`
    - `layout_centerVertical`

## LinearLayout

线性布局管理器——将组件按水平或垂直方向一一排列

#### 布局管理器属性

- `orientation`
    - 垂直线性布局管理器：`vertical`
    - 水平线性布局管理器：`horizontal`
- `gravity`：同相对布局管理器

#### 子组件属性

- `layout_weight`：分配剩余空间，而不是整个空间

## FrameLayout

帧布局管理器

## TableLayout

表格布局管理器

#### 布局管理器属性

- `collapseColumns`：指定的列将被隐藏，从`0`开始计数，使用`,`分隔
- `stretchColumns`：指定的列将被拉伸，从`0`开始计数，使用`,`分隔
- `shrinkColumns`：指定的列将被收缩，从`0`开始计数，使用`,`分隔

#### 表格行

- 使用`TableRow`来添加行，每个组件占一列，没有表格列属性
- 与`TableRow`同级的组件将占一行

## GridLayout

网格布局管理器

#### 布局管理器属性

- `columnCoount`：指定网格的最大列数
- `orientation`：当子组件没有设置行或列属性时，其位置摆放方式，同`LinearLayout`
- `rowCount`：指定网格的最大行数

#### `GridLayout.LayoutParams`设置在布局管理器内的组件属性中

- `layout_column`：设置子组件的列
- `layout_columnSpan`：设置子组件跨越列的数量
- `layout_columnWeight`：设置子组件分配水平剩余空间的占比
- `layout_gravity`：设置子组件在网格中的摆放位置
- `layout_row`：设置子组件的行
- `layout_rowSpan`：设置子组件跨越行的数量
- `layout_rowWeight`：设置子组件分配垂直剩余空间的占比

## TableLayout与GridLayout对比

1. 在`TableLayout`中只能实现跨列显示；而在`GridLayout`中既能跨列，也能跨行
1. 在`TableLayout`中超出屏幕显示范围的组件将不会显示；而在`GridLayout`中超出的组件将会自动换行

## AbsoluteLayout

绝对布局管理器（已弃用）