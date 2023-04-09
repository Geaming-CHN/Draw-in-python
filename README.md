# Draw-in-python

一个记录绘图常用的python代码库。

以 https://www.python-graph-gallery.com/ 为参考基础，不过这个仓库似乎到2022年5月份左右就没有更新了。

在文末也附有相关的实用链接。

# 基础设置

## 起手式
```Python
import matplotlib.pyplot as plt

from matplotlib import rcParams

import seaborn as sns
sns.set_palette("rainbow") # 设置颜色

config = {
    "font.family": 'serif', # 衬线字体
    "font.size": 12, # 相当于小四大小
    "font.serif": ['SimSun'], # 宋体
    "mathtext.fontset": 'stix', # matplotlib渲染数学字体时使用的字体，和Times New Roman差别不大
    'axes.unicode_minus': False # 处理负号，即-号
}
rcParams.update(config)

%matplotlib inline
%config InlineBackend.figure_format = 'svg'  # svg矢量图不会模糊
```

## 常见设置
```python
plt.figure(figsize=(18,7)) # 设置画布大小
plt.xlabel("") # x轴label
plt.ylabel("") # y轴label
plt.legend(loc='best') # 图例放置

x_pos, x_ticks = [], []
for i in range(1, df.shape[0], 30):
    x_pos.append(i)
    x_ticks.append(str(df.iloc[i,1]).split(" ")[0])

plt.xticks(x_pos, x_ticks, rotation = 40)
plt.savefig("1.eps", format="eps") # 保存图片，这里指定为eps格式
```



# 2D drawing

## Distribution

### Violin

### Density

### Histogram

### Boxplot

### Ridgeline

## Correlation

### Scatterplot

### Heatmap

### Correlogram

### Bubble

### Connected Scatter

### 2D Density

## Ranking

### Barplot

### Spider / Radar

### Wordcloud

### Parallel

### Lolipop

### Circular Barplot

## Part Of A Whole

### Treemap

### Venn Diagram

### Donut

### Pie Chart

### Dendrogram

### Circular Packing

## Evolution

### Line Chart

### Area Chart

### Stacked Area

### Streamgraph

### Timeseries

## Map

### Map

### Choropleth

### Hexbin

### Cartogram

### Connection

### Bubble

## Flow

### Chord Diagram

### Network

### Sankey

### Arc Diagram

### Edge Bundling

# 3D drawing

# 其他

## Cheat Sheets