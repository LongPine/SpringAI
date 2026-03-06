## 一、项目基本信息
- **项目名称**：SpringAI
- **项目作者**：LongPine
- **仓库类型**：GitHub Public 开源项目
- **完成时间**：2025-11-12
- **开发语言**：Java
- **核心框架**：Spring Boot / Spring AI
- **构建工具**：Maven（mvnw 包装器）
- **部署支持**：Nginx 反向代理

---

## 二、项目功能清单（4 大核心应用）
1. **聊天机器人**
   基于大模型接口实现多轮对话、意图理解、自然语言交互。
2. **哄哄模拟器**
   情感对话场景，生成安抚、安慰、哄人式话术回复。
3. **智能助手**
   通用任务处理、信息查询、指令执行、日常问答。
4. **ChatPDF**
   PDF 文件上传 → 文本解析 → 内容问答 → 总结提取。

---

## 三、完整技术栈归档
### 1. 后端核心
- Java 8+/11+
- Spring Boot
- **Spring AI**（大模型统一调用层）
- Maven 项目构建

### 2. 文件处理
- PDF 文本提取（PDFBox 或 Tika）
- 文件上传、本地存储管理

### 3. 部署与运维
- Nginx（spring-ai-nginx 配置）
- Maven Wrapper（跨环境构建）
- Git 版本管理

### 4. 基础组件
- pom.xml 依赖管理
- .gitignore / .gitattributes
- README 项目说明

---

## 四、项目目录结构说明
```
LongPine/SpringAI
├── .mvn/wrapper/        # Maven 包装器，无环境也可构建
├── spring-ai-nginx/     # Nginx 部署配置文件
├── src/                 # 项目主源码（业务+控制器+服务）
├── pom.xml              # Maven 依赖、插件、版本管理
├── mvnw / mvnw.cmd      # Maven 启动脚本
├── .gitignore           # Git 忽略文件
├── README.md            # 项目说明文档
└── 中二知识笔记.pdf     # ChatPDF 测试文件
```

---

## 五、核心业务流程（重点归档）
### 1. ChatPDF 流程
1. 用户上传 PDF
2. 后端解析 PDF 提取文本
3. 拼接提示词 + 文档内容
4. 调用 Spring AI 大模型接口
5. 返回问答/总结结果

### 2. 对话类应用流程
1. 前端输入文本
2. Controller 接收请求
3. Service 调用 Spring AI
4. 模型生成回复
5. 返回前端展示

---

## 六、技术亮点与价值
- 基于 **Spring 生态**，Java 后端友好，易维护、易扩展
- Spring AI 统一封装大模型调用，降低切换成本
- 提供**4 个可直接运行的 AI 场景**，开箱即用
- 支持 Nginx 部署，可上线对外提供服务
- 标准 Maven 结构，适合学习、二次开发

---

## 七、可优化与扩展方向（归档版）
1. **代码架构**
   - 分层：Controller / Service / Client / Utils
   - 通用 AI 客户端封装
2. **功能增强**
   - 流式输出 SSE
   - 多模型切换
   - 大文件分片解析
   - 向量库检索（RAG）
3. **部署安全**
   - Docker 容器化
   - API 鉴权、限流
   - 密钥环境变量配置
4. **体验提升**
   - 日志、异常处理
   - 前端页面
   - 多文档批量处理

---

## 八、项目定位总结
**SpringAI 是一套基于 Spring Boot + Spring AI 实现的 Java AI 应用集合，包含聊天机器人、哄哄模拟器、智能助手、ChatPDF 四大场景，是 Java 后端快速入门 AI 大模型应用的完整实战项目。**

---
