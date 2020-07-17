# Threat Intelligence feed from Logical IT

Threat Intelligence feed about COVID-19

----------------------------------

Use Information:

* Colums: 
  * IOC_dna|CVE_dna: A SHA1 hash about all extract columns
  * IOC|CVE: The IOC or CVE-ID itself.
  * hit: Colum for search on graylog.
  * IOC_Category: A IOC Category type as (Artifacts dropped / Payload delivery / Network activity / etc).
  * IOC_Comment|CVE_Comment: A String comment about this IOC | CVE-ID
  * IOC_Source|CVE_Source: A Threat Feed or Campaign about this IOC.
  * CVE_Date: Date where this IOC or CVE-ID were detected. 

* Lists by Product:
  * \*graylog*: IOCs exported compatible with Graylog lookup searching
    * Fields Enclosed by: |
    * Fields Separation by: ;
  * \*splunk*: IOCs exported compatible with Splunk lookup searching (can use it as MISP Feed also)
    * Fields Enclosed by: "
    * Fields Separation by: ,
    
* Lists by Type:
  * \*vulnerabilities*: CVE-IDs exploited detected on campaigns
    * Headers Graylog: |CVE|;|hit|
    * Headers Splunk: "CVE_dna","CVE","hit","CVE_Category","CVE_Comment","CVE_Source","CVE_Date"
  * \*hostname|ip-src|ip-dst|md5|sha1|sha256|imphash*: IOCs detected on campaigns
    * Headers Graylog: |IOC|;|hit|
    * Headers Splunk: "IOC_dna","IOC","hit","IOC_Type","IOC_Category","IOC_Comment","IOC_Source"
  * \*json-misp*: Full Contexted MISP Json Format (Events and Attributes)
    
* Lists by IOC Trustworthiness:
  * \*graylist*: Suspicious IOC. 
    * Recommended Action: Detection Only
  * \*blacklist*: Confirmed IOC.
    * Recommended Action: Prevention
    
* Lists by Additional Filters:
  * \*-br: Brazilian registered IOCs (domains / IP CIDR)
