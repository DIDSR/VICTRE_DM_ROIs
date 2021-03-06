# VICTRE Digital Mammography ROIs
![](https://user-images.githubusercontent.com/5750606/41682198-0b250648-74a5-11e8-9578-f93602efa5ab.png)\
***Virtual Imaging Clinical Trial for Regulatory Evaluation***

Clinical trials are expensive and delay the regulatory evaluation and early patient access to novel devices. In order to demonstrate an alternative approach, a recent effort at the Division of Imaging, Diagnostics, and Software Reliability at the U.S. Food and Drug Administration (known as the VICTRE project) demonstrated the replication of one such clinical trial using completely in-silico tools and compared results in terms of imaging modality performance between the human trial and the computational trial. The VICTRE trial involved imaging approximately 3000 digital breast models in digital mammography and digital breast tomosynthesis system models. VICTRE pipeline tools and details are available at https://github.com/DIDSR/VICTRE/. 

The last component of the VICTRE pipeline is Regions of Interest (ROIs) extraction. **On this page we make available the VICTRE dataset' ROI patches for digital mammography.** The ROI patches for digital breast tomosynthesis are available at https://github.com/DIDSR/VICTRE_DBT_ROIs.

**Citation:** ''Evaluation of Digital Breast Tomosynthesis as Replacemnet of Full-Field Digital Mammography Using an In Silico Imaging Trial.'' Aldo Badano, Ph. D., Christian G. Graff, Ph. D., Andreu Badal, Ph. D., Diksha Sharma, M. Sc., Rongping Zeng, Ph. D., Frank W. Samuelson, Ph. D., Stephen Glick, Ph. D., and Kyle J. Myers, Ph. D.  *JAMA Network Open. 2018;1(7):e185474; [doi:10.1001/jamanetworkopen.2018.5474]( https://doi.org/10.1001/jamanetworkopen.2018.5474)*. 

*VICTRE team: Aldo Badano, Ph. D., Christian G. Graff, Ph. D., Andreu Badal, Ph. D., Diksha Sharma, M. Sc., Rongping Zeng, Ph. D., Frank W. Samuelson, Ph. D., Stephen Glick, Ph. D., and Kyle J. Myers, Ph. D.*

Disclaimer
----------

This software and documentation (the "Software") were developed at the Food and Drug Administration (FDA) by employees of the Federal Government in the course of their official duties. Pursuant to Title 17, Section 105 of the United States Code, this work is not subject to copyright protection and is in the public domain. Permission is hereby granted, free of charge, to any person obtaining a copy of the Software, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, or sell copies of the Software or derivatives, and to permit persons to whom the Software is furnished to do so. FDA assumes no responsibility whatsoever for use by other
parties of the Software, its source code, documentation or compiled executables, and makes no guarantees, expressed or implied, about its quality, reliability, or any other characteristic. Further, use of this code in no way implies endorsement by the FDA or confers any advantage in regulatory decisions. Although this software can be redistributed and/or modified freely, we ask that any derivative works bear some notice that they are derived from it, and any modified versions bear some notice that they have been modified. 

Data organization
-----------------
The VICTRE ROI patches for digital mammography for the four breast density categories (extremely dense, heterogenously dense, scattered density, and fatty) are available in the four folders. Each folder contains gzipped files with ROI patches for signal absent and signal present phantoms. Two types of signals were inserted - microcalcification cluster and spiculated mass. 

Gzip files can be extracted using WinZip on Windows or from the command line in Linux with $tar -xvzf gzip-filename.

*Viewing the ROI patches:* The patches can be opened in [ImageJ](https://imagej.nih.gov/ij/) with the following parameters:

- Microcalcification cluster signal present and signal absent - 65x65 pixels image, 32-bit Real, Little-endian byte order.
- Spiculated mass signal present and signal absent - 109x109 pixels image, 32-bit Real, Little-endian byte order.

There are approximately 2800 ROIs each for extremely dense and fatty breast categories, and over 11200 ROIs for heterogeneously dense and scattered density types.

File naming
-----------
Individual ROI patches are named as roiMAMMO_X_Y_Z.raw, where X denotes signal absent (SA) or signal present (SP), Y is the ROI index of phantom, Z is the seed number of the phantom. Each seed denotes a different phantom, and files containing same seed are different ROI patches from the same phantom.

