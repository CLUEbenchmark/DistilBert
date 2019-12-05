一、DistilBert for Chinese 海量中文预训练蒸馏Bert模型

拟于12月16日发布 target to release on Dec 16th.

拟发布内容 Contents：

1.1 可下载的蒸馏模型，已经训练过 

a pretrained chinese DistilBert, others can use it directly or  trained again on their own corpus; 

1.2 可用于下游任务的例子和代码，包括3个ChineseGLUE(CLUE)的任务 

fine tuning examples and codes using DistilBert on three ChineseGLUE(CLUE) tasks; 

1.3 小模型基准测评

performance comparsion with albert_tiny, ernie_tiny.


二、distillbert简介

2.1 BERT 瘦身之三个思路

Distillation（蒸馏）：通过蒸馏技巧，将 BERT 模型知识导入小模型，之后用小模型；
Quantization（量化）：将高精度模型用低精度来表示，使得模型更小；
Pruning（剪枝）：将模型中作用较小部分舍弃，而让模型更小。

2.2 Distillation最早的蒸馏法原理

一般认为是 Hinton 在 Distilling the Knowledge in a Neural Network 提出，之后得到推广，Hinton 在论文中提出方法很简单，就是让学生模型的预测分布，来拟合老师模型（可以是集成模型）的预测分布。

2.3 目前较好的实现实践

比较完美实现上述经典方法对 BERT 蒸馏的是 HuggingFace 前段时间提出的 DistilBERT，将 BERT-base 从 12 层蒸馏到 6 层 BERT 模型。当然除了上述方法，还用了些其他技巧，比如用老师模型参数初始化学生模型，更多细节可看 HuggingFace 的博客和论文。

三、其他

Contact with chineseGLUE@163.com to join us.

