:tocdepth: 1

.. sectnum::

.. Metadata such as the title, authors, and description are set in metadata.yaml

Abstract
==========

This technote shows analysis of the drift during tracking.

Drift during tracking uses the following files in `lsst-sitcom/notebooks_vandv <https://github.com/lsst-sitcom/notebooks_vandv/>`__
in the ``notebooks/tel_and_site/subsys_req_ver/tma/`` directory:

- ``LVV-T2738-ST_PTT_Tracking_drift_check.ipynb``

Methodology
================

The goal of this study was to analyze the drift rate while tracking in March 2023. 

This was done using the RA and DEC data in RubinTV. 

.. image:: ./_static/historical.png
  :width: 300px

.. image:: ./_static/download_metadata.png
  :width: 700px

Grabbing the json file from the Rubin TV and reading out calculated RA, calculated DEC, and time information, 
we selected the sequence numbers based on the night logs in 
`Startracker night logs <https://confluence.lsstcorp.org/pages/viewpage.action?spaceKey=LSSTCOM&title=StarTracker+Night+Logs>`__

This analysis was done for the data taken while tracking testing was done on 2023/03/09 and 2023/03/24.



Results
===========

We ran the notebook to take 1800 images each from all 3 generic cameras (startrackers and DIMM camera) while tracking, on 2023/03/09. 

On 2023/03/24, grid test was done with tracking. Here are example plots from 2023/03/24.

.. image:: ./_static/ra_dec_drift_2023_0324_22_64.png
  :width: 700px

.. image:: ./_static/ra_dec_drift_2023_0324_402_444.png
  :width: 700px

.. image:: ./_static/ra_dec_drift_2023_0324_746_788.png
  :width: 700px

Figure 1.  Calculated RA and DEC and residuals during the tracking.

.. image:: ./_static/draft_velocity_hist.png
  :width: 700px

Figure 2.  Coordinate Draft velocity and Angular Draft Velocity Histograms




