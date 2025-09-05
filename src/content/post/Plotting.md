---
title: Data Visualization using Matplotlib and Seaborn - Part 1
description: Creating Beautiful Plots 
dateFormatted: Sep 05, 2025
---

I have been trying to come up with good ways of producing high quality visualizations for research papers and / or presentations. While there may be specific requirements through publishers and personal preferences, I have always grappled with understanding what constitues a good visualization. In this post, I will try to develop my personal thesis / brand on what constitues a good plot/chart/visualization.

```python showLineNumbers=false

import matplotlib.pyplot as plt
import numpy as np

# Set clean style
plt.rcParams.update({
    'font.size': 12,
    'axes.linewidth': 1,
    'axes.spines.top': False,
    'axes.spines.right': False,
    'figure.dpi': 150
})

# Generate simple data
x = np.linspace(0, 10, 100)
y = 2 * np.sin(x) + 0.5 * x + np.random.normal(0, 0.1, 100)

# Create the plot
fig, ax = plt.subplots(figsize=(8, 5))

# Simple line plot
ax.plot(x, y, color='#2E86AB', linewidth=2)

# Labels
ax.set_xlabel('Time (s)')
ax.set_ylabel('Signal Amplitude')
ax.set_title('Signal over Time')

# Clean up
plt.tight_layout()
plt.show()
```

(Living Document)