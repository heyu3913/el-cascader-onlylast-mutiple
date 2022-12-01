## 背景：

### 我们经常级联合选择器多选的需求，但是element UI提供的级联选择器并不能只多选最后一级，所以我考虑基于element UI的级联选择器优化一下，实现可以多选最后一级，并且尽量可以保留级联选择器原有功能。

##DEMO地址：
https://heyu3913.github.io/el-cascader-onlylast-mutiple/dist/index.html

## 使用方法：

```javascript
  下载依赖
  npm i el-cascader-onlylast-mutiple -S
  引入依赖
  import Cascader from  'el-cascader-onlylast-mutiple'
  使用依赖 具体可看本项目中App.vue
   <Cascader></Cascader>
```

#### 参数：

| 参数    | 说明 | 类型 | 可选值 |  默认值 |
| ------ | ------ | ------ |  ------ |  ------ |
| visibleData | 选中项绑定值     | array | - | -
| options | 可选项数据源，键名可通过 Props 属性配置 | array |
| size | 尺寸 | string | medium / small / mini |
| placeholder | 输入框占位文本| string | -|请选择
| disabled | 是否禁用 | boolean | - | false |
| clearable | 是否支持清空选项     | boolean | - | false |
| collapseTags | 多选模式下是否折叠Tag     | boolean | - | false |
| popperClass | 自定义浮层类名     | string | - | - |
| props | 配置选项，具体见下表     | object | - | - |

#### props配置选项

| 参数|    说明|    类型|    可选值|    默认值
| ------ | ------ | ------ |  ------ |  ------ |
| expandTrigger|    次级菜单的展开方式    | string    | click / hover    | 'click'| 
| value    | 指定选项的值为选项对象的某个属性值    | string|    —    | 'value'
| label    | 指定选项标签为选项对象的某个属性值    | string|    —    | 'label'
|children |指定选项的子选项为选项对象的某个属性值|    string    |—    |'children'
|disabled    |指定选项的禁用为选项对象的某个属性值    |string|    —    |'disabled'

#### 事件：

| 事件名称    | 说明 | 回调参数 | 
| ------ | ------ | ------ | 
| change    | 当选中节点变化时触发    | 选中节点的值| 

### tips:

目前只兼容了以上属性与方法，别的element中原有的方法并没有测试过，可能会出现意想不到的错误。如果有需求可以联系我 vx: iverson96i


