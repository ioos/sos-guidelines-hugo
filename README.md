This repository contains materials that describe the IOOS SOS Profile v1.0:

 * _**Web Service Description Document (WSDD)**_ - provides a description of the IOOS Sensor Observation Service (SOS) Profile that has been developed by U.S. IOOS for deployment by NOAA data providers and IOOS Regional Associations (RAs).
 * _**List of SOS Tests**_ -  describes a collection of tests that have to be run in order to ensure a required level of compliance with IOOS SOS Profile 1.0 and official OGC SOS 1.0.0 specification.
 * _**IOOS SOS Templates**_ - explicitly define the IOOS SOS operation responses for the CF feature types “point”, “timeSeries”, and “timeSeriesProfile”.
 
The documentation in the [sos-guidelines](https://github.com/ioos/sos-guidelines) repository is organized in the following order: 
```
   ioos/sos-guidelines/
    ├── doc/
    |    ├── testing/
    |    |    └── sos_test_list_github_notoc_summary.md
    |    └── wsdd/ 
    |         ├── sos_wsdd_github_notoc.md    
    |         └── sos_wsdd_github_toc.md
    ├── template/
    |    └── milestone 1.0/
    |          ├── OM-GetObservation.xml
    |          ├── SML-DescribeSensor-Network.xml
    |          ├── SML-DescribeSensor-Station.xml
    |          ├── SOS-GetCapabilities.xml
    |          ├── SWE-MultiStation-TimeSeries.xml
    |          ├── SWE-MultiStation-TimeSeries_QC.xml
    |          ├── SWE-SingleStation-SingleProperty-TimeSeries.xml
    |          ├── SWE-SingleStation-TimeSeriesProfile.xml
    |          └── SWE-SingleStation-TimeSeriesProfile_QC.xml
    └── README.md
```      

The rest of repository content is placed there only for website deployment with the _**Hugo**_ static page generator. The deployment workflow is described in the [_**Website Deployment Workflow**_](sos-guidelines/Website_Deployment_Workflow.md) document located in the root directory next to this _README_.