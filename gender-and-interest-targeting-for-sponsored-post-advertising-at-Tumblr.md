tumblr的广告定向 和 用户性别预测

广告定向：基于demographics 一般指性别 年龄；另外一类为兴趣定向。

如何提取用户兴趣？

1. 人工定义用户的兴趣体系 

2. 从文章中提取关键字 共现的词频  检测bigrams 方法 两个词的共现 /  每个词单独出现的次数乘积

3. 文章中提取关键字作为用户兴趣  然后将这些兴趣分类到现有的用户体系（预定义好的体系）先试用word2vec训练tag的向量 然后knn来进行分类（cosin距离）

4. 兴趣公式时间衰减 加和 保证能够按照天级别来计算 merge


小技巧：
1. 特征取log log(1+x)

2. 时间衰减 \alpha ^ time_delta alpha = 0.9
