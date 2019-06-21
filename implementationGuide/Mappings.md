﻿

# Mappings
This section descripes how the profiles defined in this guide relate to several other data models, mainly from other biobank-related projects. Items in *italic* imply slice names.

## BBMRI-ERIC  Directory
The BBMRI-ERIC Directory can be found [here](https://directory.bbmri-eric.eu).

### Biobank
The BBMRI-ERIC Directory *Biobank* entity corresponds to the *Biobank* profile from this guide.

| BBMRI-ERIC | Biobank Profile |
|--|--|
|id | identifier:*Bbmri-EricId*.value |
|name | name |
|acronym | alias |
|description | extension.description.value |
|url | telecom:*url*.value|
|juridical_person | extension.juridicalPerson.value |
|country | address.country |
|head_title_before_name | contact:*head*.name.prefix |
|head_firstname | contact:*head*.name.given |
|head_lastname | contact:*head*.name.family |
|head_title_after_name | contact:*head*.name.suffix |
|contact | *see section contact* |
|network | *see section network* |

### Contact Information
In FHIR, the contact information is included in the [*Organization* resource][1], which is profiled as *Biobank* in this guide.

| BBMRI-ERIC| Biobank.contact |
|--|--|
| title_before_name |  prefix |
|first_name | given |
|last_name | family |
|title_after_name | suffix |
| phone | contact:*contact*.telecom:*phone*.value |
|email | contact:*contact*.telecom:*email*.value |
|address | contact:*contact*.address.line |
|zip | contact:*contact*.address.postalCode |
|city | contact:*contact*.address.city |
|country | contact:*contact*.address.country |



### Collection


### Network
This project does not contain a specific profile for biobank networks. While such networks could be represented as [*Organization* resources][1], it is outside the scope for this project.
 To record a biobank's membership in a network, we use a profiled *OrganizationAffiliation*: *NetworkMembership*. There, the refernce to the network happens via its BBMRI Directory id since we do not have an actual FHIR resource. (For further information see section on *NetworkMembership*.)


## MIABIS

TODO

[1]:https://www.hl7.org/fhir/organization.html