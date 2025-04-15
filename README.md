# WordNet MCP 服务

这是一个基于WordNet的Model Context Protocol (MCP) 服务实现，提供词汇查询功能，包括同义词、反义词、上下位词和定义等。

## 功能

- 查询单词的同义词
- 查询单词的反义词
- 查询单词的上位词（更一般的概念）
- 查询单词的下位词（更具体的概念）
- 查询单词的定义和例句
- 获取单词的综合信息

## 安装

本项目使用 uv 进行依赖管理。确保已安装 uv，然后执行以下命令：

```bash
# 安装依赖
uv add nltk httpx "mcp[cli]"
```

## 使用方法

### 启动服务

```bash
# 使用 uv 运行
uv run python app.py

# 或者使用 mcp 命令行
uv run mcp
```

### 在 Cursor 中添加 MCP 服务

1. 在 Cursor 中安装 MCP 服务
2. 添加 WordNet MCP 服务
3. 在使用时，可以选择所需的功能进行调用

## 示例

```python
# 查询单词 "happy" 的同义词
get_synonyms("happy")

# 查询单词 "happy" 的反义词
get_antonyms("happy")

# 获取单词 "happy" 的所有相关信息
get_word_info("happy")
```

## 开发

### 安装开发依赖

```bash
uv add -d ruff pytest
``` 