# Sentiment Track
# Bert
首先用数据对BERT模型进行预训练，再对模型进行fine-tuning，使得预训练好的模型进行情感分类这个下游任务的训练。
之后，对Bert模型得到的新闻用句向量表示，使用captum 包进行Integrated Gradients解释，得到每个词语的动态情感分。
接下来将情感分用dct变换标准化，之后用KMeans聚类得到七个轨道，并标记同类型的新闻。由此产出了三万条带有情感分和轨道标签的新闻
