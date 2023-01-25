# Python Scripting Cheat Sheet
Patterns I use all the time in Python scripts. 

Create a path that leads to the 'data' directory located wherever the executed script is located. Create the 'data' directory if it does not exist.
```
dirname = os.path.dirname(__file__)
results_dir = os.path.join(dirname, 'data')
if not os.path.isdir(results_dir):
    os.mkdir(results_dir)
```

Execute code only when it is run in a script context (as opposed to a module context).
```
if __name__ == '__main__':
    pass
```

Assemble the team.
```
import numpy as np
import maptlotlib.pyplot as plt
import matplotlib as mpl
import pandas as pd
import seaborn as sns
import os
import sys
import uuid
import pdb
import shelve
```
