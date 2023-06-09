# GPT-PROMPT (GPTP)

一个 CHAT-GPT 提示指令工具根据用户的输入转指令为提示指令 （prompt instruction）, 用户可根据不同的需求场景来选择。GPT 不再是一个 通用AI 而是有许多的角色能更好的限制其能力。

# 技术栈
后端：Go
前端：Vue.js
脚手架：Go-Admin
# 特点
为了让GPT理解和执行这些指令，我们需要开发一个自然语言编译器。编译器的主要任务是将用户输入的指令翻译成GPT可以理解的格式，并将GPT的输出转换为用户期望的结果。

例1：

```
ROLE: lawyer   # 充当一个律师
CATE: 本科  # 定义律师知识的范畴，不定义则默认全领域专家
ASK: 写一个法律纲要
SIZE: 200
```

发送给 GPT 的就是： 你现在是一个 [lawyer] , 知识范围限定为 [本科]。 我需要你写一个法律纲要。字数在200。


例2：

```
TOOL: sql  # 一个sql编译器工具
TYPE: mysql # 工具有可能是 mysql 也可能是 其他的
ASK: 用户和订单表查询销量最高的用户  # 把需要输出的 SQL 打印出来

```

发送给 GPT 的就是：你现在充当一个 [ SQL ] 编译器，类型为 [mysql]。用户和订单表查询销量最高的用户。

```
    ROLE: 命理师
    CATE: 易经
    ASK:  [1998-8-8 11:20:20] [男] [四川] [广安] [xxx]
```

发送给 GPT 的就是：你现在是一个 [命理师]，使用 [易经]。用户的生辰八字是 [1998-8-8 11:20:20] [男] [四川] [广安] [xxx]。

# 开发计划

GPTL的开发将分为以下几个阶段：

1. 设计和实现自然语言编译器：将用户输入的指令翻译成GPT可以理解的格式，并将GPT的输出转换为用户期望的结果。
2. 构建前端界面：使用Vue.js开发用户友好的前端界面，允许用户输入指令并查看GPT的执行结果。
开发后端服务：使用Go语言实现后端服务，用于处理前端发送的请求，与数据库进行交互，以及与GPT模型进行通信。
3. 集成数据库：将指令动态添加和更新，并保存在数据库中，以便在后端动态生成GPT指令。
测试和优化：在实际使用中对GPTL进行测试和优化，以提高性能和用户体验。
4. 文档和示例：编写详细的文档和示例，帮助开发者和用户更好地理解和使用GPTL。

# 贡献
我们欢迎有兴趣的开发者加入这个伟大的项目，共同为实现GPTL的愿景而努力！请查看我们的贡献指南，了解如何为项目做出贡献。如果你在使用GPTL过程中遇到问题或有建议，请随时提交问题或拉取请求。

# 感谢

快速搭建脚手架：https://github.com/go-admin-team/go-admin/blob/master/README.Zh-cn.md

CHATGPT: https://openai.com/

