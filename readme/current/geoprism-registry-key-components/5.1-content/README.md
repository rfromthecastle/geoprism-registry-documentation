# 5.1. Content

GeoPrism Registry is being used to simultaneously host, maintain, update and share **lists** as well as associated **hierarchies** and **spatial data** for the **geographic objects** core to development in general and public health in particular.

The following sections describe in more detail these different elements, as well as those associated with them (geographic features, geographic object types, data elements, classification tables).

Please refer to the latest Health GeoLab Collaborative [guidance](https://healthgeolab.net/DOCUMENTS/Guidance\_Common\_Geo-registry\_Ve2.pdf) on the establishment of a common geo-registry for the simultaneous hosting, maintenance, update and sharing of lists as well as associated hierarchies and spatial data, for specific considerations to take into account when developing such content before uploading it in GeoPrism Registry (quality, unique identifier, master versus non-master list, etc.).

## 5.1.1. Geographic features and geographic objects

Geographic features are features of the Earth, natural (e.g., rivers) or artificial (e.g., buildings), physical (e.g., roads) or abstract (e.g., administrative division). Each sector has its own set of geographic features that are core to the implementation of its programs and activities. Those core to the health sector, for example, include but are not limited to: health facilities, vaccination points, settlements, ambulances, patients, roads and administrative divisions.

GeoPrism Registry does nevertheless only handle geographic features for which it makes sense to establish and maintain a master list. These include fixed features such as health facilities, schools, bridges, or villages; artificially-created features such as administrative units, foci or health areas; or mobile features such as vehicles or individuals. A master list for other geographic features would either not be necessary (e.g., roads, rivers)\* or not applicable (e.g., continuous features like topography or population distribution). A geographic object, or **Geo-Object**, is itself the computer representation of a geographic feature. It can be represented as a point, line, or polygon on a map (more details on this in the next section).

\*_GeoPrism Registry does nevertheless provide the possibility to handle geographic objects represented by lines and can handle roads and rivers should master lists exist for them._

## 5.1.2. Geographic object types and groups

The types of geographic objects (a.k.a. **Geo-Object Types**) handled by GeoPrism Registry can be categorized based on how they would be represented on a map:

* Fixed geographic objects that can be simplified by a point, for example: household, health facility, human settlement
* Fixed geographic objects that should be represented by polygons due to their much larger extent, for examples: administrative units, health districts, or by a line due to their shape, for example: road, river
* Mobile geographic objects, for example: individuals, patients, vehicles; the geography of these objects would either be obtained by considering them attached to a fixed geographic object or by simplifying them as a point that would be located through their geographic coordinates (latitude and longitude) taken at a given point in time.

In GeoPrism Registry, these can be further aggregated into groups of geographic object types having the same attribute configuration (e.g., health facilities as a Geo-Object Type group could group health posts, health centers, and hospitals).

## 5.1.3. Data elements and classification tables

GeoPrism Registry focuses on all the information that allows to contextualize any piece of information in both space and time. It therefore only handles data elements meant to:

1. Uniquely identify,
2. Classify,
3. Locate, and
4. When applicable, contact

each geographic object it contains (the set of data elements referred to as the **signature domain**; see [Health Facility Technical Working Group (2007)](https://www.measureevaluation.org/resources/publications/wp-07-91.html)). Such a list will be specific to each type of geographic object hosted in the platform.

Other types of data elements, including programmatic ones (e.g., statistics), are not meant to be managed in GeoPrism Registry but in program-, or even sector-, specific information systems. Some of the reasons behind this are the sensitivities often linked to programmatic data, the difference in data flow between this type of data and the geographic objects they are attached to, as well as the difference in the management of the time dimension (e.g., the temporal validity of a statistic might be different from the temporal validity of the geographic object it is attached to). In addition, managing these data elements in these other systems allows the programs to benefit from functionalities that are not available within a registry, including, but not limited to, data collection, statistical analysis, or visualization (graphs, thematic maps).

The identification of the data elements to be associated with each geographic object and stored in GeoPrism Registry should take place as part of a process involving all concerned stakeholders. The result is a data dictionary containing at least the following information for each of the selected data elements (an example for a health facility master list is presented in Annex 2 of [Ebener (2022)](https://healthgeolab.net/DOCUMENTS/Guidance\_Common\_Geo-registry\_Ve2.pdf)):

* The data element code as implemented in GeoPrism Registry
* A short description of the data element
* The data element type
* The size of the data element (number of storage units)
* Whether the data element is considered as mandatory when adding a new record in the master list

Examples, notes, and, when applicable, the source (reference) of each data element can be added to the above information if it can help those in charge of managing GeoPrism Registry content and its users to have a clear understanding of each of these data elements. A classification table also needs to be defined for each of the data elements where the values are limited to a few options to ensure consistency across records, for example, type, ownership, etc. Such tables should at least contain the following for each option: a unique code, a label (English and local language) and/or acronym, a description (English and local language), and, when applicable, the source of the definition. The following table provides an example of a classification table for health facility types in Cambodia following this structure:

| Health facility type code | Acronym | Health facility type in English | Health facility type in Khmer | Definition                                                                                                                                                                                                                                                                         | Source of the definition                                                                        |
| ------------------------- | ------- | ------------------------------- | ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| 6                         | NH      | National Hospital               |                               | Health facility used to train health personnel and undertake research studies, in addition to providing specialized referral services.                                                                                                                                             | Modified from Ministry of Health, Cambodia (1998): _Guide for developing operational districts_ |
| 5                         | PH      | Provincial Hospital             |                               | Health facility under the administration and technical supervision of the Provincial Health Department. In the Health Coverage Plan, Provincial Hospitals function as Operational District Referral Hospitals and will also provide the Complimentary Package of Activities (CPA). | Modified from Ministry of Health, Cambodia (1998): _Guide for developing operational districts_ |
| 4                         | RH      | Referral Hospital               |                               | Health facility providing the CPA.                                                                                                                                                                                                                                                 | Modified from Ministry of Health, Cambodia (1998): _Guide for developing operational districts_ |
| 3                         | HC/B    | Health Center with Beds         |                               | Health facility delivering primary healthcare through the Minimum Package of Activities (MPA) and having beds for patients.                                                                                                                                                        | Modified from Ministry of Health, Cambodia (1998): _Guide for developing operational districts_ |
| 2                         | HC      | Health Center                   |                               | Health facility delivering primary healthcare through the MPA.                                                                                                                                                                                                                     | Modified from Ministry of Health, Cambodia (1998): _Guide for developing operational districts_ |
| 1                         | HP      | Health Post                     |                               | Health posts are located in remote areas and function as the lowest level within the district health system, and are thus the first point of contact with the population in low density provinces.                                                                                 | Modified from Ministry of Health, Cambodia (1998): _Guide for developing operational districts_ |

## 5.1.4. Hierarchies

Knowing how geographic objects relate to each other over time as part of different hierarchies is important not only to be able to aggregate information to support decision making, when applicable, but also to ensure relational consistency between geographic objects.

One of the functions of GeoPrism Registry is to capture and use not only geographic relationships that exist between geographic objects (is within, lives in) but also other types of relationships such as administrative (is reporting to), health-related (covers, providing service to, refers to), and associative (is part of).

These different relationships can be represented in distinct **hierarchies** like those included in Figure 1.

<figure><img src="../../../../.gitbook/assets/Screenshot 2022-11-01 141427.jpg" alt=""><figcaption><p>Figure 1: Example of hierarchies.</p></figcaption></figure>

## 5.1.5. Lists

A **list** is a tabular representation of the data elements associated with all the active, and past active, geographic objects (records) of a given type at a given point in time.

Lists represent the most familiar way for users to look at the information associated with any type of geographic object. When they are authoritative and curated by the mandated governmental entity, these lists, referred as **master lists** in this case, also serve as a ground reference to assess the completeness, uniqueness, timeliness, validity, and consistency of the geospatial data also hosted in a common geo-registry, as well as a denominator for the implementation of any public health program.

<figure><img src="../../../../.gitbook/assets/Screenshot 2022-11-01 141635.jpg" alt=""><figcaption><p>Extract of list corresponding to the data dictionary reported in Annex 2 of <a href="https://healthgeolab.net/DOCUMENTS/Guidance_Common_Geo-registry_Ve2.pdf">Ebener (2022)</a>.</p></figcaption></figure>

## 5.1.6. Spatial data

Also referred to as spatial data, **geospatial data** corresponds to information about the locations and shapes of geographic features and the relationships between them, usually stored as coordinates and topology (e.g., geographic location of health facilities, boundaries of administrative units…).

As GeoPrism Registry only handles types of geographic objects that can be managed in a list, it stores these in vector format geographic information system (GIS) layers. Raster format GIS layers cannot be uploaded to the platform.

GeoPrism Registry is able to handle the three modes of representation of geographic features in the vector format: points, lines, or polygons (Figure 2).

<figure><img src="../../../../.gitbook/assets/Screenshot 2022-11-01 141959.jpg" alt=""><figcaption><p>Figure 2: Modes of representation in the vector format: (a) points, (b) lines, and (c) polygons</p></figcaption></figure>

## 5.1.7. Data quality

The content hosted in GeoPrism Registry is meant to serve as the source of truth (ground reference) for any information system to properly contextualize, visualize, and analyze business data in both space and time. As such, this content is meant to present the highest level of quality possible across the six dimensions of data quality (uniqueness, completeness, timeliness, accuracy, validity, and consistency).

While GeoPrism Registry is meant to help improve and maintain the quality of this content across these dimensions, the higher the quality of this content at the time of uploading it in the platform, the lesser the work afterwards and the faster positive impacts can be seen.

The quality of the content before its upload in the platform can be ensured through the implementation of good data management practices throughout the overall geospatial data management cycle in Figure 3. The implementation of this cycle, and associated good practices, should ideally take place as part of the activities of the National Spatial Data Infrastructure (NSDI).

If an NSDI is not in place, the [reference material](https://healthgeolab.net/resources/reference-materials/) from the Health GeoLab Collaborative can be consulted to ensure the quality of the data and information to be uploaded in the platform.

<figure><img src="../../../../.gitbook/assets/Screenshot 2022-11-01 142310.jpg" alt=""><figcaption><p>Figure 3: Geospatial data management cycle.</p></figcaption></figure>
