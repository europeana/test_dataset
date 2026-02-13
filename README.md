# Test Dataset

This project brings together all source metadata and content that make up the Europeana test dataset.

The dataset is designed as a central repository of test records that represent concrete use cases supported by Europeana products and services.

The records included in the Europeana test dataset serve a dual purpose:
* they provide concrete examples for documentation, demonstrations, and the onboarding of data providers; and
* they function as test cases to support development, quality assurance, and the ongoing validation of Europeana’s tools and services.

# Inventory of test use cases 

## already covered use cases

## existing resource to be migrated

* Metadata and content tier examples: https://europeana.atlassian.net/wiki/spaces/EF/pages/2157510701/Example+records+-+content+metadata+tiers


## planned use cases to be covered

3D
* ~~A 3D object displayed using an existing embed service~~
* ~~A 3D object containing a 3D model alongside a embeddable view~~
* ~~A 3D object containing a 3D model with Paradata, alonside an embeddable view~~
* ~~A 3D object containing a 3D model and a 2D screenshot of the 3D object~~
* ~~A 3D object containing two 3D models encoded using different formats, alongside one only embeddable view.~~
* A 3D object containing two (alternative) embeddable views
* A 3D object containing a 3D model and two (alternative) embeddable views where the model only represents one of the views
* A 3D object containing two pairs of 3D model and embeddable view

# Guidelines for creating test records


## Defining scope for a test record

* Start from the use case. Carefully analyse the intended use case before defining the scope of a test. The use case determines which parts of the data must be included.
* Include only what is necessary. Ensure that all data elements required to support the use case are present, and deliberately exclude any unnecessary properties or structures.
* Adjust complexity to the test scope. The scope of a test record may range from very simple to highly complex, depending on what the test case aims to validate.
* Use minimal records for focused scenarios. For narrowly defined cases—such as a data provider supplying an existing manifest—a simple record is sufficient. This may include only mandatory properties alongside an edm:isShownBy and an associated svcs:Service.
* Use richer records for advanced use cases. More complex scenarios, such as representing a Metadata Tier 4 record, may require a significantly more elaborate data structure in order to fully satisfy the use case.

## Building a test record

* Use the provided template (see next section). Always start from the template below when creating a new test record to ensure consistency.
* Assign a clear identifier. Give each record an identifier starting with "TEST_". The identifier should reflect the use case and make it easy to group related test cases contextually.
* Provide an explicit title. Assign a title that clearly identifies the record as a test record. Start the title with "TEST RECORD: " and include the record identifier, following the established naming convention used in existing cases.
* Describe the scope meaningfully. Use dc:description to provide a clear and meaningful explanation of the test case or example. Avoid placeholder, fake, or random text.
* Indicate operational status. Use dcterms:conformsTo to specify the operational status of the test case.

## Template for a test record

```
<edm:ProvidedCHO rdf:about="TEST_{CATEGORY}">
  <dc:title xml:lang="en">TEST RECORD: {SHORT_TITLE}</dc:title>
  <dc:description xml:lang="en">This is an example record for XXX, covering the case where YYY.</dc:description>
  <dc:creator xml:lang="en">Europeana Data Services Team</dc:creator>
  <dcterms:isPartOf xml:lang="en">Example Dataset</dcterms:isPartOf>
  <dcterms:conformsTo xml:lang="en">{OPERATIONAL_STATUS}</dcterms:conformsTo>
</edm:ProvidedCHO>
```

Where:
* CATEGORY: A underscore dilimited set of keywords that identify the test case
* OPERATIONAL_STATUS: A keyword indicating whether it is fully supported or under development






