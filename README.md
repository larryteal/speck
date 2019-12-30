![speck](https://i.imgur.com/nE4Xhac.png)
======

[![Python 3.6](https://img.shields.io/badge/python-3.6+-blue.svg)](#)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)


Render images as a set of continuous lines representing each horizontal row of pixels:
- Line width varies with greyscale pixel darkness.
- Set line width range. Lower range effectively reduces contrast
- Add noise profiles to introduce randomness
- Add colour profiles to vary line colours

## Example:

```python
from speck.draw import SpeckPlot
from speck.noise import SineNoise
from speck.colour import CmapColour

s = SpeckPlot.from_path('...')

s.draw(
    y_range=(0.2, 0.6),
    noise=SineNoise(scale=0.7),
    colour=CmapColour('Oranges')
)
```

![Example](https://i.imgur.com/SHUMebO.png)