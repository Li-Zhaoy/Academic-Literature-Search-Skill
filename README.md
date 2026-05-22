# Academic-Literature-Search-Skill

一个专为 Claude 设计的结构化 Prompt Skill，让 Claude 化身专业学术文献检索助手，自动完成双源检索、去重、分类统计和多级回退 PDF 下载。

## 特性
- **双源检索**：同时挖掘 arXiv (预印本) 和 Semantic Scholar (正式发表)。
- **智能去重**：优先保留顶会/顶刊正式发表版本，剔除重复的预印本。
- **多级回退下载**：从 OA 官方源 -> Unpaywall -> CrossRef -> arXiv -> 搜索引擎兜底，尽可能获取免费 PDF。
- **结构化产出**：自动生成按关键词分类的 Excel 统计表，并标注跨词重复情况和下载状态。

## 如何使用

### 前置准备
申请 [Semantic Scholar API Key](https://www.semanticscholar.org/product/api#api-key) (免费)

### 导入 Skill
1. 下载本仓库中的 `skill.md` 文件。
2. 打开 Claude，进入 **Project Knowledge** (项目知识库) 设置。
3. 将 `skill.md` 的内容上传或粘贴进去。
4. 在项目指令中添加："请严格按照 skill.md 中的流程执行文献检索任务。"

### 运行
向 Claude 发送指令，例如：
> "请严格按照 skill.md 中的流程执行文献检索任务，帮我检索近90天内关于'大语言模型在医疗诊断中的应用'的最新文献。"

Claude 会自动引导你输入 API Key，并按步骤确认关键词、检索和下载。

## License
MIT License
