# CSS

## 一、CSS 简介

### 1. 什么是 CSS
- **CSS**：Cascading Style Sheet，层叠样式表。
- **作用**：是一组样式设置规则，用于控制页面的外观和样式。

### 2. CSS 的作用
- 美化页面的外观。
- 用于布局和定位页面内容。

## 二、CSS 的基本用法

### 1. CSS 语法
```html
<head>
  <style type="text/css">
    选择器 {
      属性名: 属性值;
      属性名: 属性值;
    }
  </style>
</head>
```
- **选择器**：需要修饰的对象。
- **属性名**：需要修饰的样式属性。
- **属性值**：属性的取值。

### 2. CSS 的应用方式
CSS 有三种应用方式：**内部样式**、**行内样式** 和 **外部样式**。

#### 2.1 内部样式
- 通过 `<style>` 标签在页面头部定义。
- 适用于当前页面所有符合样式选择器的标签。

#### 2.2 行内样式
- 使用 HTML 标签的 `style` 属性定义。
- 仅对设置 `style` 属性的标签起作用。

#### 2.3 外部样式
- 使用单独的 `.css` 文件定义，在页面中通过 `<link>` 标签引入。
  ```html
  <link rel="stylesheet" href="css样式文件的路径">
  ```
- 适用于所有引入样式表文件的页面。

## 三、CSS 选择器

### 1. 基础选择器

#### 1.1 标签选择器
- 使用 HTML 标签作为选择器名称，例如 `p { color: red; }`。

#### 1.2 类选择器
- 以 `.` 作为前缀，自定义名称，通过 HTML 标签的 `class` 属性调用。
  ```css
  .classname { color: blue; }
  ```

#### 1.3 ID 选择器
- 以 `#` 作为前缀，自定义名称，通过 HTML 标签的 `id` 属性调用。
  ```css
  #idname { color: green; }
  ```

### 2. 复杂选择器

#### 2.1 复合选择器
- 组合标签选择器和类选择器或标签选择器和 ID 选择器，必须同时满足两个条件才能应用样式。

#### 2.2 组合选择器
- 使用逗号 `,` 将多个选择器组合，如 `.class1, .class2 { color: red; }`。

#### 2.3 嵌套选择器
- 在某个选择器内设置选择器，只有最里层选择器对应的标签才会应用样式。

#### 2.4 伪类选择器
- 根据状态不同应用不同样式，常用于 `a` 标签的四种状态：
  ```css
  a:link { color: blue; }
  a:visited { color: purple; }
  a:hover { color: red; }
  a:active { color: yellow; }
  ```

## 四、常用 CSS 属性

### 1. 字体属性
- 定义字体相关的样式，如 `font-size`、`font-weight`、`font-family`、`font-style` 等。

### 2. 文本属性
- 例如 `color`、`line-height`、`text-align`、`vertical-align`、`text-decoration` 等。

### 3. 背景属性

| 属性                  | 含义               | 取值说明                                            |
| --------------------- | ------------------ | --------------------------------------------------- |
| `background-color`    | 背景颜色           | 可以是英文单词、16 进制 RGB 值                      |
| `background-image`    | 背景图片           | 使用 `url(路径)`                                    |
| `background-repeat`   | 背景图片的重复方式 | `repeat`、`repeat-x`、`repeat-y`、`no-repeat`       |
| `background-position` | 背景图片的显示位置 | `top`、`bottom`、`left`、`right`、`center` 等关键字 |
| `background`          | 背景简写           | 按顺序：颜色、图片、重复方式、显示位置              |

### 4. 列表属性
- 使用 `list-style` 设置列表项前的标记。

### 5. 浮动属性
- 通过 `float` 实现元素浮动，取值：`left`、`right`、`none`。

### 6. 元素的显示和隐藏
- 使用 `display` 设置元素显示方式，常用取值：
  - `none`：不显示。
  - `inline`：将块级元素变为行级元素。
  - `block`：将行级元素变为块级元素。
  - `inline-block`：允许设置宽高。

## 五、盒子模型

### 1. 概念
盒子模型将页面中的每个元素视为一个盒子，包括以下几个属性：
- `width`：宽度
- `height`：高度
- `border`：边框
- `padding`：内边距
- `margin`：外边距

![image-20241110210607041](https://cdn.jsdelivr.net/gh/wwwqqqzzz/Image/img/image-20241110210607041.png)

### 2. 盒子属性

#### 2.1 `border`
- 表示边框，分为四个方向：`top`、`right`、`bottom`、`left`。
- 每个边框包含三种样式：颜色、粗细和样式，如 `solid`、`dashed`、`dotted`、`double` 等。

#### 2.2 `padding`
- 表示内容与边框之间的内边距，可简写为按顺时针方向（上、右、下、左）分别定义。

#### 2.3 `margin`
- 表示盒子与其他元素之间的外边距，简写规则与 `padding` 类似。

### 3. 元素所占空间计算
元素的实际空间计算公式：
- 宽度：`width + 左右 padding + 左右 border + 左右 margin`
- 高度：`height + 上下 padding + 上下 border + 上下 margin`