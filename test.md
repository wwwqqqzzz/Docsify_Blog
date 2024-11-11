# test

## tabs

```markdown
<!-- tabs:start -->

#### **English**

Hello!

#### **French**

Bonjour!

#### **Italian**

Ciao!

<!-- tabs:end -->
```

plantuml绘图

```plantuml
@startuml
skinparam linetype ortho

package "技术栈" {

  package "前端" {
    [Vue.js] as Vue
    [Vuex] as Vuex
    [Vue Router] as VueRouter
    [Axios] as Axios
    [jQuery] as jQuery
    [JSP] as JSP
  }

  package "后端" {
    [Spring Boot] as SpringBoot
    [MyBatis-Plus] as MyBatisPlus
    [Java] as Java
  }

  package "数据库" {
    [MySQL] as MySQL
    [Redis] as Redis
  }

  package "开发工具" {
    [Git] as Git
    [IntelliJ IDEA] as IDEA
    [VS Code] as VSCode
    [Maven] as Maven
  }

  package "云服务" {
    [AWS] as AWS
    [Azure] as Azure
  }
}

' 前端与后端的连接
Vue --> Axios : 发起请求
Vue --> Vuex : 状态管理
Vue --> VueRouter : 路由管理
Vuex --> SpringBoot : 与后端交互
Vue --> jQuery : 页面交互（可选）
Vue --> JSP : 服务器端渲染（可选）

' 后端与数据库的连接
SpringBoot --> MyBatisPlus : 数据库操作
SpringBoot --> MySQL : 数据存储
SpringBoot --> Redis : 缓存

' 开发工具的配合
Git --> IDEA : 版本控制与开发环境
Git --> VSCode : 版本控制与开发环境
Maven --> SpringBoot : 依赖管理与构建

' 云服务
AWS --> Maven : 部署到云
Azure --> Maven : 部署到云

@enduml
```

mermaid绘图

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {'primaryColor': '#00796b', 'edgeLabelBackground':'#ffffff', 'tertiaryColor': '#b2dfdb'}}}%%
graph TD
  subgraph 技术栈
    subgraph 前端
      Vue[Vue.js]
      Vuex[Vuex]
      VueRouter[Vue Router]
      Axios[Axios]
      jQuery[jQuery]
      JSP[JSP]
    end

    subgraph 后端
      SpringBoot[Spring Boot]
      MyBatisPlus[MyBatis-Plus]
      Java[Java]
    end

    subgraph 数据库
      MySQL[MySQL]
      Redis[Redis]
    end

    subgraph 开发工具
      Git[Git]
      IDEA[IntelliJ IDEA]
      VSCode[VS Code]
      Maven[Maven]
    end

    subgraph 云服务
      AWS[AWS]
      Azure[Azure]
    end
  end

  Vue --> Axios
  Vue --> Vuex
  Vue --> VueRouter
  Vuex --> SpringBoot
  Vue --> jQuery
  Vue --> JSP


  SpringBoot --> MyBatisPlus
  SpringBoot --> MySQL
  SpringBoot --> Redis


  Git --> IDEA
  Git --> VSCode
  Maven --> SpringBoot


  AWS --> Maven
  Azure --> Maven
```





### Here are some of your previous markdown contents



> [!NOTE]
>
> 翻页
>
> tab



### gif图片使用

```pdf
https://gbodigital.github.io/docsify-gifcontrol/#/
```





### Q&A

# FAQ Section

Introduction text for the FAQ page.

+ 这是什么 +

  blog

+ 这是什么 +

  blog



### HTML Preview

```html preview
<p>Hello, World.</p>
```

