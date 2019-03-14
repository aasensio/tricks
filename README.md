# tricks
Tips & tricks

## matplotlib

### Include legend bar at whichever position

http://matplotlib.org/examples/api/colorbar_only.html

```
cm=pl.cm.cool
sm=pl.cm.ScalarMappable(cmap=cm)
sm.set_array([])

f = pl.figure()
ax = f.add_axes([0.05, 0.80, 0.9, 0.15])
pl.colorbar(sm, cax=ax,orientation='horizontal')

```

## Videos

### Generate a gif from an mp4
```
ffmpeg -y -ss 30 -t 3 -i input.mp4 -vf fps=10,scale=320:-1:flags=lanczos,palettegen palette.png
ffmpeg -ss 30 -t 3 -i input.mp4 -i palette.png -filter_complex "fps=10,scale=320:-1:flags=lanczos[x];[x][1:v]paletteuse" output.gif

```
