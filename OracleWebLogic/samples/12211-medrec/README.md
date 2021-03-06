Example of Image with WLS Domain
================================
This Dockerfile extends the Oracle WebLogic image by installing the Supplemental package of WebLogic which includes the MedRec WLS sample.

# How to build and run
First make sure you have built **oracle/weblogic:12.2.1.1-developer**. 

Then download file [fmw_12.2.1.1.0_wls_supplemental_quick_Disk1_1of1.zip](http://www.oracle.com/technetwork/middleware/weblogic/downloads/wls-for-dev-1703574.html) and place it next to this README.

To build, run:

        $ docker build -t 12211-medrec .

To start the Admin Server, run:

        $ docker run -d -p 7011:7011 12211-medrec

When you run the container a MedRec domain is created and the server started. To access the MedRec application, go to:

        http://localhost:7011/medrec

# Copyright
Copyright (c) 2015 Oracle and/or its affiliates. All rights reserved.
