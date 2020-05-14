---
layout: post
title: "jupyter note test 2"
categories: misc
---

# 이병문 정성훈

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

py.iplot(data, filename = 'basic-line2')
```





<iframe
    width="100%"
    height="525px"
    src="https://plotly.com/~nchae8/162.embed"
    frameborder="0"
    allowfullscreen
></iframe>





```python
print('hello world')
```

    hello world



```python

import pandas as pd

# load dataset
df = pd.read_csv("https://raw.githubusercontent.com/plotly/datasets/master/volcano.csv")

# create figure
fig = go.Figure()

# Add surface trace
fig.add_trace(go.Surface(z=df.values.tolist(), colorscale="Viridis"))

# Update plot sizing
fig.update_layout(
    width=800,
    height=900,
    autosize=False,
    margin=dict(t=0, b=0, l=0, r=0),
    template="plotly_white",
)

# Update 3D scene options
fig.update_scenes(
    aspectratio=dict(x=1, y=1, z=0.7),
    aspectmode="manual"
)

# Add dropdown
fig.update_layout(
    updatemenus=[
        dict(
            buttons=list([
                dict(
                    args=["type", "surface"],
                    label="3D Surface",
                    method="restyle"
                ),
                dict(
                    args=["type", "heatmap"],
                    label="Heatmap",
                    method="restyle"
                )
            ]),
            direction="down",
            pad={"r": 10, "t": 10},
            showactive=True,
            x=0.1,
            xanchor="left",
            y=1.1,
            yanchor="top"
        ),
    ]
)

# Add annotation
fig.update_layout(
    annotations=[
        dict(text="Trace type:", showarrow=False,
        x=0, y=1.085, yref="paper", align="left")
    ]
)

# fig.show()
py.iplot(fig, filename = 'test_3D')
# fig.write_html('sec_figure.html', auto_open=True)


```





<iframe
    width="800px"
    height="900px"
    src="https://plotly.com/~nchae8/164.embed"
    frameborder="0"
    allowfullscreen
></iframe>





```python

```
