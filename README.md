# RWS
Translator plugin for Episerver/Optimizely

The RWS add-on manages languages and translations of content on multi-lingual websites. After an administrator installs the add-on, you can get additional RWS Menu in admin section where we can do following things :
- Save Configurations
- Create translation projects
- View translation projects

This Visual Studio extension only supports Visual Studio 2019 and EPiServer CMS 11 on .NET Framework 4.x.


#	Configure Episerver NuGet Feed

You need to add the Episerver Nuget feed within your Visual Studio, otherwise, you will not be able to find and install the Episerver packages. To add the feed, within Visual Studio click:
Tools ➡ Options➡ NuGet Package Manager ➡ Package Sources
 
Click the + icon and at the bottom add EpiServer as the name of the feed and within package source option, use this URL:

http://nuget.episerver.com/feed/packages.svc/

Click Update and you're done . In Nuget explorer, you should now see an Episerver option within the Online section. From here you can browse all the packages within the Episerver feed.


#	Install Package 

Now In the NPM(Nuget Package Manager), Browse for RWS.Translator and install it

 
#	RWS Menu

After install and run the application, there is RWS tab menu showing on website
When you click on nine dots left side of Dashboard you can see RWS menu tab in the Menu Section

# Dependencies

1.RestSharp  -   104.5.0
2.Entity Framework   -   6.1.0
3.PagedList.MVC   -   4.5.0
4.Newtonsoft.Json   -   10.0.3

# Run Database Script

After installation, you need to run the script to your respective database.you get the db script in the folder :  

RWS >> DBScripts >>  RWSSchemaOnlyScriptConnector.sql

Make sure to run the script successfully and your connection string should be correct in web config.

#	Configuration  
              
*	Username – textbox –  This information is shared by Product owner team (RWS team)
*	Password – textbox – This information is shared by Product owner team (RWS team)
*	Client Id – textbox – This information is shared by Product owner team (RWS team)
*	Client Secret – textbox – This information is shared by Product owner team (RWS team)
*	Base Url  – textbox - This information is shared by Product owner team (RWS team)
*	Page/Block properties – List – Select multiple available types in EPiServer which needs to be translated
*	Language Map –dropdown –  Select the variants(there are multiple language mapped with a particular language like en(English) has multiple variants example en, en-US, en-GB, en-NZ etc.) for the languages enabled in the EPiServer, it gets only those languages which are available in the cloud for translate
 o	First Field –  textbox –  Showing the enabled languages in EPiServer
 o	Second Field –  dropdown – fetch the available variants on behalf of enabled language in episerver from the cloud   


# Create Project 
 
*	Project Name –textbox–  it is a mandatory field as it represents the name of the project
*	Project Description – textbox– it is a mandatory field. This will shows the description related to the project.
*	Due Date – date – Select the due date of the project. It is a mandatory field
*	Project Option – dropdown– this section provides you the project options from the cloud.It is mandatory field and it render the source and  target language fields.
*	Source Language – radio button–fetch on behalf of project option value .it is mandatory filed, select the source language of your content
*	Target Language – checkbox–Select multiple target language which are getting on behalf of project option in which user wants to translate the content
*	Target Pages – checkbox tree structure – fetch the tree structure from the EPiServer site .select multiple target pages from tree structure .Here parents are pages and its child’s are blocks .It is mandatory fields 


# Enable Language

*	After selecting project option if source and target language doesn’t get (shows you need to enable language in admin section and select language at start page)  then you need to enabled the language in Epi Server Admin section and also select the language at start page section
*	To enable the language in EPiServer Admin tab, select config section >> Manage Website languages , you can add language or enable the languages after clicking on the language name
*	After enabling the language, you have to select the language at start page for that you need to select CMS menu from menu tab and here in the tools section, you can select the language settings
*	After selecting language setting, you can select or unselect the available languages as per your choic 


# Project
 

*	This section gets all the projects
*	Get your projects with the languages (target language) you want to translate the target pages/ blocks properties
*	Search : This enables the searching of the project 
*	Textbox : you can search with project name .
*	Dropdown : You can select the status of the project and search project with its status

*	It also shows the status with the : 
*	Approve/Reject
*	In Progress
*	For Download
*	Preparing
*	Completed
*	Partial Download
*	In Review
*	Reviewed
*	In Signoff
*	Signed off
*	For Vendor Selection
*	Cancelled


#	Schedule Jobs

According to the EPiServer User Guide, a scheduled job is a service performing a task (job) at a given time interval. An administrator can start a job manually. By default, EPiServer platform with EPiServer CMS and EPiServer Commerce includes several scheduled jobs. Some are enabled by default with preset values.

*	If the project status showing for download then after you can fetch the translated content for that you need to go to Admin section >> Scheduled jobs >> RWS Fetch Projects >> you can start manually or there is active checkbox you can set time interval in it.
*	Scheduled jobs are executed as per time interval or we can execute it manually as well
*	You can check the History section for job scheduler successful integration or the translated content fetched successfully or fetch with errors 
*	Now go to tree structure and fetch the target page you selected for translation for example we selected the     Whitepaper target page for translate the content
*	You can check it on website within the Edit Section >> Options >> View on website
*	This shows the translated content in German (de-DE) on website


 














