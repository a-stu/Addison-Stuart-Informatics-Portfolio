# Addison-Stuart-Informatics-Portfolio
This is a repo to showcase some of the normalization work I have done as an informaticist. It features my use of LLMs for query formulation and leveraging APIs for automapping logic.

These projects were carried out during the course of my Nursing Informatics practicum and concurrent employment at Project Ronin. They do not contain PHI or IP.

## Table of Contents

### Addison's Capstone Generative AI Query Development with Azure AI slides

(You'll have to download this PowerPoint, as it's too big for github to display)

This is a presentation I gave for the University of Utah Department of Bioinformatics. It demonstrates my process for Gen AI query formulation, and shows how I used it to retrieve a concept map's source FHIR URI from Ronin's clinical content database.

### Concept Map FHIR URI Workflow Map

This workflow map shows the problems that my project team was seeking to solve by populating a concept map's source FHIR URI in its publish screen.

### Concept Map Source FHIR URI Query Diagram

A diagram of the query used to retrieve a concept map's source FHIR URI. It's important to document out complex queries, because you need to be able to understand it thoroughly in order to describe it to an LLM so it can translate your request into code.

### FHIR URI in Concept Map Publish Screen

A screenshot of the display I built in Ronin's concept mapping tooling. It displays a concept map's source FHIR URI on the publish screen of a concept map so that an informaticist will have timely access to it during their next step, which is to publish the concept map to the FHIR model. The display includes a link to the Data Normalization Registry, which is a tooling interface which facilities registering clinical informatics content with the FHIR model in Simplifier.

### Terminology Creation FHIR URI Workflow Map

This workflow map demonstrates the pain points associated with the previous state of the terminology creation tool, namely that it required manual typing of the source FHIR URI.

### FHIR URI Builder

A screenshot of the interface I built in Retool which allows Informaticists to build a source FHIR URI from selectable components instead of typing it in by hand. This protects the FHIR model from erroneous entries, and copy+paste error proliferation.

Notably, the FHIR Resource field queries Simplifier's API and retrieves a list of unique FHIR Resources in Ronin's FHIR model.


### LOINC API Property & Units

A screenshot of a proof-of-concept OCI notebook in which I used LOINC FHIR APIs to retrieve the property and example units out of the very large JSON that the API returns when given a LOINC code. Property and example units were two of the most looked-up LOINC parts by Ronin informaticists to check the validity of LOINC codes called out in client source codes before mapping to them or not. Before Ronin closed down, my plan was to use this query to build API-assisted concept mapping CDS modules within the concept map tooling.

### Medication Automapping Logic

This is a screenshot of the logic I devised to automap client source medication codes to RxNorm. It leverages a combination of exact-match and probabilistic candidate vetting mappings via the RxNorm API, and algorithmic mapping for codes not mapped by the first two methods.

