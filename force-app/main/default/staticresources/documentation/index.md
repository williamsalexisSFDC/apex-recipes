# Reference Guide

## Async Apex Recipes

### [AtFutureRecipes](async-apex-recipes/AtFutureRecipes.md)

Demonstrates the `@future` syntax and usage

### [BatchApexRecipes](async-apex-recipes/BatchApexRecipes.md)

Demonstrates the use of the Database.Batchable interface. The 
methods in this class are called by the system as the batch executes. 
To execute this batch use `Database.executeBatch(new BatchApexRecipes());` 
 
More on the Batchable interface: 
https://sfdc.co/batch_interface

### [QueueableChainingRecipes](async-apex-recipes/QueueableChainingRecipes.md)

Demonstrates how to use the Queueable interface 
to chain multiple queueable instances together. The methods in this class, 
with the exception of the constructor, are run automatically by the system 
as the job runs. To enqueue this job, use: 
 `System.enqueueJob(new QueueableChainingRecipes());` 
 
More on the Queuable interface: 
https://sfdc.co/queueable-apex

### [QueueableRecipes](async-apex-recipes/QueueableRecipes.md)

This class demonstrates how to construct a Queueable class. 
The methods in this class are run automatically by the system 
as the job runs. To enqueue this job, use: `System.enqueueJob(new QueueableRecipes());` 
 
More on the Queable interface: 
https://sfdc.co/queueable-apex

### [QueueableWithCalloutRecipes](async-apex-recipes/QueueableWithCalloutRecipes.md)

Demmonstrates the use of the Queueable interface to make 
callouts. The methods in this class are called by the system at run time. 
To enqueue this job and see it&#x27;s results, use `System.enqueueJob(new QueueableWithCalloutRecipes());` 
 
More on the Queable interface: 
https://sfdc.co/queueable-apex

### [ScheduledApexDemo](async-apex-recipes/ScheduledApexDemo.md)

A demo class to be scheduled by ScheduledApexRecipes

### [ScheduledApexRecipes](async-apex-recipes/ScheduledApexRecipes.md)

Demonstrates how to implement the Schedulable interface. The 
methods in this class are designed to be scheduled, similar to a cron job. 
 
More on the Schedulable interface: 
https://sfdc.co/scheduled-apex

## Collection Recipes

### [CollectionUtils](collection-recipes/CollectionUtils.md)

Library of generic, type safe collection methods.

### [IterationRecipes](collection-recipes/IterationRecipes.md)

Demonstrates how to iterate on lists and sets

### [ListSortingRecipes](collection-recipes/ListSortingRecipes.md)

Demonstrates how to sort lists using the Comparator Interface

## Custom Metadata Recipes

### [CustomMetadataUtilties](custom-metadata-recipes/CustomMetadataUtilties.md)

This class utilizes Custom Metadata objects and the example 
use case we&#x27;ve established for Apex Recipes.

## Custom Objects

### [Account](custom-objects/Account.md)

### [Bucketed_Picklist_Value__mdt](custom-objects/Bucketed_Picklist_Value__mdt.md)

### [Bucketed_Picklist__mdt](custom-objects/Bucketed_Picklist__mdt.md)

### [Contact](custom-objects/Contact.md)

### [Disabled_For__mdt](custom-objects/Disabled_For__mdt.md)

### [Event_Recipes_Demo__e](custom-objects/Event_Recipes_Demo__e.md)

### [Junction_Demo_1__c](custom-objects/Junction_Demo_1__c.md)

### [Junction_Demo_2__c](custom-objects/Junction_Demo_2__c.md)

### [Junction__c](custom-objects/Junction__c.md)

### [LogEvent__c](custom-objects/LogEvent__c.md)

### [Log__e](custom-objects/Log__e.md)

### [Metadata_Driven_Trigger__mdt](custom-objects/Metadata_Driven_Trigger__mdt.md)

### [Permission_Set_Group_Testing_Result__mdt](custom-objects/Permission_Set_Group_Testing_Result__mdt.md)

### [Picklist_Bucket__mdt](custom-objects/Picklist_Bucket__mdt.md)

## Data Recipes

### [DMLRecipes](data-recipes/DMLRecipes.md)

Demonstrates various ways of making Data Manipulation Language 
(DML) calls. Note that this class demonstrates both Database methods as 
well as DML Keywords.

### [DynamicSOQLRecipes](data-recipes/DynamicSOQLRecipes.md)

Demonstrates how to construct a SOQL query dynamically, and 
safely 
 
More on dynamic SOQL and SOQL injection: 
https://sfdc.co/soql-injection

