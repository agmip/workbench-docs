Quick Start Guide
=================

This document will show you how to the AgMIP Workbench up and running quickly,
with support for the basic crop model tools for validation and packaging.

Installation
------------

*These instructions require an internet connection.*

Download and run the latest version of the AgMIP Workbench Installer for 
your platform from the `AgMIP Toolshed`_.

Go to *Tools -> Plugins*

Under **Available Plugins** check the three available packages.

Click **Install** and accept all the default values.
*(NOTE: We are currently updating our code signing keys and will have our code
signed in upcoming releases)*

Click **Close** on the *Plugins* window.


Import Your Dataset
-------------------

Click on the **Packaging** button in the workflow panel. If this panel is
missing, go to *Window -> Workflow*.

This will open up various panels which will be used by the validation and
packaging steps in the RIA Crop Model Workflow. On the left is the panel for
your files, the middle will be any files you open inside the editor (**this is
not recommended**) and logs for validation. The right panel will have the information
for your dataset, as well as the validation and packaging buttons.

To import your existing data, either click the `New Project..` button on the
toolbar, or go to *File -> New Project*. Choose the **AgMIP RIA Crop Model
Dataset** and click **Next**. Type in a name for your dataset and then click
**Browse** to choose the root directory for your dataset. Click **Finish** and
your project should appear in the project panel.

Please note that all files under this directory will be searched for AgMIP data.

Dataset Validation
------------------

To validate your dataset, click the **Validate Dataset** button in the
*Packaging* panel. This *may* take some time to complete, based on the size of
your dataset.

Identify Your Cultivar File(s)
------------------------------

In the *Project* panel, you can right click on a file and select **Mark as
Cultivar package**. These should be in the AgMIP Cultivar zip format. These
files are **NOT** currently validated and should be included with caution.

Package Your Dataset
--------------------

CLick on the **Package Dataset** to create a zip file containing your ACEB,
DOME, ACMO and CULTIVAR files. Please type the full name **INCLUDING .zip at the
end** and save. Only validated files will be included the packaged zip file.

The packaging completes the following tasks:

* Merge all ACEB files into one ACEB file, removing any duplicate data.

* Merge all DOME files into one DOME file, removing any duplicate data.

* Organize ACMO files according to the Crop Model activity (CM0-6).

* Rename ACMO files according to the AgMIP Protocols.

* Copies all cultivar zip files into the packaged zip file.

.. _AgMIP Toolshed: http://tools.agmip.org/
