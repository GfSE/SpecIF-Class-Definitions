![SpecIF logo](https://github.com/GfSE/SpecIF/blob/master/logo/SpecIF_Logo_small.png?raw=true)

# SpecIF class and data type definitions

This repository is part of the SpecIF initiative (https://specif.de).
It is included as submodule in the main SpecIF repository located at https://github.com/GfSE/SpecIF.

If you want to support the SpecIF standardization process, join us and take a look at https://specif.de.

It contains the vocabulary and the data type and class definitions for the SpecIF metatypes:
* Primitive data types
* Enumeration data types
* Property classes
* Resource classes
* Statement classes

The vocabulary and the class definitions form the semantic definitions of SpecIF.

<b>It is currently still under development. Have a look at the table below for release status.</b>

## Domains

The definition of the SpecIF classes is organized in application domains. 
This allows the definition of releases for some domains at the same time where 
other domains are still under discussion and under development.

### Domain types
The following list shows the currently identified domains and their IDs:

|Domain ID|Domain|Description|Release status|
|---------|-|-|-|
|01|Base definitions|Common definitions relevant for all domains (e.g. primitive data types)|Released in 1.1|
|02|Requirements Engineering|Classical requirements engineering following the IREB definitions|Released in 1.1|
|03|Model Integration|SpecIF mapping for model integration based on the Fundamental Modeling Concepts approach|Released in 1.1|
|04|Automotive Requirements Engineering|Automotive-specific requirements engineering extensions (VDA)|Unreleased|
|05|Agile Requirements Engineering|Requirements engineering for agile development (e.g. epics and user stories)|Unreleased|
|06|UML-SpecIF mapping|Extensions to map UML (Unified Modeling Lanaguage) models to SpecIF|Deprecated. Use Model Integration types.|
|07|Issue Management|Issue and Task management|Unreleased|
|08|BOM|Bill of materials|Unreleased|
|09|Variant Management|Feature model-based variant management|Unreleased|
|10|Vocabulary Definition|Resources to define Vocabularies (e.g. SpecIF Vocabulary)|Unreleased|
|11|Testing|System and software testing domain (using definitions from ISQB and UML2 testing profile)|Unreleased|
|12|SpecIF-Events|SpecIF data events (CRUD) for event-based notifications about SpecIF data changes.|Unreleased|

## File naming schema
For the discussion process the metadata files have a special naming schema with a 3 digit number as prefix in the filename:

* The **first digit** stands for the meta type kind, that is defined by the file
* The **next two digits** are the domain IDs, listed above

This makes it possible to define a metatype by a set of files with the same first digit describing the class definition kind and the next digits referencing the domain.

<i>Example:</i> The files starting with `101_` is the definition of primitive data types for the domain 01-Base definitions. 
The superset of all files starting with the same digit are building the complete specification for one metatype.

## Current file naming schema
Currently the following digits are assigned with the SpecIF metatypes. It is possible that this will change in the future, e.g when further metatypes are defined.

|1st Digit|SpecIF Metatype|
| ----|---------------|
|   1 | Primitive data types     |
|   2 | Enumeration data types |
|   3 | Property classes |
|   4 | Resource classes |
|   5 | Statement classes |

## The folder `_Packages`

The folder packages contains merges of class definitions to one single SpecIF file. 
In the class definitions the data types and class definitions are separated into single files. 
To have all relevant data together in one SpecIF file, the _Packages folder contains SpecIF files, that are generated from the class definition files.

## The folder `vocabulary`

The folder vocabulary contains the SpecIF vocabulary defining a set of terms used for SpecIF.

<b>The vocabulary is currently only available in SpecIF 1.0 JSON-format. We work to provide it as soon as possible using the SpecIF schema format 1.1.</b> 

## What about the file `Empty.specif` ?

This file can be used as base for further metatype definitions. If you want to add a new definition file, please ensure to change the SpecIF file ID, title and check the SpecIF version.