### [MetadataCatalogRecipes](data-recipes/MetadataCatalogRecipes.md)

Demonstrates how to query the Metadata Catalog. This is 
sometimes faster that Schema Describe calls especially for large complex orgs

### [SOQLRecipes](data-recipes/SOQLRecipes.md)

Demonstrates how to make various types of SOQL calls 
including multi-object queries, and aggregate queries

### [SOSLRecipes](data-recipes/SOSLRecipes.md)

Demonstrates how to use SOSL. 
SOSL is used for full text, and fuzzier text searching. 
 
More on the difference between SOQL and SOSL: 
https://sfdc.co/soql-sosl

## DataWeaveInApex Recipes

### [BasicDataWeaveInApexRecipes](dataweaveinapex-recipes/BasicDataWeaveInApexRecipes.md)

Demonstrates various ways of invoking a DataWeave scripts 
in Apex. Note that this class demonstrates both static and dynamic way of 
invoking DataWeave scripts.

### [CsvToJsonConversionRecipes](dataweaveinapex-recipes/CsvToJsonConversionRecipes.md)

Demonstrates how to use DataWeave 
in Apex to convert CSV to JSON.

### [DataWeaveErrorRecipes](dataweaveinapex-recipes/DataWeaveErrorRecipes.md)

Demonstrates how to handle DataWeave script errors in Apex.

### [FormattingRecipes](dataweaveinapex-recipes/FormattingRecipes.md)

Demonstrates various ways to apply formatting using DataWeave scripts in Apex.

### [LoggingRecipes](dataweaveinapex-recipes/LoggingRecipes.md)

Demonstrates how to use the logger in DataWeave scripts in Apex.

### [MultipleInputRecipes](dataweaveinapex-recipes/MultipleInputRecipes.md)

Demonstrates how use multiple input parameters in a DataWeave script in Apex.

### [ObjectConversionRecipes](dataweaveinapex-recipes/ObjectConversionRecipes.md)

Demonstrates how to convert data in CSV or JSON format 
into Salesforce sObjects and Apex objects using DataWeave scripts in Apex. 
Notice that all script output MIME types are set to `application/apex` .

## Email Recipes

### [InboundEmailHandlerRecipes](email-recipes/InboundEmailHandlerRecipes.md)

Demonstrates how to use the inboundEmailHandler 
interface to create custom logic and automation on the reception 
of an email. This class demonstrates saving the email 
to an EmailMessage Object along with Attachments. 
 
NOTE: This class *does not* specify a sharing model. 
This is on purpose - When this class is executed, by the inbound 
email system, it will execute in a system context and pieces of 
this class need to be able to *read* all contacts - which is a 
common use case. Because of this, we&#x27;re suppressing the PMD 
ApexSharingViolation warning.

## Encryption Recipes

### [EncryptionRecipes](encryption-recipes/EncryptionRecipes.md)

Demonstrates how to use different encryption and signing algorithms in Apex

## Files Recipes

### [FilesRecipes](files-recipes/FilesRecipes.md)

Demonstrates how to create, link and share Files

## Integration Recipes

### [ApiServiceRecipes](integration-recipes/ApiServiceRecipes.md)

This recipe extends the custom RestClient class and 
represents a specific REST API service we need to interact with - in 
this case the Google Books API. This class is responsible 
for serializing and deserializing the Data Transfer Objects (Model Objects) 
necessary for input and output from this org to the third party system and 
back. 
 
More on the Google Books API here: https://developers.google.com/books/docs/v1/reference/volumes

### [ApiServiceRecipesDataModel](integration-recipes/ApiServiceRecipesDataModel.md)

This class contains the &#x27;data transfer object&#x27; details. 
Data transfer objects are used to serialize Apex objects to JSON and 
web service response JSON to Apex objects.

### [AuraEnabledRecipes](integration-recipes/AuraEnabledRecipes.md)

Demonstrates how to expose a class method to Aura and LWC 
components. Also demonstrates how to return an AuraHandledException.

### [CalloutRecipes](integration-recipes/CalloutRecipes.md)

Demonstrates how to make an opinionated REST callout. 
This class utilizes the custom RestClient from the Shared Code group.

### [CustomRestEndpointRecipes](integration-recipes/CustomRestEndpointRecipes.md)

An Apex class can be used to generate a custom REST endpoint 
that can be exposed to the Salesforce API. In order to achieve this, we can 
annotate the class with `@RestResource` and then provide a URL mapping. In 
this example we are using `/integration-service/*` to expose the class. It can 
then be accessed at by performing a callout to 
 `<INSTANCEURL>/services/apexrest/integration-service` . Once the class has been 
