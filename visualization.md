

```python
import pandas as pd
import plotly as plotly
from plotly.offline import download_plotlyjs, init_notebook_mode, plot, iplot,offline
import plotly.graph_objs as go
offline.init_notebook_mode()
```


<script type="text/javascript">window.PlotlyConfig = {MathJaxConfig: 'local'};</script><script type="text/javascript">if (window.MathJax) {MathJax.Hub.Config({SVG: {font: "STIX-Web"}});}</script><script type='text/javascript'>if(!window._Plotly){define('plotly', function(require, exports, module) {/**
* plotly.js v1.42.5
* Copyright 2012-2018, Plotly, Inc.
* All rights reserved.
* Licensed under the MIT license
*/



```python
labels = ['Vim','Emacs','NotePad','VsCode','Atom','Sublime','Others']
values = [86,19,129,284,113,145,46]
colors = ['#7CFC00', '6A5ACD', '#00FFFF', '#4682B4','#D3D3D3','#FFD700','#DB7093']

trace = go.Pie(labels=labels, values=values,
               hoverinfo='label+percent', textinfo='value',
               title = 'Text Editors',
               textfont=dict(size=15),
               marker=dict(colors=colors, 
                           line=dict(color='#000000', width=2)),
              )

plotly.offline.iplot([trace], filename='Text Editors')
```


<div id="bbf96293-abec-4378-b82b-a91aa75d115b" style="height: 525px; width: 100%;" class="plotly-graph-div"></div><script type="text/javascript">require(["plotly"], function(Plotly) { window.PLOTLYENV=window.PLOTLYENV || {};window.PLOTLYENV.BASE_URL="https://plot.ly";Plotly.newPlot("bbf96293-abec-4378-b82b-a91aa75d115b", [{"hoverinfo": "label+percent", "labels": ["Vim", "Emacs", "NotePad", "VsCode", "Atom", "Sublime", "Others"], "marker": {"colors": ["#7CFC00", "6A5ACD", "#00FFFF", "#4682B4", "#D3D3D3", "#FFD700", "#DB7093"], "line": {"color": "#000000", "width": 2}}, "textfont": {"size": 15}, "textinfo": "value", "title": "Text Editors", "values": [86, 19, 129, 284, 113, 145, 46], "type": "pie", "uid": "bee8b39c-ed9b-4487-b304-3afedd368c59"}], {}, {"showLink": true, "linkText": "Export to plot.ly", "plotlyServerURL": "https://plot.ly"})});</script><script type="text/javascript">window.addEventListener("resize", function(){window._Plotly.Plots.resize(document.getElementById("bbf96293-abec-4378-b82b-a91aa75d115b"));});</script>



```python
# The code to generate WordClouds
# from os import path
# from PIL import Image
# import numpy as np
# import matplotlib.pyplot as plt
# import os

# from wordcloud import WordCloud, STOPWORDS

# # get data directory (using getcwd() is needed to support running example in generated IPython notebook)
# d = path.dirname(__file__) if "__file__" in locals() else os.getcwd()

# # Read the whole text.
# text = open(path.join(d, 'text/vscode.txt')).read()


# alice_mask = np.array(Image.open(path.join(d, "text/vim.png")))

# # stopwords = set(STOPWORDS)
# # stopwords.add("hahaha")

# wc = WordCloud(background_color="white",max_words=100000, mask=alice_mask,
#                stopwords=stopwords, contour_width=1, contour_color='steelblue',max_font_size=200)

# # generate word cloud
# wc.generate(text)

# # store to file
# wc.to_file(path.join(d, "vscode.png"))

# # show
# plt.imshow(wc, interpolation='bilinear')
# plt.axis("off")
# plt.figure()
# plt.imshow(alice_mask, cmap=plt.cm.gray, interpolation='bilinear')
# plt.axis("off")
# plt.show()

```