# Owners (Side bar) #

 
///TO DO: List owners, technical and product ones:


| **Stakeholder**  | **Role  **            | 
| -------------    |:-------------:        | 
|  Michael Cestone | Solution Lead         | 
|  Sheraz          | Business Analyst      | 
|                  | Dev Manager           | 

 
# What Is It? #

   Rave Web Services (RWS) integrates Medidata Rave with third-party systems to exchange CDISC ODM 1.3 standard clinical data or metadata synchronously and with immediate confirmation. More information on RWS features can be found here.
[About Rave Web Services](https://learn.mdsol.com/display/RWSprd/About+Rave+Web+Services)


# How to Use (User Documentation and Training) #

## Links to Existing User-Level Documentation ##


    ///TODO: Provide links with descriptions of what each link points to
 
## Links to Training Manuals ##
[Rave Web Services API](https://learn.mdsol.com/display/RWSprd/About+Rave+Web+Services)
[PDF User Guide](file:///C:/Users/drisack/Downloads/RWS_1.6_Combined_User_API_Guide_FINAL%20(1).pdf)

## Links to Training Videos ##

# How It Was Put Together (Architecture Overview) #
    
    RWS uses the Representational State Transfer (RESTful) architecture. Data is posted to or retrieved from Rave using HTTP protocol messages posted to specific URLs. Each message receives an immediate success or failure response. In the event of a failure, any pending changes are rolled back. As it uses “RESTful” web services RWS does not require the use of either Simple Object Access Protocol (SOAP) or Web Services Description Language (WSDL).


            
        ## Requirements ##
         //TODO: Link to any requirements here,
 
        ## Component(s) /Subsystems architecture high level ##
    //TODO: List the components that comprise the whole. E.g., for Architect, it would be Amendment Manager, Global Library, etc., if applicable. 
    

## Database ##

Provide an ERD diagram of the relevant tables


# Interaction with other products/subsystems #

     //TODO: What other products/systems/areas use data from this one. So developers can understand change impacts.
## Products/Areas that use RWS ##
Patient Cloud Mobile use of RWS
Rave/CTMS integration via RWS
Rave/CTMS - Designing CTMS Integration
KB information links
Install diagrams
Rave CTMS integration folder
Rave/Coder integration
https://mdsol-quality.veevavault.com/ui/#doc_info/58041/0/3
https://learn.mdsol.com/pages/viewpage.action?spaceKey=EngineerGuild&title=Rave-Coder+Integration&focusedCommentId=47581858
Diagnosing coder issues Part 1
More Rave/Coder integration

     //TODO: What data does this component/area/submodule rely on from other products/areas/systems

# Technical Detail Links #
    
     The links should have (Overview, Architecture detailed, High level classes, Diagnosing issues, Entry points, FAQs).
Rave Web Services Technical Training
ODM Schema Definitions
New RWS API Docs
RWS Tests
Knowledge Transfer
Introduction to RWS documentation
RWS and mAuth
RWS Authentication with iMedidata
Old statistics on RWS usage
RWS Authentication methods
RWS Limitations and wish list
RWS MAuthTools
RWS Cucumber regression vs regression lite
ODM Adapter - New Lab Analyte Ranges Dataset
ODM Adapter documentation
RWS Performance
More RWS Performance
 
      ODM Adapter consists of
Clinical Audit Records dataset (CDS)
Version Folders dataset (CDS)
Study Metadata (Native RWS)
Sites dataset (CDS)
Users dataset (CDS)
Signatures dataset (CDS)
Subjects List (Native RWS)
Lab Analysts (CDS)
Developer training video's
RWS Overview
RWS KT Session 1 (Using RWS)
RWS KT Session 2 (Tesing RWS)
RWS KT Session 3 (Bug Fix Walkthrough)
RWS ODM Adapter
 Rave Web Services Customer care
 Rave Coder Integration
 
# How to Diagnose (Diagnostic, Troubleshooting and Monitoring) #
    
      `//TODO: Provide a link to outside page(s) or to the child page`
    Link to child page containing:
    How to diagnose common issues that might happen during setup of Rave, and customer usage of the functionality.
 
# How to Debug (Debugging Entry Points) #

  //TODO: Specific project, File, Method useful entry points to diagnose issues.

Logs
Logs can be viewed on the Rave database itself using this query:
select * from WebServicesLogInbound

The IIS logs can also be selected via Sumologic.
Example all requests for JnJ url
_sourceCategory=IIS "RaveWebServices"  | split _sourceHost delim='_' extract 1 as RaveURL | toLowerCase(RaveURL) as RaveURL | where RaveURL="jnj"

Example all requests for clinical audit records:
_sourceCategory=IIS "RaveWebServices" and ClinicalAuditRecords.odm | split _sourceHost delim='_' extract 1 as RaveURL | toLowerCase(RaveURL) as RaveURL | where RaveURL="jnj"
 

# Future #
  
##Planned changes##

   [ODM v2 Performance Enhancements](https://docs.google.com/document/d/1vVj4jFlZ-kq-6BxGgow0WltgeF_noewq5I6MUqNeuqU/edit?ts=5644a485)
 
## Suggested improvements/ideas ##

   `//TODO: Any suggestions for improvements - link to pages/subpages as needed`
 
# FAQs #

  `//TODO: Any frequently asked questions and the answers that would be useful to developers, SQA`

 
#Revision History #
 
Version	Date	Description	Author

| **Version**   | **Date  **            |  **Author**     |
| ------------- |:-------------:        | :-------------: | 
|               |                       |                 |
|               |                       |                 |
|               |                       |                 |