designated as a REST resource, we can then annoate our apex methods with 
 `@HttpGet` , `@HttpDelete` , `@HttpPut` , `@HttpPost` , and `@HttpPatch` to enable access 
via it&#x27;s relative Http Method. 
 
Note: The examples in this class are not Apex code, but rather cURL commands. 
cURL is a command line utiltiy for Windows, Mac and Linux that allows you to 
interact with Rest Resources and URLs to exchange data. Please excute these 
examples in your terminal application of choice.  You might also consider a 
third party UI based tool like Postman to ease things like authentication. 
 
Note: There is a `@suppressWarnings` annotation on this class for Cyclomatic 
Complexity. You can read more about what Cyclomatic Complexity is here: 
https://en.wikipedia.org/wiki/Cyclomatic_complexity Classes with a high 
Cyclomatic Compelexity score are harder to test, and more prone to bugs 
because of the sheer number of branching logic paths available. This class 
is made up of a number of small methods, each of whom does CRUD/FLS Checks 
and therefor every method includes at least one branching path - but not 
much else. Other classes in this repository do not have such a high 
Cyclomatic Complexity because the ratio of logic to if/else statments is much 
lower. 
 
See CalloutRecipes for examples on how to call the custom REST endpoint.

### [NamedCredentialRecipes](integration-recipes/NamedCredentialRecipes.md)

Demonstrates how to manage named credentials from Apex

## Invocable Recipes

### [InvocableMethodRecipes](invocable-recipes/InvocableMethodRecipes.md)

Demonstrates how to create Apex classes and methods that 
can be invoked from Visual Flows and Process Builder Processes 
This also demonstrates custom input and output inner classes allowing 
you to create code that accepts input from a flow/process and 
returns data to the flow

## LDV Recipes

### [LDVRecipes](ldv-recipes/LDVRecipes.md)

A demonstration recipe for how to process a large amount of 
records in serial chunks using Queueables. The idea behind this recipe 
is that Queueables, in production, have no max-queue depth. Meaning that so 
long as you only enqueue one new queueable, it can keep cycling through until 
the entire data set is processed. This is useful for instance, when you want 
to process hundreds of thousands of records. 
 
Note: You&#x27;re not able to re-enqueue within a test context, so the unit test 
for this code is limited to the same number of records as chunkSize below. 
 
Note: This should be refactored to be an abstract class that you can extend 
named &#x27;Ouroboros&#x27;. (Ouroboros &#x3D; the snake eating it&#x27;s own tail)

## Miscellaneous

### [AccountNumberOfEmployeesComparator](miscellaneous/AccountNumberOfEmployeesComparator.md)

An example implementation of the Comparator Interface 
In this example we show how to sort all the accounts by their employee numbers in ascending order

### [AccountShippingCountryComparator](miscellaneous/AccountShippingCountryComparator.md)

An example implementation of the Comparator Interface 
In this example we show how to sort all the accounts by their country names in alphabetical order

### [IterableApiClient](miscellaneous/IterableApiClient.md)

Demonstrates an interable REST API client that loads paginated records (strings) thanks to an iterator

### [CsvData](miscellaneous/CsvData.md)

### [PlatformCacheBuilderRecipes](miscellaneous/PlatformCacheBuilderRecipes.md)

demonstrates how to use the Cache.CacheBuilder Interface

### [Safely](miscellaneous/Safely.md)

Class wraps DML Calls in FLS / Crud checks. Library is baseed on 
a fluent api system. All calls are constructed, then chained with options. 
For instances. `new Safely().allOrNothing().doInsert(List<sObject>);` 
 
Notable chainable methods include: 
- allOrNothing() - this enforces the AllOrNothing DML flag. All DML is 
eventually executed via Database.* methods which accept an allOrNothing 
parameter requiring all of the records to succeed or fail. 
- throwIfRemovedFields() - this method, if called, will result in an 
exception being thrown if any record being modified has fields removed 
by the security decision.

### [StubExample](miscellaneous/StubExample.md)

### [StubExampleConsumer](miscellaneous/StubExampleConsumer.md)

### [TestDouble](miscellaneous/TestDouble.md)

Implements an easy and re-usable StubProvider 
Utilizes a fluent interface for ease of use. 
This is merely an example of how you could build a reusable stub provider 
class. There are definitely edge cases or features not handled by this class. 
 
The general mechanism for use looks like this: 
```apex
 TestDouble stub = new TestDouble(SomeClass.class);
 TestDouble.Method methodToTrack = new TestDouble.Method('methodName')
     .returning(someObject);

 stub.track(methodToTrack);

 ConsumingClass consumer = new ConsumingClass(
    (someClass) stub.generate()
 );
```

