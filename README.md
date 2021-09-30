# HL7 norway ig template for IG Publisher

This is a basic fhir implementation guide template based on the
[fhir.base.template](https://github.com/HL7/ig-template-base) for the [IG Publisher](https://wiki.hl7.org/IG_Publisher_Documentation) and forked from the HL7 Switzerland modification of the base template.

## Features

* Custom logos (see below)
* Propose a change with is routed through Google Forms to github

## Using the ig template

You can use the template by referencing it from the HL7 Norway Github.
Edit the template element of you ig.ini file to point to the GitHub source:
```
template = https://github.com/HL7Norway/ig-template
```

* Provide [packages-list.json](https://wiki.hl7.org/index.php?title=FHIR_IG_PackageList_doco) in input/pagecontent directory

## Note on HL7/FHIR Logos

This template does include the use the hl7/fhir logo by uncommenting the html-code in the logo.html and fhirlogo.hml in input/includes directory. Logos can be accessed from input/pagecontent/assets/images/ or online on Github. The template is designed for IG's controlled by HL7 Norway. 
> Please check rules for FHIR/HL7 logo use on [zulip](https://chat.fhir.org/#narrow/stream/179294-committers.2Fannounce/topic/HL7.20Trademark.20Issues) before publishing an implementation guide containing official HL7/FHIR or affiliate logo.

## Add a feedback form for your ig

In your ig add (or create) to input/data/features.yml the following properties

```yaml
---
feedback:
    active: true
    formUrl: provide link (see below)
```

1. For the form request a copy of the feedback form https://docs.google.com/forms/d/1sdG-LgSlNaSDJ1HHABEVgmk0etXT-qZd-4bh2iBzUps/edit
2. Don't change the different entries, otherwise they will not be prefilled
3. In the kebab menu select Script Editor
4. Adjust handle to github repo organization where ig lives in
5. Adjust repo to github repo name of ig
6. In Script Editor to the left select Trigger (clock icon)
7. Add Trigger for Submit Feedback, select Event Type On Form Submit (you need to confirm this with your google account)
8. Back in the form, copy the link form Send form - link and put it in above field
