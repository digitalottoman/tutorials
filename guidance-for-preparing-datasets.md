---
title: Guidance for Preparing Mutually-Intelligible Datasets
author: Mark Polczynski
---

# Guidance for Preparing Mutually-Intelligible Datasets

One goal of the Digital Ottoman Platform is to serve as a common general repository for databases associated with the Ottoman world.  Further, it is desirable that databases contributed to the repository ultimately be mutually-intelligible, meaning that users could aggregate data from different databases using basic spreadsheet functions.  The purpose of this document is to outline guidelines that would aid in achieving mutual intelligibility of DOP gazetteer databases.

## Use unique identifiers to capture many-to-many relationships

In cases where many-to-many relationships among entities can occur (e.g. places, people), it is necessary to assign a unique identifier to each different entity.

A primary example is toponyms (place names), where a particular place can have multiple names at different times and rendered in multiple languages in multiple scripts, and may also have different locations at different times.  A similar situation holds for individual people (or groups of people), who can have multiple names at different times in their lives.

Per these examples, each particular place and person must have a unique identifier.  Note that in both of these examples, the name of a place and the name of a person does not constitute a unique identifier, since multiple places (and people!) can all have the same name.

**Guideline 1:** A database must have a field (column) to store unique IDs, and each record (row) in a database must contain an ID value.  
____________________________________________________________________________________________
## Include attributes to disambiguate many-to-many relationships.

Supporting many-to-many relationships means, for example, that a particular name may apply to multiple places, people, etc.  The result is that a search on a particular name can return information on multiple places, people, etc.  This requires disambiguation, which allows data in the database to be associated with the appropriate entity, which in turn requires that entities in the database have attributes that facilitate disambiguation.

Primary examples of this are the association of both a name and a location with a place, and a name and birth date with a person.

**Guideline 2:** For each entry (record, row) in a database, include at least two (and preferably more) attributes (field, column) that can aid in disambiguating database entities.
___________________________________________________________________________________________
## Create structured dictionary of attributes.

As implied in the previous guideline, each field/column in a database contains an attribute of the entity represented by a database entry/record/row, where the attribute names are the database column headers.

In terms of contributing a database to a common repository, it can be beneficial to create a dictionary of attributes which includes a brief definition of each attribute.  This not only assists in clarifying to the database contributor exactly what their database contains, but ultimately assists in aggregation of databases, since different databases may use different names for the same attribute (same type of data).

Further, it can beneficial to structure the dictionary of attributes according to attribute types.  Here is an example of Ottoman Turkish occupant tax designations:

```
Occupant tax designation – (definition)
  Ottoman – (definition)
    Household – (definition)
      Male/female Muslim – (definition)  →  Database column header
      Male/female Christian – (definition) →  Database column header
    Resident – (definition)
      Male unmarried Muslim – (definition) →  Database column header
      Male unmarried Christian – (definition) →  Database column header
      Female widow – (definition) →  Database column header
```

If an attribute has a numerical value, it can be beneficial to include the attribute’s measurement system in the definition.   For example, for male Armenian residents in the example above, the measurement system would be a count of individuals.  Other examples would be currency system for a monetary attribute, calendar system for a date attribute, weight system for a crop yield attribute.

**Guideline 3:**  For each field (column) in a database, create a definition for the associated attribute.  Convert the list of definitions into a structured dictionary of attributes.
_____________________________________________________________________________________________
## Cite data source.

When contributing databases to a common repository, it is beneficial to cite the source that the data came from.  This can apply at the database level, at the database entry level, and at the entry attribute level.  If all the data in a database comes from a single source, then a database source can be cited, but if different entries in a database have different sources, then the source for each entry should be cited, and if different attributes in a database have different sources, then the source of each attribute should be cited.

For example, a database of tax records may include place names and counts of, say, male Armenians derived from multiple tax records, and place locations from GeoNames.  In this case, the database can include separate fields/columns for place name sources, for counts of male Armenians sources, and for place location sources.

It is beneficial to cite a source using some standardized method.  For example, Beauplan’s A Description of Ukraine could be cited using the WorldCat catalog number: [http://www.worldcat.org/oclc/28080018.](http://www.worldcat.org/oclc/28080018)  It is also beneficial to cite the date of the source (vs. the date that the data applies, see Guideline 6).

**Guideline 4:**  Include data source information at the database level, and/or at the database entry level, and/or at the entry attribute level as dictated by the sources of the data.
____________________________________________________________________________________________
## Estimate data confidence.

All data by nature has some degree of certainty.  As with citation of data sources, confidence of a piece of data can be estimated at the database level, at the entry level, and at the attribute level.  An estimate of data confidence can be per a simple scale such as: certainly accurate; probably accurate; possibly accurate; inaccurate.

**Guideline 5:**  Include an estimate of data confidence at the database level, and/or at the database entry level, and/or at the entry attribute level as dictated by the sources of the data.
_____________________________________________________________________________________________
## Provide dates for data items.

Guideline 4 recommends including dates for data sources, but it is also beneficial to provide start and end dates for the data entered in the database.  For example, a source written in 1776, may state that a name for a place was used from the 1550’s through the 1600’s.  As with citation of data sources, dates for data can be estimated at the database level, at the entry level, and at the attribute level.

**Guideline 6:**  Include start and end dates for the applicability of data at the database level, and/or at the database entry level, and/or at the entry attribute level as dictated by the sources of the data.
_____________________________________________________________________________________________
_____________________________________________________________________________________________
## Example of Structured Dictionary of Attributes

The following provides an example of a prtion of a structured dictionary of attributes derived from a database constructed by [Grigor Boykov](https://github.com/griboykov).  ( ) indicates fields not currently contained in Grigor’s database.  → indicates links to detailed elements of the dictionary.

```
Place						
  ID
  Name →
  Location →
  Land owner →
  Administrative structure →
  Occupants →

Name
  Language

Location
  Latitude/longitude

Land owner
  Name →

Administrative structure
  Modern
    Country
  Ottoman
    Sanjak
      Name →
    Kaza
      Name →
  Nahia
      Name →

Occupants
  Religion →
  Occupant tax designation →

Religion
  Male/female Muslim
  Male/female Christian
  Male/female Muslim converts

Occupant tax designation
  Ottoman
    Household
      Male/female Muslim
      Male/female Christian
    Resident
      Male unmarried Muslim
      Male unmarried Christian
      Female widow
      Male Jew
      MaleArmenian
      Male Gypsy
      Male Yuruk – Semi-nomad 
```