### [MDTAccountTriggerHandler](miscellaneous/MDTAccountTriggerHandler.md)

This is a simple trigger handler class for Account that is used 
to demonstrate the custom metadata trigger handler approach to multiple 
trigger handler classes ordered by and controlled by custom metadata.

### [MDTSecondAccountTriggerHandler](miscellaneous/MDTSecondAccountTriggerHandler.md)

This is a simple trigger handler class for Account that is used 
to demonstrate the custom metadata trigger handler approach to multiple 
trigger handler classes ordered by and controlled by custom metadata.

### [MetadataTriggerService](miscellaneous/MetadataTriggerService.md)

### [SampleHandler](miscellaneous/SampleHandler.md)

This class is a sample trigger handler for use while testing 
the metadataTriggerHandler. Because custom metadata cannot be inserted, and 
because the MetadataTriggerHandler instantiates handler classes from custom 
metadata records, even when we stub/mock the metadata record retrieval we 
still need an actuall class that it can instantiate. 
 
Note, this class is annotated with `@isTest` to prevent it&#x27;s use outside of 
tests, not because it contains tests.

## Platform Cache Recipes

### [PlatformCacheRecipes](platform-cache-recipes/PlatformCacheRecipes.md)

Illustrates how to programatically use the Platform Cache 
feature of Salesforce. Many of these recipes are, taken together, not very 
DRY (don&#x27;t repeat yourself). However, they&#x27;re intentionally listed here as a 
way of repeatedly demonstrating Platform Cache functionality

## Platform Event Recipes

### [PlatformEventPublishCallback](platform-event-recipes/PlatformEventPublishCallback.md)

Demonstrates how to write Platform Event publish success and failure callbacks

### [PlatformEventRecipes](platform-event-recipes/PlatformEventRecipes.md)

Demonstrates how to publish events on the event bus

## Quiddity Recipes

### [QuiddityGuard](quiddity-recipes/QuiddityGuard.md)

contains methods and static lists for rapid acceptence of a 
particular set of quiddities

### [QuiddityRecipes](quiddity-recipes/QuiddityRecipes.md)

Demonstrates the use and functionaly of Quiddity

## Schema Recipes

### [SchemaRecipes](schema-recipes/SchemaRecipes.md)

Responsible for showing how to use schema and schema tokens

## Security Recipes

### [CanTheUser](security-recipes/CanTheUser.md)

A reusable, intuitive library for determining wether or not the 
current use can create, read, edit, or delete objects as well as 
determining if the user has access or update permissions on specific fields. 
This class name was chosen to facilitate easy-to-understand and read code. 
Whenever you need to check FLS or CRUD access your code reads like this 
 `if(CanTheUser.read(new account())){}` making the calling and use of this 
code easy and intuitive.

### [StripInaccessibleRecipes](security-recipes/StripInaccessibleRecipes.md)

Demonstrates the use of Security.stripInaccessible() 
and the SObjectAccessDecision object. This helps developers write 
secure code that prevents users from seeing and accessing fields 
they cannot access.

## Shared Code

### [AccountServiceLayer](shared-code/AccountServiceLayer.md)

Demonstrates what a Service Layer object might look like 
for teh Account object. Demonstrates the placement of shared code that 
is specific to the Account Object, and contains code that is called 
by the AccountTriggerHandler

### [ApexClassUtilities](shared-code/ApexClassUtilities.md)

Contains reusable code dealing with ApexClass objects. 
This is primarily used by the LWC components for displaying code 
in an org.

### [ConnectApiWrapper](shared-code/ConnectApiWrapper.md)

Most Connect in Apex methods require access to real organization data, 
and fail unless used in test methods marked `@isTest(SeeAllData=true)` . 
An alternative to that, is mocking the calls to the ConnectAPI class. 
This class can be used to inject the ConnectAPI dependency, 
allowing its methods to be mocked in test classes.

### [DataFactoryForPackageInstalls](shared-code/DataFactoryForPackageInstalls.md)

Class generates data for installation cases where we cannot 
create example data via a Salesforce CLI call

### [FormattedRecipeDisplayController](shared-code/FormattedRecipeDisplayController.md)

this is the server side controller for the Formatted Recipe 
Display component. It has one method that delivers a class, and it&#x27;s matching 
test class to the UI for display. The component is reponsible for formatting 
and syntax highlighting

### [Log](shared-code/Log.md)

Generic logging framework that persists across DML reversions 
by publishing a Platform Event

### [LogMessage](shared-code/LogMessage.md)

A class for automatically attaching metadata to log messages 
like Quiddity and RequestID

### [LogSeverity](shared-code/LogSeverity.md)

A top-level severity enum for Log, and LogMessage to use.

### [OrderAppMenu](shared-code/OrderAppMenu.md)

A queueable class to prioritize this sample app in the org wide 
App Menu. This is done as a Queuable, because calling setOrgSortOrder causes 
an exeception if your setup script is also creating non-metadata records, 
for instance accounts.

### [OrgShape](shared-code/OrgShape.md)

Class contains static methods for determining if specific 
platform features are enabled. For example, do we have platform cache 
enabled. You could also write similar methods for experiences.

### [RecipeTreeViewController](shared-code/RecipeTreeViewController.md)

Provides the necessary data to populate a lightning-tree base 
component with recipe and group information

### [RelatedCodeTabsController](shared-code/RelatedCodeTabsController.md)

Apex server side controller for discovering other classes 
related to the one being viewed

### [RestClient](shared-code/RestClient.md)

This class provides an example of an intelligent abstraction for 
making REST callouts to external endpoints. It utilizes NamedCredentials 
for security. This class is designated as Virtual so that 
API Service classes can extend it, and make use of it&#x27;s methods easily. 
See the CovidTrackerAPI class for an example of how an API service class 
can extend RestClient. 
 
This class also provides static methods - so that the abstractions 
provided can be used in a one-off or ad-hoc manner for situations 
where a full API Service class isn&#x27;t needed. 
 
More on Named Credentials: 
https://sfdc.co/named-credentials

### [TriggerHandler](shared-code/TriggerHandler.md)

An opinionated trigger handler framework. 
Originally by Kevin O&#x27;Hara github.com/kevinohara80/sfdc-trigger-framework

## Testing Recipes

### [TestHelper](testing-recipes/TestHelper.md)

This class serves as a library of useful methods for writing 
more expressive, cleaner unit tests. Initialy this class contains a method 
for identifying the name of an object&#x27;s class expressed as a string.

## Trigger Recipes

### [AccountTriggerHandler](trigger-recipes/AccountTriggerHandler.md)

Demonstrates how to construct a TriggerHandler using the 
trigger handler framework found in Shared Code/TriggerHandler.cls

### [LogTriggerHandler](trigger-recipes/LogTriggerHandler.md)

Trigger handler for persisting Platform Event based 
log messages.

### [MetadataTriggerHandler](trigger-recipes/MetadataTriggerHandler.md)

This class exists as a unified, trigger handler class. It 
uses Custom Metadata, and introspection of the Trigger.new variable to 
determine what trigger handler classes should be called, and in what order. 
 
Metadata_Driven_Trigger__mdt has three fields: 
* Object__c - is a metadata entity look up to an sObject ie: Account 
* Execution_Order__c - is an integer and determines the order the trigger 
*   handlers are executed 
* Class__c - is a String holding the name of the Trigger Handler to execute 
 
Note: This Trigger framework works like this: 
 
An .trigger for a sObject invokes this class via: 
new MetadataTriggerHandler().run(); 
 
This trigger handler class extends TriggerHandler - all the trigger handler 
classes _must_ extend trigger handler. Most classes will only overwrite the 
context methods like afterUpdate(). This class, however, overrides the run 
method. This class is responsible for determining which other trigger 
handler classes to instantiate and run. 
 
Concrete example: 
AccountTrigger.trigger (in this org) - invokes this class. 
This class queries the custom metadata and will find (at least) one metadata 
record tied to Account and the metadata record&#x27;s Class__c specifies 
AccountTriggerHandler. This class then loops over the returned metadata 
records, instantiating the classes specified. It then calls the appropriate 
context methods on those classes. 
 
Note: The TriggerHandler framework below does *not* give you the ability to 
order, or re-arrange the trigger work of managed packages. It also does not 
allow you to declare the *order of methods* within the triggerHandler classes 
themselves. When using the MetadataTriggerHandler, it&#x27;s better to have a 
high number of singularly focused trigger handler classes than a few classes 
with multiple methods.

### [PlatformEventRecipesTriggerHandler](trigger-recipes/PlatformEventRecipesTriggerHandler.md)

Demonstrates how to construct a trigger handler for 
platform events

## Triggers

### [AccountTrigger](triggers/AccountTrigger.md)

### [LogTrigger](triggers/LogTrigger.md)

### [PlatformEventRecipesTrigger](triggers/PlatformEventRecipesTrigger.md)