# mpl_cbar
List of colorbar tweaks in matplotlib

Colorbar is an object under matplotlib.colorbar. There are, in general, two ways to construct a colorbar using matplotlib

Colorbar constructed directly from plot
1. Position of colorbar is preset
2. A natural link to an existing plot
```
Example:
img = ax.plot/imshow/pcolor(mesh)/contour(f)/...()
cbar = plt.colorbar(img, ...)
```

Colorbar constructed using a separate axis
1. Can set positions separately
2. Can construct standalone colorbar
```
Example:
```
In either way, the colorbar constructed inherits the properties of an Axes class, its properties can be set in the same way as an Axes object, the following is a list of common setting parameters.
```
cbar.set_label()
cbar.ax.tick_params()
```
