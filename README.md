# XForms
The first objective of the project was to develop 2 XForms for assisting on-field data collectors – surveyors – to collect data from respondents. The first of the 2 XForms is __Epidemiological pro forma__, which is concerned with data collection of patients suffering from various types of fever. The second of the 2 XForms is __Entomological pro forma__, which concerns data collection of an establishment with elementary questions about the physical well-being of a building.

The forms are available in 2 languages – English and Hindi.


## Application
The XForms developed in this project find their application extensively in _GIS_. The information collected is used for several operations in GIS. One such application of the XForms finds its way in a plugin developed previously in IIRS – *__QRealTime__*. The following is the flow chart depicting the use of an XForms at various stages.

![Flowchart depicting XForm life cycle in QGIS](https://github.com/yashdeep01/XForms/blob/master/Flowchart.png)

The XForm, once developed successfully, is uploaded on the aggregate server. It can be accessed through two platforms – mobile app and web server. The mobile app is available for Android on Play Store as *ODKCollect App*. ODK is the acronym for Open Data Kit. The web server through which the XForms can be accessed is *Enketo*. These accessed forms can be used to conduct surveys from a mobile phone with the ODKCollect app or any other device connected to the web server Enketo most conveniently. The data collected through these forms is, too, uploaded on aggregate server. This data can be obtained on QGIS through _QRealTime_ plugin by importing and syncing it.


## Epidemiological Pro Forma
This questionnaire mainly deals with collecting information about patients suffering from fever. The form is divided into 4 groups. The first group, *To be pre-filled*, contains the fields that are supposed to be filled by the surveyors before recording respondent’s responses. These fields include *NIMR Clinic Reference No., Zone, Ward No./Name*, and *GPS ID of Patient’s House*, which records the coordinates and the elevation of patient’s house. Second group, *Patient’s details*, has the fields asking the patient some general information about the patient that are not related to his/her health condition. These include *Patient’s Name, Age of the patient, Occupation, Work place* or *School location* depending on the occupation, *Floor residing*, and *Travel History* (No. of places visited in last 15 days). The third group, *Travel History*, occurs if the number filled in the previous field is greater than zero. It records the coordinates of places visited by the patient in last 15 days. The final group, *Fever*, first asks whether the patient is suffering from a fever. If not, the form is terminated. If yes, it gives four options – *Malaria, Dengue, Chikungunia*, and *Other*. If the user fills other, he/she is ask to fill which fever it is, if he/she is aware. The form terminates by displaying the *metadata* in the end – *Survey start time, Survey end time, Today* (date), and *deviceid*.


## Entomological Pro Forma
This form is categorised into 3 groups. The first group, *To be pre-filled*, consists of the fields *Team no., Zone, Ward No/Name*, and *Locality/Lane*. This group is followed by *Location*, which collects the *House no.* and *GPS ID*. The last group is the *Response Sheet*, which comprises of questions of the nature of an elementary inspection of the building, for example *checking over-head tank, solid waste*, etc. The form is terminated after filling an optional *Remarks* textbox. Again, at its termination, the user sees the *metadata*.
