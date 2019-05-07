# ![LOGO](logo.png) BC Geographical Names Web Service - **flow**ground Connector

## Description

A generated **flow**ground connector for the BC Geographical Names Web Service - API (version 3.x.x).

Generated from: https://api.apis.guru/v2/specs/gov.bc.ca/bcgnws/3.x.x/openapi.json<br/>
Generated at: 2019-05-07T17:42:11+03:00

## API Description

This REST API provides searchable access to information about geographical names in the province of British Columbia, including name status and details about the corresponding geographic feature. 

Please note that you may experience issues when submitting requests to the delivery or test environment if using this [OpenAPI specification](https://github.com/bcgov/api-specs) in other API console viewers.

## Authorization

This API does not require authorization.

## Actions

### Get all feature categories

> Gets a list of all feature categories used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class.

*Tags:* `feature taxonomy`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml.

### Get all feature classes

> Gets a list of all feature classes used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class.

*Tags:* `feature taxonomy`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml.

### Get all feature types

> Gets a list of all feature types used by the BC Geographical Names Information System (BCGNIS).  Note: there are three levels of classification in the BCGNIS feature taxonomy: classes, categories and types.  A type is a subset of a category, and a category is a subset of a class.

*Tags:* `feature taxonomy`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml.

### Get a feature by its featureId

> Get information about the geographical feature with the specified featureId.

*Tags:* `feature`

#### Input Parameters
* `featureId` - _required_ - The unique identifier for a feature

### Get all name authorities

> Gets a list of all name authorities responsible for naming decisions of the geographical names in the BC Geographical Names Information System (BCGNIS)

*Tags:* `name authority`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml.

### Search for names with metadata changes in a given period

> Search for information about geographical names which have changed most recently within a specified time window.  Changes may include status cupdates and metadata corrections.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `fromDate` - _required_ - Defines the earliest date (YYYY-MM-DD format) of the change time window for the search
* `toDate` - _required_ - Defines the latest date (YYYY-MM-DD format) of the change time window for the search
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Search for names affected by recent naming decision

> Search for information about geographical names affected by naming 'decisions' made by the BC Geographical Names Office (naming authority) within the last X days.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `days` - _required_ - The number of days used to define the time window of naming decisions to search.  The number is interpreted as searching for 'names affected by decisions within the last X days'.
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Search for names affected by naming decisions in a given year

> Search for information about geographical names affected by naming 'decisions' made by the BC Geographical Names Office (naming authority) in a given year.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `year` - _required_ - The year in which to search for names affected by naming decisions'.
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Search in a geographic area

> Search for information about geographical names that correspond to features within a geographic bounding box.  Various options and filter parameters are available to refine the search.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `bbox` - _required_ - A geographic bounding box defining the search area.  Must be specified as a string of the form 'minLongitude,minLatitude,maxLongitude,maxLatitude' (WGS84). e.g. -119,49,-118,50
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Search near to a geographic point

> Search for information about geographical names that correspond to features within a geographic area defined by a centre point and a radius.  Various options and filter parameters are available to refine the search.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `featurePoint` - _required_ - A geographic coordinate specifying the centre point of the search area.  Must be specified as a string of the form 'longitude,latitude' (WGS84).  e.g. -120,51
* `distance` - _required_ - A radius (in kilometres) around the centre point.
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Search by name, limit to unofficial names only

> Search for information about unofficial geographical names by the text of the name itself.  Various options and filter parameters are available to refine the search.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `name` - _required_ - A filter to search based on the the text of the name itself.  Use the asterisk (*) as a wildcard character.  For example 'vancouv*'
* `exactSpelling` - _optional_ - If the 'name' parameter is specified, 'exactSpelling' specifies whether to include only names that exactly match the search text (exactSpelling=1), or whether to also include names with similar spellings (exactSpelling=0)
    Possible values: 0, 1.
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: relevance, name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Search by name, limit to official names only

> Search for information about official geographical names by the text of the name itself.  Various options and filter parameters are available to refine the search.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `name` - _required_ - A filter to search based on the the text of the name itself.  Use the asterisk (*) as a wildcard character.  For example 'vancouv*'
* `exactSpelling` - _optional_ - If the 'name' parameter is specified, 'exactSpelling' specifies whether to include only names that exactly match the search text (exactSpelling=1), or whether to also include names with similar spellings (exactSpelling=0)
    Possible values: 0, 1.
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: relevance, name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Search by name

> Search for information about geographical names by the text of the name itself.  The response will include both official and unofficial names.  Various options and filter parameters are available to refine the search.

*Tags:* `search` `name`

#### Input Parameters
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv.
* `name` - _required_ - A filter to search based on the the text of the name itself.  Use the asterisk (*) as a wildcard character.  For example 'vancouv*'
* `exactSpelling` - _optional_ - If the 'name' parameter is specified, 'exactSpelling' specifies whether to include only names that exactly match the search text (exactSpelling=1), or whether to also include names with similar spellings (exactSpelling=0)
    Possible values: 0, 1.
* `featureClass` - _optional_ - A filter to limit the search to names associated with features of a certain 'class'  The value of this parameter should be a 'featureClassCode' value returned by the /featureClasses resource, or an asterisk (*) to request that all feature classes be included.
* `featureCategory` - _optional_ - A filter to limit the search to names associated with features of a certain 'category'  The value of this parameter should be a 'featureCategoryCode' value returned by the /featureCategories resource, or an asterisk (*) to request that all feature categories be included.
* `featureType` - _optional_ - A filter to limit the search to names associated with features of a certain 'type'  The value of this parameter should be a 'featureTypeCode' value returned by the /featureTypes resource, or an asterisk (*) to request that all feature types be included
* `sortBy` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
    Possible values: relevance, name, featureType, decisionDate.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries.
    Possible values: 4326, 4269, 3005, 3857, 26907, 26908, 26909, 26910, 26911.
* `embed` - _optional_ - A flag to indicate whether to embed the corresponding 'feature' into each matching name
    Possible values: 0, 1.
* `outputStyle` - _optional_ - A flag indicating whether to include with each matching name a succinct list of attributes (summary), or a comprehensive list of attributes (detail)
    Possible values: summary, detail.
* `itemsPerPage` - _optional_ - The number of search results to return (1-200)
* `startIndex` - _optional_ - The index of the first record to be returned (>= 1)

### Get a name by its nameId

> Get information about the geographical name with the specified nameId.

*Tags:* `name`

#### Input Parameters
* `nameId` - _required_ - The unique identifier for a name
* `outputFormat` - _required_ - The format of the output.
    Possible values: json, xml, kml, csv, html.

## License

**flow**ground :- Telekom iPaaS / gov-bc-ca-bcgnws-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
