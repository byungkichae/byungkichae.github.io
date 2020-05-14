---
layout: post
title: "jupyer markdown test"
categories: misc
---

# 테스트 Page


```python
import chart_studio.plotly as py
import plotly.graph_objects as go
import chart_studio

chart_studio.tools.set_credentials_file(username='nchae8', api_key='gUleU1WNyzgo1rDMjrbB')

chart_studio.tools.set_config_file(sharing='public')
trace0 = go.Scatter(
    x=[1, 2, 3, 4],
    y=[10, 15, 13, 17]
)
trace1 = go.Scatter(
    x=[1, 2, 3, 4],
    y=[16, 5, 11, 9]
)
data = [trace0, trace1]

py.iplot(data, filename = 'basic-line')
```





<iframe
    width="100%"
    height="525px"
    src="https://plotly.com/~nchae8/159.embed"
    frameborder="0"
    allowfullscreen
></iframe>





```python
print('hello world')
```

    hello world

