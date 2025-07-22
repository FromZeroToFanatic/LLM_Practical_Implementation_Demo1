# 问答模型

## 任务描述
本次作业要求完成一个基于Google T5-Base的生成式问答模型。模型需要能够根据输入的"问题"和"参考文章"生成对应的答案。

## 模型要求
- 模型类型：生成式问答模型
- Backbone：Google T5-Base
- 预训练模型地址：[uer/t5-base-chinese-cluecorpussmall](https://huggingface.co/uer/t5-base-chinese-cluecorpussmall)

## 数据格式
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

## 评价指标
模型的评价指标采用BLEU-1，BLEU-2，BLEU-3，BLEU-4。

## 要求：
- 完成模型训练的代码，并画出模型收敛曲线图。
- 完成模型的预测代码，给定任意context和query，可以生成对应答案。

## 附加
- 预训练模型地址：https://huggingface.co/uer/t5-base-chinese-cluecorpussmall
- 数据集：链接：https://pan.quark.cn/s/6d4a98cd65f2 提取码：****
