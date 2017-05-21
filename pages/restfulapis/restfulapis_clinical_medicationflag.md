---
title: Clinical | Medication Flag
keywords: usecase, medication, flag
tags: [fhir, rest, clinical, medication, workflow]
sidebar: foundations_sidebar
permalink: restfulapis_clinical_medicationflag.html
summary: Workflow Medication Flag
---

## Mediciation Flag ##

{% include profile.html content="[Care Connect Medication Flag](http://www.interopen.org/candidate-profiles/care-connect/CareConnect-Medication-Flag-1.html)" %}

{% include note.html content="The API for Medication Flag is the same as Flag" %}

## Read ##

Return a single `Flag` for the specified id

```http
GET /Flag/[id]
```


## Search Parameters ##

Search for all flag resources for a patient. Fetches a bundle of all `Flag` resources for the specified patient.

```http
GET /Flag?[searchparameters]
```

{% include moscow.html content="[Flag](https://www.hl7.org/fhir/DSTU2/flag.html#search)" %}


| Name | Type | Description | SHALL |
|------|------|-------------|-------|
| `patient` | `reference` | The patient for the vaccination record | Y |
| `status` | `token` | Flag status: active, inactive or entered-in-error | Y |
| `date` | `date` | Time period when flag is active |  |

{% include search.patient.html content="Flag" %}

{% include search.status.html content="Flag" options="active | inactive | entered-in-error" selected="active" %}