# tricks
Tips & tricks

## matplotlib

### Include legend bar at whichever position
```
cm=pl.cm.cool
sm=pl.cm.ScalarMappable(cmap=cm)
sm.set_array([])

f = pl.figure()
ax = f.add_axes([0.05, 0.80, 0.9, 0.15])
pl.colorbar(sm, cax=ax,orientation='horizontal')

```
