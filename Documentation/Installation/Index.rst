﻿.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../Includes.txt


.. _installation:

Installation
============

#. **Install ext:fal_securedownload**

   Download and install fal_securedownload through extension manager or clone from https://github.com/beechit/fal_securedownload.git in typo3conf/ext/

#. **Create non public file storage (under rootlevel)**

   Un-check the 'public' checkbox for your existing file storage or create a new file storage and set it to non public

   .. figure:: ../Images/secure-file-storage.png
      :width: 400px
      :alt: Create non-public file storage

      **Image 1:** Create non-public file storage

   Best is to have the physical folder outside of your document root. If not, add an .htaccess with "Deny from all" (Apache < 2.3) or "Require all denied" (Apache >= 2.3) in your file storage root folder.


#. **Configure lockRootPath !!! Required >11.5.35 & >12.4.11**

   Refer to the TYPO3 Backend Configuration to ensure paths outside the project path are restricted for added security.
   https://docs.typo3.org/m/typo3/reference-coreapi/main/en-us/Configuration/Typo3ConfVars/BE.html#confval-globals-typo3-conf-vars-be-lockrootpath

#. **Set permissions**

   Set fe_group permissions to a file or folder of the non-public file storage

   .. figure:: ../Images/set-folder-permissions.png
      :width: 400px
      :alt: Set FE permissions for folder

      **Image 2:** Set FE permissions for folder though context menu item

   .. figure:: ../Images/set-folder-permissions2.png
      :width: 400px
      :alt: Set FE permissions for folder

      **Image 3:** Set FE permissions for folder though button in button bar



