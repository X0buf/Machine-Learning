# TF-IDF

- 朴素贝叶斯
- TF：term frequency  词的频率        出现的次数
- idf：逆文档频率 inverse document frequency       log（总文档数量/该词出现的文档数量）

TF-IDF的主要思想是：如果某个词或短语在一篇文章中出现的概率高，并且在其他文章中很少出现，则认为此词或者短语具有很好的类别区分能力，适合用来分类。

TF-IDF作用：用以评估一字对于一个文件集成或一个语料库中的其中一份文件的**重要程度**。

类：sklearn.feature_extraction.text.TfidfVectorizer

## TdidfVectorizer语法

- TfidfVectorizer(stop_word=None,...)
  - 返回词的权重矩阵
  - TfidfVectorizer.fit_transform(X)
    - X: 文本或者包含**文本字符串的可迭代对象**
    - 返回值: 返回sparse矩阵
  - TfidfVectorizer.inverse_transform(X)
    - X：array 数组或者sparse矩阵
    - 返回值：转换之前数据格式
  - TfidfVectorizer.get_feature_names()
    - 返回值：单词列表

## 为什么需要TfidfVectorizer

- 分类机器学习算法的重要依据