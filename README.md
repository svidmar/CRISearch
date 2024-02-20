# CRISearch
Compare publications in local research information system with publications in OpenAlex.

![alt text](https://github.com/svidmar/CRISearch/blob/bc15c98cce496f75c4d574fc664bcb701887b139/img.png)


PowerBI Report which compares publications in an institutions research information management system - in this case Pure - with the institutions publications in OpenAlex. Can be used to find missing publications, enrich metadata, find Unpaywall URL’s and more.

To import missing publications, this might come in handy: [](https://github.com/svidmar/OpenAlex2RIS)

The report consists of three data tables and a function. 
M code available for inspiration. Change InstitutionID’s, API keys, e-mail etc. accordingly. 

# DOIs_in_Pure
Table which includes all the DOI’s you have in the institutions CRIS – in this case Pure. Get these from an API, from a CSV file export, from a database or likewise. 

# DOIs_in_OpenAlex
Queries the OpenAlex API for your institutions publications for in a defined year range. Generates a table which includes the DOI’s in OpenAlex with a relation to your institution.

# DOIs_not_in_Pure
Table which compares the institutions DOI’s in OpenAlex, with the DOI’s from your CRIS. The DOI’s found in both OpenAlex and your CRIS are filtered out, which leaves only the DOI’s not found in your CRIS, but found in OpenAlex.
 
# CheckTitleInPureAPI
This function is added to the “DOIs_not_in_Pure” table. It is used to check the Pure API for any potential matches on publication title. This is to account for cases, where the DOI is missing from the registration in Pure, has a wrong format, is entered in the wrong field etc.
