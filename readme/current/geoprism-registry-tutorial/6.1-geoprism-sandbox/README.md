# 6.1 GeoPrism Sandbox

### 6.1.1 Purpose

The GeoPrism Registry sandbox is a controlled testing and demo environment that resets at 12:00 AM Geneva, Switzerland (GMT+1) every day. This allows users to test and learn about the GeoPrism Registry functionalities without the risk of affecting some specific content.

Because of the above, the sandbox is used as the reference for all the examples included in the present tutorial.

### 6.1.2 Organizations and roles

The Tolkien dataset has been designed in such a way that it is distributed among 3 organizations:

* Ministry of Home Affairs (MOHA)
* Ministry of Health (MOH)
* Ministry of Education (MOE)

For each of these organizations, a Registry Administrator (RA), Registry Maintainer (RM) and Registry Contributor (RC) user role has been created. Users can also access the demo instance as a System Administrator (SA). Please refer to the [CGR role section ](../../../../versions/current/geoprism-registry-key-components/#5.3-user-roles-and-their-rights)for more details on each of them.

### 6.1.3 Content

The sandbox contains fake data that has been generated in order to facilitate testing sessions and demos that would cover a large number of use cases including changes over time.

This “Tolkien land” was initially created for a training that took place in the Philippines in 2019. It has since been expanded for GPR demonstration purposes.

#### Geo-Object Types

As it currently stands, the Tolkien land dataset contains Geo-Object Types under the curation mandate of three different organizations as follows:

* Ministry of Home Affairs (MOHA)
  * Provinces - Polygons
  * Counties - Polygons
  * Shire - Polygons
  * Villages - Points
* Ministry of Health (MOH)
  * National Hospitals - Points
  * Referral Hospitals – Points
  * Health Centre – Points
  * Health Posts – Points
  * Catchment areas – Polygons
  * Community Health workers - Points
* Ministry of Education (MOE)
  * Universities - Points
  * Colleges - Points Secondary schools - Points
  * Primary schools - Points

#### Hierarchies

Organization specific hierarchies based on the above Geo-Object Types and the geographic location (latitude/longitude) or the geographic extent (polygon) of each Geo-Object are also being implemented in the dataset.

The hierarchies that were created per organization are as follows:

* MOHA
  * Administrative structure hierarchy: hierarchy showing how the different administrative divisions are aggregated from the lowest level to the highest.\
    ![](https://lh3.googleusercontent.com/4UsBNirqTK0IpOyc3fNSZjMC1YjokQAFKMBgvlNSJc8zeLUCVTXtpd3ggyBcAZOoAJctNYT0NahJiqdXXEZxUspxTkZ8NSPM7i7\_z-GPXJVwx-gwt9oGIsaWlhDXZhc5\_FG4C2ZAjMMqi-EpXKxgniJNYOieG7kBY2xE3L8qctSLAknn\_-MjME5d)
* MOH
  * Community Health Workers (CHW) - Health Post hierarchy: hierarchy linking each CHW to the health post she/he is reporting to\
    ![](https://lh3.googleusercontent.com/j1wjHMr6XV8aWsAx0gsE1a0nAHlMv0LwGon0pmQ0JArSpyJuVn0s7skJPhjAoia901W9q4XS7KicWlqeNY3oPHlBzt9x4b9HrIbjPezY6wdj5DT9p5e3aiK5D0zlR8i0CPN32URr2hEd\_-TofVNARBktra5vRH0MysSqSv94OM9BWO8bjfeIKpOL)
  * Health care referral hierarchy: hierarchy that describes how patients are being referred from the village to the national hospital level\
    ![](https://lh6.googleusercontent.com/wMYOwYZMl6dagIUS3L7V\_vWofo5duYia-TdEU\_8IGpQoys5g2vOqtDzxT-g0FukNln0-WSG6RBHM75Uk-uw\_m5u5KzgkS-eXdypd09WYdhAkFU6mYmjKjWA3e4JbB1AoBaPPAY9XwjYTavv7UhYvroJleUbTozgC72mIOcbbpyH4fnisISZrUMEa)
  * Health geography hierarchy: hierarchy that allows to link each health facility with the Shire in which it is located\
    ![](https://lh5.googleusercontent.com/gQLefeAo5O9U1KfMVbWth17LvEN8JOKiukH0ftIPbn6tOjdBOPaq6Z\_n5UhCaARpmJTPHyiBQ5X0QpTlpI-UQiuPaPnGEXlWc3z3DsyWBA3MqeVlvFqwWVhrqgExuK9ESpgajv7IaW7vpu9XolMMKg35Mj2u1UG9uLyKijKwAkrimtekp02r9RxP)
  * MOH-MOHA Village hierarchy: hierarchy linking the MOHA with the MOH village for the purpose of managing MOH-specific hierarchies and lists\
    ![](https://lh5.googleusercontent.com/FDOl2jLp3PSDFbP6S6DXpFI2EX6J\_K6oYNKjrcpSNZPVAIubGRZKhVpWpa1woU\_UbriRjL2aQEMmJwEsIOYGDcQ1C09zTbCLyffyPkdOT3\_SNCYSX34ai3DVZhfNzLPt5KyAsvEHIYSwtvruyX8YEM0DVL7RljOGTNtzk0EzSr9Mu5VR9dbJPaIG)
* MOH
  * Educational geography hierarchy: hierarchy that allows to link each school with the administrative division in which it is located\
    ![](https://lh4.googleusercontent.com/eNqXvK5Q1v1XKOmcnD2cW3Q9JAOYf8KxstTjpim\_azV7SF-a\_XyJrmeiwv8xfoTJ7gOG4UiuCk\_8YDjhaNJpbYx1CSf2TDsACNah91hIP9iFfwLlY5OeNfQeNOiMKjJoLI-6\_93Neln0fYqAmQ7DO5GQnySj0iLGbVWCtuVfyYQzTYP4BtyquzQb)
  * Educational path hierarchy: hierarchy that describes the journey through which students go through during their education\
    ![](https://lh4.googleusercontent.com/v7vCOkEgbMpdrnzfLIJOmrhQT89tZR-bmf9WDfklkKniIhMFxZguGEI5R4G2QR5GzIl3iSuWgPR\_TcDmumb3lAx1AfJdCvk9orBIBS72EiOR5CeJIumanfUOT3S\_5O6cCXlJH-tO9JzNovtA0iicy8eRrYT5uwi17ctXtN2maQEwlvu6OGhF\_GaY)

### 6.1.4 Access

The GeoPrism Registry Sandbox can be accessed from the following URL : https://demo-georegistry.geoprism.net

The sandbox is currently accessible through the following set of roles to external users.

![](<../../../../.gitbook/assets/Screenshot from 2022-09-28 15-56-36.png>)
