# Custom plotting utilities for matplotlib #

Some useful little tidbits for plotting in matplotlib.  Contains tools for
plotting timeseries (smoothed and annotated autocorrelation plots) and for
thinning down a collection of a large number of points in $n$ dimensions based
off of a minimum distance between any two points (rather like thinning
seedlings in a planting bed).

This latter tool works best for plotting scatterplots in 2D, potentially with
millions of datapoints, where a set of representative points (and weights
denoting how many actual points they represent) is desired, rather than a
density-histogram visualization (e.g. [datashader](https://datashader.org/)).
The representative-sample visualization may be more useful for showing the
overall spread of the data while preserving a sense for how tightly they
cluster about the central distribution.

Also contains the four-colour "Dark2" palette from
[colorbrewer](https://colorbrewer2.org/#type=qualitative&scheme=Dark2&n=4),
which should be readable for most people with some type of colour vision
deficiency.  Note that this palette is now available directly in matplotlib:
```python
from matplotlib import pyplot as plt
print(plt.cm.Dark2.colors)
```

Copied from [my other repo](https://github.com/max-veit/pyutils).
