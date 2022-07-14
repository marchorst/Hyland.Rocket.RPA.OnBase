# Hyland RPA Onbase / Unity **Custom Activities**
This activities are build for showcases and customers who want to start as early as possible with Hyland RPA integration to OnBase.\
*Official "Core-Activities" will be available around April 2021.*
## Unity Scope
You have to use the following activities inside a Unity Scope Activity.\
When using Onbase connection multiple times in the process you should create a "Connection" variable/argument.\
You can reuse this the next time you use a Unity Scope within the "Existing Connection" field.

## Archiving new document/s
Archives Documents.

## Get Document keywords by DocId
Get Keywords from a Document.
Standard Keyword Record		|	AdditionalMultiInstanceKeywordRecord_[INDEX]\
<DataTable with Keywords>	|	<DataTable with Keywords>

## Update Document keywords by DocId
Updates a specific Keyword Value and / or creates it when it is not existing yet.

## Create WorkView Object
Creates an WorkViewObject from a specific class.

## Get WorkView Object by attributes
Get all WorkView Objects filtered by attributes.
The result is a *IDictionary<int64, WorkView.Object>* (ObjectId, WorkView Object).\
To loop through the results use a "Foreach Loop" with an *KeyValuePair<int64, WorkView.Object>*
You get the ObjectId by\
*Item.Key.ToString*\
The attributes you can get this way i.e. \
*Item.Value.AttributeValues.Find("InvoiceNumber").AlphanumericValue*


## SHOWCASE ONLY: Finish Workflow Onbase Document by DocId 
### Warning
Do not use this activity outside the showcase! If you need a fully functional activity please contact marc.horst@hyland.com or Michaela.Kroeber@hyland.com\
Actually it looks for the first Queue by DocId and executes the first AdHocUserTask.

# Download
The latest versions will be available in this Sharebase folder.\
https://app.sharebase.com/#/folder/1432651/share/3-2P0Trq5WNw0sb5srxEl--WYEJsOM