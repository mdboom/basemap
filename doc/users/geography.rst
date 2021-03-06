.. _geography:

Drawing a Map Background
========================

Basemap includes the 
`GSSH <http://www.soest.hawaii.edu/wessel/gshhs/gshhs.html>`_
coastline dataset, as well as datasets for rivers, state and
country boundaries from 
`GMT <http://gmt.soest.hawaii.edu>`_.
These datasets can be used to draw coastlines, rivers and political
boundaries on maps at several different resolutions.  The relevant Basemap 
methods are:

* :func:`~mpl_toolkits.basemap.Basemap.drawcoastlines`: draw coastlines.
* :func:`~mpl_toolkits.basemap.Basemap.fillcontinents`: color the interior
  of continents (by filling the coastline polygons).
* :func:`~mpl_toolkits.basemap.Basemap.drawcountries`: draw country boundaries.
* :func:`~mpl_toolkits.basemap.Basemap.drawstates`: draw state boundaries
  in North America.
* :func:`~mpl_toolkits.basemap.Basemap.drawrivers`: draw rivers.

Instead of drawing coastlines and political boundaries, an image can be
used as a map background.  Basemap provides several options for this:

* :func:`~mpl_toolkits.basemap.Basemap.drawlsmask`: draw a high-resolution 
  land-sea mask as an image, with land and ocean colors specified.
* :func:`~mpl_toolkits.basemap.Basemap.bluemarble`: draw a NASA
  `Blue Marble <http://visibleearth.nasa.gov/view_set.php?categoryID=2363>`_
  image as a map background.
* :func:`~mpl_toolkits.basemap.Basemap.warpimage`: use an abitrary
  image as a map background.  The image must be global, covering the
  world in lat/lon coordinates from the international dateline eastward
  and the South Pole northward.

Here are examples of the three different ways to draw a map background.

1. Draw coastlines, filling ocean and land areas.

.. literalinclude:: figures/background1.py

.. image:: figures/background1.png

2. Draw a land-sea mask as an image.

.. literalinclude:: figures/background2.py

.. image:: figures/background2.png

3. Draw the NASA 'Blue Marble' image.

.. literalinclude:: figures/background3.py

.. image:: figures/background3.png
