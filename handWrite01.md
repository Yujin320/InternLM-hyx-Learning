## 书生-浦语大模型全链路开源体系

#### 模型

1. InternLM-7B
2. InternLM-20B
3. InternLM-123B（非开源）

#### 从模型到应用

业务场景复杂 -> 模型微调 -> 全参数微调/部分参数微调 -> 构建智能体（与数据库交互或调用外部api）

#### 全链路开源开放体系

1. 书生-万卷：开源的训练数据（文本数据，图像-文本数据，视频数据）
2. InternLM-Train：预训练工具
   1. 多显卡拓展支持
   2. 并行性能优化
   3. 兼容HggingFace等训练生态
   4. 开箱即用，支持语言模型
3. XTurner：微调工具（适配多种微调算法，开源生态，显存优化效果巨大）
   1. 增量续训（模型学习新的知识）
   2. 有监督微调（模型学会遵循固定的指令和少量领域知识）
4. LMDeploy：GPU部署解决
   1. 模型轻量化：4b量化，8bk/v
   2. 推理引擎魔改优化
   3. 基于大模型提供兼容生态接口（比如OpenAI）
5. OpenCompass：评测工具：
   1. 测试方面：学科，语言，知识，理解，推理，安全
   2. 提供工具：评测时可用的工具（提示工具）
   3. 自定义评测数据集和大模型评测接口
6. Lagent，AgentLego：智能体应用
   1. Lagent：智能体框架
      1. 支持多种智能体工作流程能力
      2. 支持多种大语言模型（chatGPT，InternLM，Llama，HuggingFace）
      3. 支持多种工具，多模态工具或者能力拓展工具
   2. AgentLego：多模态智能体工具集合
      1. 多模态工具额
      2. 支持多个智能体系统（Langchain）
      3. 多模态工具调用接口
      4. 远程工具部署和调试支持
