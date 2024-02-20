---
sidebar-label: 'Hi!'
sidebar_position: 0
---


# Hello

This is my **first Docusaurus document**!


## 链接

支持使用url路径或相对文件路径的常规Markdown链接

Let's see how to [Tutorial Intro](intro).

Let's see how to [Create a page](tutorial-basics/create-a-page.md).

## Images

![Docusaurus logo](/img/docusaurus.png)

也可以使用相对于当前文件的图像.
![docsVersionDropdown](./tutorial-extras/img/docsVersionDropdown.png)

## 代码块

```jsx titile="src/compoments/HelloDocusaurus.js"
function HelloDocusaurus(){
    return <h1>Hello,Docusaurus!</h1>;
}
```

## 告诫
:::tip[My tip]

Use this awesome feature option

:::

:::danger[Take care]

This action is dangerous

:::

## MDX and React Components

```
export const Highlight=({children,color})=>(
    <span style={{
       backgroundColor: color,
       borderRadius: '20px',
       color: '#fff',
       padding: '10px',
       cursor: 'pointer',
    }}
    onClick={()=>{
        alert(`You clicked the color ${color} with label ${children}`)
    }}
    >
    {children}
    </span>
);

This is <Hightlight color="#25c2a0">Docusaurus green</Highlight> !

This is <Highlight color="#1877F2">Facebook blue</Highlight> !
```

export const Highlight=({children,color})=>(
    <span style={{
       backgroundColor: color,
       borderRadius: '20px',
       color: '#fff',
       padding: '10px',
       cursor: 'pointer',
    }}
    onClick={()=>{
        alert(`You clicked the color ${color} with label ${children}`)
    }}
    >
    {children}
    </span>
);

This is <Highlight color="#25c2a0">Docusaurus green</Highlight> !

This is <Highlight color="#1877F2">Facebook blue</Highlight> !

## 构建你的网站

为生产构建站点:
```
npm run build
```
静态文件在文件夹中生成

## 部署站点

```
npm run serve
```

## 创建文档版本

```
npm run docusaurus docs:version 1.0
```

## 添加版本下拉列表

```jsx docusaurus.config.js
export default{
    themeConfig:{
        navbar:{
            items:[
                {
                    type:'docsVersionDropdown',
                },
            ],
        },
    },
}
```

## 翻译网站

### 配置i18n

修改以添加对区域设置的支持

```jsx docusaurus.config.js
export default {
  i18n: {
    defaultLocale: 'en',
    locales: ['en', 'fr'],
  },
};
```

### 添加区域设置下拉列表
若要跨语言无缝导航，请添加区域设置下拉列表。

修改文件：docusaurus.config.js

```jsx docusaurus.config.js
module.exports = {
  themeConfig: {
    navbar: {
      items: [
        {
          type: 'localeDropdown',
        },
      ],
    },
  },
};
```