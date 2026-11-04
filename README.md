# LLM-Commonsense-Benchmark

## Motivation

这是一个专门测试LLM智慧程度的benchmark，这是一个对于人类非常简单的问题。任何智力正常的人类都能在10s内知道怎么做。题中涉及找规律，人类可以轻而易举的根据常识判断出正确的规律出来。但是图片在数学上有一个更简单形式的“陷阱”规律，虽然人类不会想到，但是对于世界知识不充分的AI来说容易踩坑。在当前LLM卷前端和长程Agent能力的时代，不能放弃对于LLM世界知识和数据集泛性的测试。

## 测试方法
1. 让待测试的模型阅读 Benchmark 文件夹，且access仅限该文件夹，不允许读取外部文件。
2. 比较 Answer 文件夹和 Benchmark/1 文件夹中的内容，必须完全一致。
3. 这是一个 P/NP 问题，如果没有通过，则记录；如果通过了，再记录它的整体耗时。

## 测试结果

### 测试环境

Windows10 + pi v1.5.0 + 各模型开最高思考

### 测试结论

| 模型 | 结果 | 耗时 | 评语 |
| --- | --- | --- | --- |
| GPT 6.1 Sol | 通过 | 1min | 秒了 |
| GPT 6 Astra | 通过 | 1min | 秒了 |
| GLM 5.3 Flash | 通过 | 10min | 看着菜，其实是国模里最强的了 |
| Qwen3.8 Max | 通过 | 20min | 孩子傻，但是孩子肯用工 |
| MiMo V2.6 Flash | 通过 | 21min | 孩子傻，但是孩子肯用工 |
| Claude Fable 5.1 | 未通过 | - |  |
| Claude Haiku 5 5 | 未通过 | - |  |
| Claude Opus 5.5 | 未通过 | - |  |
| Claude Sonnet 5.5 | 未通过 | - |  |
| DeepSeek V4 Pro | 未通过 | - |  |
| DeepSeek V4.1 Flash | 未通过 | - |  |
| Gemini 4 Argon | 未通过 | - |  |
| GLM 5.3 | 未通过 | - |  |
| GPT 6.1 Terra | 未通过 | - |  |
| Grok 4.7 | 未通过 | - |  |
| HY4 Preview | 未通过 | - |  |
| LongCat 2.0 | 未通过 | - |  |
| MiMo V2.6 Flash | 未通过 | - |  |
| MiMo V2.6 Pro | 未通过 | - |  |
| MiniMax M3 | 未通过 | - |  |
| MiniMax M3.1 Flash | 未通过 | - |  |
| Qwen3.8 Flash | 未通过 | - |  |
| Step 5 Preview | 未通过 | - |  |

共测试 23 个模型，通过 5 个，未通过 18 个，通过率 21.7%。
