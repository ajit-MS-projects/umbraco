Umbraco Version Upgrade step-by-Step
Skip to end of metadata
Created by Ajit Chahal (S24H), last modified on Apr 14, 2016 Go to start of metadata
Umbraco version upgrade step by step process
 
General upgrade guidlines: https://our.umbraco.org/documentation/Getting-Started/Setup/Upgrading/general
Version specific (changes with every release) https://our.umbraco.org/documentation/Getting-Started/Setup/Upgrading/version-specific
Make sure all .proj of solution are Checked-in by all developers.
Make sure there is content freez - mean no content is added/changed by marketting or content managers 
Check out all files and folders of Umbraco_Web project (from source explorer) before nuget update package command.
Check out all packges from source control explorer
Make sure all dlls. Of …FS24Umbraco_Web\bin folder are also checked out
Make sure all new files in fiolder D:\dev\FinanceScout24\FS24Umbraco\FS24Umbraco_Web\config are checked out
Upgrade Umbraco via nuget,
In solution explorer click show all files
Look for new folders and files not in project and source control, specially under FS24Umbraco_Web\umbraco and umbraco_client folders, if any include in project
from source control explorer click add new items -> then select FS24Umbraco_Web\umbraco folder to recursively add new files under umbraco folder.
from source control explorer click add new items -> then select FS24Umbraco_Web\umbraco_client folder to recursively add new files under umbraco_client folder.
When prompted to upgrade global.asax, select NO
Make sure Global.asax is not updated or inherits from
<%@ Application Codebehind="Global.asax.cs" Inherits="FS24Umbraco_Web.MvcApplication" Language="C#" %>
After nuget is complete Compare all config files in D:\dev\FinanceScout24\FS24Umbraco\FS24Umbraco_Web\config folder and merge them in merge tool
Test CMS backend at local machine
Test CMS frontend at local machine
always remove the install folder immediately (in web project D:\dev\FinanceScout24\FS24Umbraco\FS24Umbraco_Web\umbraco\Install)
Check-in all files including new packages if any.
Create and Deploy package to DEV machines.
Smoke Test CMS backend on DEV - http://umbracocms.financescout24.dev/umbraco
Smoke Test CMS frontend on DEV - http://umbraco.financescout24.dev/
 
