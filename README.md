# 大模型技术总览

## 学习资料

### 【原理】大模型原理
- [入门书籍] https://intro-llm.github.io/ （重点阅读1、2、3、6章）

---

### 【脉络】ChatGPT的前世今生
- [白话ChatGPT-李宏毅] https://www.bilibili.com/video/BV1U84y167i3
- [OpenAI-大语言模型入门] https://www.bilibili.com/video/BV1Hj41177fb
- [论文研读] InstructGPT: Training language models to follow instructions with human feedback
- [论文讲解及扩展] https://zhuanlan.zhihu.com/p/636270877
- [论文配套视频-李沐] https://www.bilibili.com/video/BV1hd4y187CR/?spm_id_from=333.788&vd_source=71b548de6de953e10b96b6547ada83f2

---

### 【手撕】图解系列Transformer/BERT/GPT
- [视频教程] https://www.bilibili.com/video/BV11v4y137sN
- [图解+手撕底层原理] https://github.com/datawhalechina/learn-nlp-with-transformers/tree/main/docs/篇章2-Transformer相关原理
- [手写大模型推理(Pytorch版)] https://github.com/naklecha/llama3-from-scratch
- [ROPE编码] https://www.bilibili.com/video/BV1Tr421p7By

---

### 【实战】大模型实战 
- [Transformer教程] https://transformers.run/ （重点阅读4～12章）

---

## 实战

### 任务描述
本次实战要求完成一个基于Google T5-Base的生成式问答模型。模型需要能够根据输入的"context"和"question"生成对应的“answer”。

### 模型要求
- 模型类型：生成式问答模型
- Backbone：Google T5-Base
- 预训练模型地址：[uer/t5-base-chinese-cluecorpussmall](https://huggingface.co/uer/t5-base-chinese-cluecorpussmall)

### 数据格式
- 每一行为一个数据样本，json 格式。
- 其中，"context" 代表参考文章，question 代表问题，"answer" 代表问题答案。
```json
{
  "context": "违规分为:一般违规扣分、严重违规扣分、出售假冒商品违规扣分...",
  "answer": "12月31日24:00",
  "question": "淘宝扣分什么时候清零", 
  "id": 203
}
```

### 评价指标
- 模型的评价指标采用BLEU-1，BLEU-2，BLEU-3，BLEU-4。

### 要求：
- 完成模型训练的代码，并画出模型收敛曲线图。
- 完成模型的预测代码，给定任意context和query，可以生成对应答案。

### 附加
- 预训练模型地址：https://huggingface.co/uer/t5-base-chinese-cluecorpussmall
- 数据集：链接：https://pan.quark.cn/s/6d4a98cd65f2 提取码：****

## 如有侵权，联系必删，仅用于学习用途，不做任何商业用途。
