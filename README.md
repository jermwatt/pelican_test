

```python
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np
from IPython.html import widgets

t = np.arange(0.0, 1.0, 0.01)

        
def pltsin(f):
    fig = plt.figure(num=None, figsize=(12,4), dpi=80, facecolor='w', edgecolor='k')
    a = plt.subplot(131)
    a.plot(t,np.sin(2*np.pi*t*f))
    a.figsize = (3,3)
    a.axis('off')
    
    a = plt.subplot(132)
    a.plot(t,np.cos(2*np.pi*t*f))
    a.figsize = (3,3)
    a.axis('off')

    a = plt.subplot(133)
    a.plot(t,np.sin(np.cos(2*np.pi*t*f)))
    a.figsize = (3,3)
    a.axis('off')

widgets.interact(pltsin, f=(1,10,1));
```
