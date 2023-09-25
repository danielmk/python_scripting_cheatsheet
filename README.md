# Python Scripting Cheat Sheet
Patterns I use all the time in Python scripts. 


```python
# Create a path that leads to the 'data' directory located wherever the executed script is located. Create the 'data' directory if it does not exist.
dirname = os.path.dirname(__file__)
results_dir = os.path.join(dirname, 'data')
if not os.path.isdir(results_dir):
    os.mkdir(results_dir)
```


```python
# Execute code only when it is run in a script context (as opposed to a module context).
if __name__ == '__main__':
    pass
```

```python
# Assemble the team.
import numpy as np
import matplotlib.pyplot as plt
import matplotlib as mpl
import pandas as pd
import seaborn as sns
import os
import sys
import uuid
import pdb
import shelve
```

```python
# Get the date and time. This is mainly for usage in unique file names that save script output.
from datetime import datetime
now = datetime.now().strftime("%Y-%m-%d_%H-%M-%S")
```

```python
# Open a shelve in a with context
with shelve.open(save_path) as ms:
    pass
```

```python
# Get all file names in results_dir that contain 'pattern'
file_names = [x for x in os.listdir(results_dir) if 'pattern' in x]
```

```python
# OIST official color theme for figures
['#C70019', '#0D6B9A', '#EE9A20', '#6389A5', '#EA521C', '#8A963F']
```

```python
# Create figure with panels organized in r rows and c columns
fig, ax = plt.subplots(r, c)
```

```python
# Make font in .svg actual font
plt.rcParams['svg.fonttype'] = 'none'
```
