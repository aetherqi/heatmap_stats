# heatmap_stats
Modified Seaborn correlation heatmap to change size of heatmap cells (e.g. proportional to p-value) and addition of dot to signify passing of false discovery rate criteria.

```python
from . import heatmap_stats
heatmap_stats.heatmap_stats(r, ax=ax, 
                                fmt='.1f', annot_kws={"size": 10},
                                mask=mask, cmap=cmap,
                                cellsize=1 - np.cbrt(p_vals),
                                square=True, annot=p_rejected, fdr=True)
```
