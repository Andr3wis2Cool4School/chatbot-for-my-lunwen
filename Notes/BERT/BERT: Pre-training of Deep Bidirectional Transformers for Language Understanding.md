**BERT stands for Bidirectional Encoder Representations from Transformers**


Encoder == 编码器
编码器把人类认识的文字 转换成计算机认识的数字特征


> BERT is designed to pre- train deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context in all layers. As a re- sult, the pre-trained BERT model can be fine- tuned with just one additional output layer to create state-of-the-art models for a wide range of tasks.


BERT 是一个PRE-TRAINED model
从没有标签的模型中进行训练的
有点像迁移学习的感觉.

--------

> Both left and right context in all layers.
it means from left to right is fine, from right to left is also fine. 
My way of thinking this sentence is that take a sentence as an example,

> The weather today is pettry good, So we will play football this afternoon.

people thinking is that from left to right. 

If we let the computer to do the predict. If we want to let our computer to predict the word `good`. From a normal condition, The computer are trying by using the content of the left to predict the word of good. This is called from Left to Right. But BERT can also do predict from right to left. **所以BERT给我的感觉有点像完形填空的感觉.-3- 在预测的时候既参考上文又参考下文.**


> As a result, the pre-trained  BERT model can be finetuned with just one additional output layer to create state-of-the-art models for a wide range of tasks.

So once we can get the pre-trained model, we can make this model into our area.站在巨人的肩膀上, 直接起飞.

**With one additional output layer**  means that we need to add one more layer into the BERT model, The output model.自己设计输出层.

---------------

> The masked language model randomly masks some of the tokens from the input, and the objective is to predict the original vocabulary id of the masked
arXiv:1810.04805v2 [cs.CL] 24 May 2019
word based only on its context. Unlike left-to- right language model pre-training, the MLM ob- jective enables the representation to fuse the left and the right context, which allows us to pre- train a deep bidirectional Transformer.


完形填空 `based only on its context`

--------------------
### BERT 

> We introduce BERT and its detailed implementa- tion in this section. There are two steps in our framework: pre-training and fine-tuning. Dur- ing pre-training, the model is trained on unlabeled data over different pre-training tasks. For fine- tuning, the BERT model is first initialized with the pre-trained parameters, and all of the param- eters are fine-tuned using labeled data from the downstream tasks.

Pre-training model: google's model
fine-tuning: our stuff 
 
正常情况下, 我们用神经网络 我们要初始化权重参数 一般情况下是随机初始化
但是有了BERT模型后 我们就不用随机初始化了 直接用谷歌训练好的BERT当成我们的一开始的权重参数.在别人学完的基础上,再微调.

当我们自己用的时候, BERT一开始初始化, 在FINE-TUning的时候用的是又标签的数据.

论文中忽略了编码器的介绍........












