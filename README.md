# Text Analysis  [2019-01]

## 数据集
包含leleketang.com做文库十万余条作文信息，每条作文包含标题、主题、作者、时间、地点、正文、评语等信息。

## 代码内容
根据文本数据，从多个维度对数据进行分析，并用python中的pyecharts绘制图表。（pyecharts是一个用于生成Echarts图表的类库。Echarts是百度开源的一个数据可视化 JS 库。用Echarts生成的图可视化效果非常棒，pyecharts是为了与Python进行对接，方便在 Python 中直接使用数据生成图。）
### Part 1 基本信息分析
分析了users和compositions的基本属性，为该网站的作文库建立了基本的画像。
1. users
- 对users进行地域分析，可视化用户数量地域分布热力图
![热力图](https://github.com/BELIEVEfxy/text_analysis/blob/master/code/统计分析与应用代码/1.png)
- 对users进行时间分析，讨论用户随时间变化的情况
![折线图](https://github.com/BELIEVEfxy/text_analysis/blob/master/code/统计分析与应用代码/3.png)
2. compositions
- 对作文按话题进行分类统计，并可视化为漏斗图
![漏斗图](https://github.com/BELIEVEfxy/text_analysis/blob/master/code/统计分析与应用代码/4.png)
- 对作文评语进行情感分析，为每个作文打分，统计不同分数段作文的数量情况，可视化为玫瑰图
![玫瑰图](https://github.com/BELIEVEfxy/text_analysis/blob/master/code/统计分析与应用代码/5.png)
- 对作文年份进行统计分析，统计每个年份下不同等级作文的数量、最大值、最小值和均值，并进行可视化
![环形图](https://github.com/BELIEVEfxy/text_analysis/blob/master/code/统计分析与应用代码/7.png)

### Part 2 文本信息挖掘
1. 关键词统计
- 使用TF-IDF、Doc2Vec的方法提取每个主题下的所有作文的前500个关键词
- 将每个话题下最重要的50个关键词用词云图的方式展示出来
![词云图](https://github.com/BELIEVEfxy/text_analysis/blob/master/code/统计分析与应用代码/8.png)
2. 推荐高级表达词
用户输入一个词语（在作文词语库中存在），首先判断该词所属的话题，接着在该话题下的所有词语中寻找距离用户输入词最近的“高级”词语。
