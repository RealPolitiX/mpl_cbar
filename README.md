# mpl_cbar
Colorbar is an object under matplotlib.colorbar. There are, in general, two ways to construct a colorbar using matplotlib

Colorbar constructed directly from plot
1. Position of colorbar is preset (defaulted to the right of the plot)
2. A natural link to an existing plot
```
Example:
fig, ax = plt.subplots()
img = ax.plot/imshow/pcolor(mesh)/contour(f)/...()
cbar = plt.colorbar(img, ...)
```

Colorbar constructed using a separate axis attached to a figure
1. Can set positions separately
2. Can construct standalone colorbar
```
Example:
fig, ax = plt.subplots()
cbar_ax = fig.add_axes([left, bottom, width, height], frameon=True)
img = ax.plot/imshow/pcolor(mesh)/contour(f)/...()
fig.colorbar(img, cax=cbar_ax, ...)
```
In either way, the colorbar constructed inherits the properties of an Axes class, its properties can be set in the same way as an Axes object, the following is a list of common setting parameters.
```
cbar.set_label("...", fontsize=xx, labelpad=xx)
    .set_ticks()
    .set_axis_off() or .axis('off')        # remove both frame and ticks
    .outline.set_visible(False)            # remove frame but keep ticks

cbar.ax.tick_params(labelsize=xx)
    .ax.set_xticklabels(["a", "b", "c",...])
    .ax.set_yticklabels(["a", "b", "c",...])
    .ax.invert_xaxis()
    .ax.invert_yaxis()
```

Set alternative labels for colorbar
```
cbar = fig.colorbar(img, ticks=old_ticklabels, orientation='vertical')
cbar.ax.set_yticklabels(new_ticklabels)
```

Colorbar normalization: https://matplotlib.org/users/colormapnorms.html
