:tocdepth: 1

.. sectnum::

.. Metadata such as the title, authors, and description are set in metadata.yaml

Abstract
========

This technote shows analysis of the drift during tracking.

Drift during tracking uses the following files in `lsst-sitcom/notebooks_vandv <https://github.com/lsst-sitcom/notebooks_vandv/>`__
in the ``notebooks/tel_and_site/subsys_req_ver/tma/`` directory:


- ``LVV-T2738-ST_PTT_Tracking_drift_check.ipynb``

Methodology
================
The goal of this study was analyze the drift rate while tracking in March 2023. 
This was done using the RA and DEC data in RubinTV. 

This analysis was done for the data taken while tracking testing was done on 2023/03/09.



Results
================

After deriving slew profiles for each identified slew we used the following notebook to identify the maximum velocity, acceleration, and jerk experienced
Link here.

We ran the slew identification script ``create_slew_profiles.py`` on all nights between 31/03/2023 and 01/11/2022. The distribution of identified slews (using method 2, add method 1) is show in Figure 1.

.. image:: ./_static/date_hist.png

Figure 1.  date distribution of identified slews

Then for each of the identified slews we computed the maximum velocity, acceleration and jerk. Histograms of the maximums are shown in Figure 2. The top row shows histograms for Azmiuth slews and the bottom for eleveation. The orange and red lines in each panel show the design and maximum limits respectively.

.. image:: ./_static/all_slews_max.png

Figure 2.  distribution of max velocities, accelerations and jerks for all identified azimuth and elevation slews


From this we flagged 19 slews as exceeding the maximum limits of the telescope. For each of these we created diagnostic plots example shown in Figure 3, and visually inspected the slews. All of the flagged ones had poor fits that when run by hand resulted in slew profiles that were within specifications.



.. image:: ./_static/example_slew_failure.png

Figure 3.  an example of 


The below table lists 

+------------+--------------+
|    Day     |  slew start  |
+============+==============+
| 2022-11-22 | 01:15:06.047 |
+------------+--------------+
| 2022-11-22 | 01:17:32.597 |
+------------+--------------+

Summary
==========================

This technote shows a summary of the tracking ....