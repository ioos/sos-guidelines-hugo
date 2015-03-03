# About SOS Guidelines

U.S. IOOS distributes ocean observations using the OGC Sensor Observation Service.  To support this effort U.S. IOOS has developed a profile of SOS v1.0 (henceforth IOOS SOS v1.0) that includes specific behaviors for the SOS interface and for the output formats delivered in response to the three operations of the SOS Core Profile.  This repository contains documentation of the IOOS SOS v1.0 profile, example templates for the responses, and information on two reference implementations developed to support the IOOS SOS v1.0 profile.  To facilitate the practical implementation of the SOS, IOOS has developed the IOOS Application Profile (AP) for SOS, which includes a series of operation templates, controlled vocabularies, IOOS Conventions for SOS Implementation, and a set of tests for IOOS SOS implementations.

## Contents

+ [Documentation of the Profile](#documentation-of-the-profile)
+ [Templates and Examples](#templates-and-examples)
+ [Reference Implementations and Current Deployments](#reference-implementations-and-current-deployments)


## Documentation of the Profile
 * _**Web Service Description Document (WSDD)**_ - provides a description of the IOOS Sensor Observation Service (SOS) Profile that has been developed by U.S. IOOS for deployment by NOAA data providers and IOOS Regional Associations (RAs).
 * _**List of SOS Tests**_ -  describes a collection of tests that have to be run in order to ensure a required level of compliance with IOOS SOS Profile 1.0 and official OGC SOS 1.0.0 specification.
 * _**IOOS SOS Templates**_ - explicitly define the IOOS SOS operation responses for the CF feature types “point”, “timeSeries”, and “timeSeriesProfile”.

The IOOS SOS 1.0 is conformant to the following OGC Standards and Conventions: 
* [OpenGIS Sensor Observation Service v1.0.0 [OGC 06-009r6]](http://www.opengeospatial.org/standards/sos), for provision of observational data; 
* [OpenGIS Sensor Model Language (SensorML) v1.0.1 [OGC 07-000 and 07-122r2]](http://www.opengeospatial.org/standards/sensorml), for platform and sensor description and result encoding;  and
* [OGC® SWE Common Data Model Encoding Standard v2.0 [OGC 08-094r1]](http://www.opengeospatial.org/standards/swecommon), for result encoding options. 
* [CF Conventions v1.6](http://cfconventions.org), for provision of standard naming and description of feature types, data components, dimensions, variables and attributes, coordinate systems definition, axis order, etc.

 IOOS Conventions for the AP v1 is described in the series of documents:
* [IOOS SOS Web Service Description Document](http://ioos.github.io/sos-guidelines/doc/wsdd/sos_wsdd_github_notoc/), which provides a detailed description of the IOOS implementation of the OGC SOS v1.0.0, including definitions, constraints, encoding requirements and “best practices” that are not explicitly defined in OGC SOS Implementation Standard;
* [Convention for Observing Asset Identifiers](http://ioos.github.io/conventions-for-observing-asset-identifiers), which describes the algorithm for identification of IOOS-related observing assets including measurement stations, platforms and sensors; [Temporary URL](https://github.com/ioos/conventions-for-observing-asset-identifiers)
* [Convention for CSV/TSV Encoding](http://ioos.github.io/ioos-csv-tsv/), which lays down rules for encoding observation data as plain text Comma-Separated Values (CSV) or Tab-Separated Values (TSV);
* [Guidelines for use of Controlled Vocabularies](https://github.com/ioos/vocabularies), which provides instructions for usage of the controlled vocabularies and vocabulary mappings developed or adopted by IOOS in IOOS-compliant data services, including existing vocabulary and terms selection process as well as request policy for new terms.  Most controlled vocabularies used by IOOS are hosted on the [Marine Metadata Interoperability](https://marinemetadata.org/) [Ontology Registry and Repository](http://mmisw.org/orr/) in the [IOOS folder](http://mmisw.org/ont/ioos).

## Templates and Examples
[SOS Operation Templates for IOOS AP v1](https://github.com/ioos/sos-guidelines/tree/master/template) include templates for SOS v1.0.0 GetCapabilities, DescribeSensor, and GetObservation server's response. The GetObservation templates describe 'point', 'timeSeries', 'profile', and 'timeSeriesProfile' [CF v1.6 Discrete Sampling Geometries](http://cfconventions.org/Data/cf-conventions/cf-conventions-1.6/build/cf-conventions.html#discrete-sampling-geometries). The templates are intended as a mandatory guidance for all developers of IOOS-compliant SOS applications.

In 2015-2016 IOOS is planning to move to IOOS SOS v2.0. A new Application Profile (AP v2) is anticipated to modify IOOS Conventions and current templates to accommodate the [OGC SOS v2.0 Interface Standard [OGC 12-006]](http://www.opengeospatial.org/standards/sos), including the Obsevations and Measurements  v2.0, Sensor Web Enablement v2.0, and SensorML v2.0 standards.  Additionally, templates will also be added for 'trajectory' and 'trajectoryProfile' CF v1.6 Discrete Sampling Geometries. 

## Reference Implementations and Current Deployments
1. [i52N](https://github.com/ioos/i52n-sos) for RDBMS observation data store (IOOS custom version of the [52°North Sensor Observation Service](https://github.com/52North/SOS), and 
2. [ncSOS](https://github.com/asascience-open/ncSOS) that adds an SOS service to any of the CF Discrete Sampling Geometries datasets in the existing [THREDDS server](http://www.unidata.ucar.edu/projects/THREDDS/). 

### Conformance Testing
Similar to OGC Compliance & Interoperability Testing & Evaluation (CITE) program, IOOS has developed a set of formal tests to ensure that IOOS SOS implementations are providing a product compliant with the IOOS AP v1. The [IOOS AP v1 Compliance Test List](http://ioos.github.io/sos-guidelines/doc/testing/sos_test_list_github_notoc_summary/) describes tests for SOS v1.0.0 developed by IOOS, and indicates optional some OGC CITE tests that are considered non-critical for the current state of IOOS SOS implementation.

A testing framework for use as a web service and as a command line tool is [being developed as well](https://github.com/ioos/ioos-sos-compliance-tests).  

### Current Deployments

The complete list of all known IOOS SOS deployments can be found at the [IOOS Catalog](http://catalog.ioos.us/services/filter/none/SOS). 

IOOS Federal and RA partners are expected to register their DMAC data access services with the IOOS Service Registry hosted and operated by NGDC. The Service Registry maintains the master list of data sets available via DMAC data access services, and allows discovery of IOOS services and data via the [NGDC ESRI Geoportal Server's web based GUI](http://www.ngdc.noaa.gov/geoportal/) or via direct queries using the OGC CS/W interface or the ESRI REST interface, e.g. the query for [all IOOS SOS services](http://www.ngdc.noaa.gov/geoportal/rest/find/document?rid=local&ridName=NOAA%27s%20Geophysical%20Data%20Center&rids=local&searchText=sos.resource.url:*%20&start=1&max=1000&orderBy=relevance&maxSearchTimeMilliSec=10000&f=html). The [IOOS Service Registry](https://github.com/ioos/registry) documentation provides detailed instructions for IOOS partners on getting dataset metadata into the Service Registry.

The [IOOS Catalog](http://catalog.ioos.us/) is intended to be the web-based client for the Service Registry and to provide a view of the data published via the registered services. Currently, the Catalog provides information under 1000 registered SOS services and 4000 data sets.  The Catalog obtains all service URLs from the metadata managed by the IOOS Service Registry via OGC CS-W interface to the NGDC's ESRI Geoportal Server. The [GitHub software repository](http://catalog.ioos.us/) contains the source code for generation of the IOOS Catalog web site.


## Documentation Generation
The documentation in the [sos-guidelines](https://github.com/ioos/sos-guidelines) repository is organized in the following order: 

```
   ioos/sos-guidelines/
    ├── doc/
    |    ├── testing/
    |    |    └── sos_test_list_github_notoc_summary.md
    |    └── wsdd/ 
    |         └── sos_wsdd_github_notoc.md
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
The rest of repository content is placed there only for website deployment with the [_**Hugo**_](http://hugo.spf13.com/) static page generator. The [_**Hosting on IOOS GitHub Pages Workflow**_](http://ioos.github.io/website_deployment_workflow_updated) located on the [IOOS GitHub top webpage](http://ioos.github.io/) describes the deployment workflow in more details.
