# AL Studio
*Development Productivity Suite for Business Central*

## Available on Visual Studio Code Marketplace

Link: [https://marketplace.visualstudio.com/items?itemName=dynasist.al-studio](https://marketplace.visualstudio.com/items?itemName=dynasist.al-studio)

## Welcome
AL Studio is a VS Code extension that aims to enhance current working experience of  Microsoft Dynamics 365 Business Central development.
This repository is to provide a place for discussion, tracking issues and suggestions related to AL Studio.

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alstudio.png)


# Note:

## **This is a premium extension with a free, community edition.**
### **Premium subscription can be purchased on our website: https://al.studio/pricing**

---

## Introduction

AL Studio is a set of visual tools for editing, navigating or documenting AL Objects without complex running environments. It is built with a holistic approach that aims to provide users with better understanding of their whole workspace.

## Product showcase

Visit out our [YouTube channel](https://www.youtube.com/channel/UCyLKtnecuIOiD13dfmlI64Q) to see AL Studio features in motion.

## Features at glance

-   [Workspace overview](#workspace-overview-al-home)
-   [Scopes (bookmarks)](#scopes-bookmarks)
-   Visual Tools:

     -   [New workspace wizard](#workspace-wizard)
     -   [Translation overview](#translation-overview)
     -   [Table Fields, Fielgroups, Keys](#table-fields-fieldgroups-keys)
     -   [Snapshots](#snapshots)
     -   [Unified Search](#unified-search)
     -   [Table editor](#table-editor)
     -   [Page editor](#section)
     -   [Enum editor](#enum-editor)
     -   [Codeunit viewer](#codeunit-interface-control-add-in-viewers)
     -   [Interface viewer](#codeunit-interface-control-add-in-viewers)
     -   [Control Add-in viewer](#codeunit-interface-control-add-in-viewers)

 -   Navigation function for Objects, Event Publishers/Subscribers
 -   [Generate Internal/Public API documentation](#generate-documentation)
 -   [CLI interface for automation](#command-line-interface)
 -   [External API for VSCode extension developers](#external-api-for-vscode-extension-developers)
 -   [Known Issues](#known-issues)
 -   [Planned Features](#planned-features)

---
## Community Features
* [Workspace overview](#workspace-overview-al-home)
* [Scopes (bookmarks)](#scopes-bookmarks)
* Navigation function for Objects, Event Publishers/Subscribers
* [New workspace wizard](#workspace-wizard) 
* [External API for VSCode extension developers](#external-api-for-vscode-extension-developers)

---
## Workspace overview: AL Home

AL Home screen is automatically loading after opening a VS Code folder / workspace. It is designed to function as a starting dashboard for usual developer/consultant activities.
AL Studio can process the complete workspace information whether it be from downloaded symbols, runtime symbols or source files.

### Features

 -   Set active project, launch build/publishing or a debug session without the need of focusing on a project-related file.
 -   Overview workspace projects and their dependencies.
 -   Overview, search, filter objects, event publishers or subscribers.
 -   Show source or designer for selected objects, event publishers or subscribers.
 -   Organize selected entries into scopes (bookmarks).
 -   Advanced data grid allows customized filtering.

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alhome.png)

---
 ## Scopes (Bookmarks)

You can create focused sets of objects, event publishers or subscribers using the object list on AL Home screen and the "Add selected to Scope" button.

It is designed to help focusing on specific tasks or troubleshooting where a limited number of objects, event publishers or subscribers are involved.

Scopes are maintained in a local json file that can be excluded from source control or even be shared with other co-workers if needed.

### Features

 -   Creation of new scopes
 -   Scope entries can be added/removed individually
 -   Clicking on a scope entry opens related object editor or source code
 -   Deletion of a scope also deletes the related entries

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alscopes.png)

---
 ## Workspace wizard

This screen helps with creating complete workspaces consisting  multiple apps. The command is also available on the sidebar as a button when no workspace is open.

### Features

-   Set workspace name that will be the name of the .workspace file
-   Set root folder of the new workspace
-   Set basic information that will be applies to each new project
     -   BC Version
     -   Target (Cloud, OnPrem, etc...)
     -   Author
     -   Launch config
 -   Define multiple projects with its own ranges
     -   Set App name and folder name
     -   Set to add Test project
     -   Set Test project range

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alworkspacewizard.png)

---

## Translation Overview

This screen provides a matrix-like summary of all available XLF translations found in the workspace. Left columns represent data from generated XLF files, translations are dynamically displayed as additional columns.

### Features

-   View translations as filterable grid
-   Quick search
-   Export to Excel

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/altranslations.png)

---

## Table Fields, Fieldgroups, Keys

This screen provides a complete list of all fields, fieldgroups and keys that are present within workspace objects or symbol packages.

### Features

-   View all table Fields
-   View all table Fieldgroups
-   View all table Keys
-   Quick search
-   One-click navigation by clicking on Table or Field/Fieldgroup/Key name

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alstudio_tablefields.png)

---

## Snapshots

Snapshots screen in AL Studio provides a visual interface to overview and examine recorded snapshots within the workspace.
You can see the complete call-stack as a tree-view, and also the list of objects that were hit during the snapshot recording.

**Note**: this feature is in preview and subject to change in the final release.

### Features

-   List of workspace snapshots as a Project - Snapshot parent-child tree
-   Complete call-stack as a tree-view
-   Related objects: individual objects that are related to a snapshot
-   Start debugging for selected snapshot.
-   One-click navigation to source of related objects

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/ALStudio_Snapshots.gif)

---

## Unified Search

This screen provides a unified experience to search in many different areas of the complete workspace.

### Features

-   Search for Objects, Event Publishers, Subscribers
-   Search for Table Fields, Groups or Keys,
-   Search in Object Properties
-   Search in Translation files
-   Search in local source code
-   Search in Symbol package source code (if included)


![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/ALStudio_Search_Demo1.PNG)

---	

## Table editor

This view allows developers and consultants to overview and edit table structure.

### Features

-   Manage table fields, field groups or keys in a data grid
     -   Add, edit, delete items
     -   Copy-paste fields from Excel
-   Property window for selected item that shows related properties
-   Display table and its extensions in a single comprehensive view
-   Navigate to table or specific extension source

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/altable.png)

---

## Page editor

This view allows developers and consultants to overview and edit page layout without having to setup docker or local Business Central instances.

### Features

-   Display page and its extensions in a single comprehensive view
-   Navigate to page or specific extension source
-   Layout designer: visual representation of pages
-   Action designer: display action in a tree-structure manner
-   Changes: summary of changes made by page extensions
-   Property window for selected item that shows related properties
-   Menu bar: actions displayed the same as it is visible in the web  client
     -   Actions with RunObject property are navigable to load the related Page Designer
-   Screenshot: you can take a full-page screenshot of a given page.

### Layout:
![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alpage.png)

### Actions:
![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alpage3.png)

### Changes (extensions):
![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alpage2.png)

---

## Enum editor

This view allows developers and consultants to overview and edit enum structure.

### Features

-   Manage enum values in a data grid
     -   Add, edit, delete items
-   Property window for selected item that shows related properties  
-   Display table and its extensions in a single comprehensive view  
-   Navigate to table or specific extension source

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alenum.png)

---

## Codeunit, Interface, Control Add-in viewers

This window provides a general overview of any codeunit, interface of control add-in object. Methods and Event publishers/subscribers are displayed on two columns next to each other.

### Features

-   Search for method/event name
-   Show Properties
-   Show source code
-   Export method signatures to markdown file

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alcodeunit.png)

---

## Generate documentation

This module allows you to create a complete, markdown-based API documentation for a project or workspace. Markdown is a human-readable format that can be converted to HMTL or many other formats using external tools.

Generated files are internally navigable, there is a table of contents for objects and for methods/events inside the objects.

### Features

-   Single documentation creation from Codeunit/Interface viewer
-   Complete documentation creation for opened workspace
     -   One big markdown file is created
     -   A folder with one Markdown/object structure is also created  

---

## Command-line Interface

Command line availability streamlines product activation and helps integrating documentation generation, transferfield validation into DevOps build process.

### Features

-   Product activation
-   Documentation generation

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/ALStudio_CLI.png)

### Transferfield validation by ruleset definition

Ensure the integrity of Transferfields rules using validation json definitions per extensions.

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/ALStudio_CLI2.png)

**Parameters:**

`-w, --workspaces` : input folder of projects. 

It can be a single path or a comma-separated list of paths. In case of many apps within a main folder, specifying the main folder path is sufficient.

`o, --output` : path to save the validation result json file (optional).

You need to specify the complete path including filename.

**Validation Rules:**

Validation works using ruleset files named `transferfields.rules.json` that are placed into the root of each app folder. You can define rules per app.

```json
[
    {
        "Name": "Custom Table Transferfields",
        "Source": "MySalesTable",
        "Fields": [
            {
                "Id": 1,
                "Requirement": 2
            },
            {
                "Id": 2,
                "Requirement": 2
            },
            {
                "Id": 3,
                "Requirement": 2
            },
            {
                "Id": 5,
                "Requirement": 1
            }
        ],
        "Destinations": [
            "MySalesTargetTable1",
            "MySalesTargetTable2"
        ],
        "ErrorAction": 2
    }
]
```

Fields that are not listed in **Fields** member will still be validated using `Default` requirement type.


*Requirement values:*

|Value|Name|Description|
|-----|----|-----------|
|0|Default|Standard behaviour is validated only, e.g. Field Type match|
|1|MustOmit|Specifies that a field must not be present in related tables|
|2|Required|Specifies that a field must be present in related tables|

*ErrorAction values:*

|Value|Name|Description|
|-----|----|-----------|
|0|None|Validation is turned off.|
|1|Warning|Validation result only create output as warning, with ExitCode 0|
|2|Error|Validation runs normally with ExitCode 0/1 depending on result|


**Validation result:**

Result is displayed on command line output and also can be saved into a json file.
* Successful validation returns ExitCode 0. 
* Failure returns ExitCode 1, so in DevOps it will break the build.

![](https://raw.githubusercontent.com/dynasist/ALStudio/master/media/alstudio_transferfields.png)

---

## External API for VSCode extension developers

AL Studio has a public API that is available for other VSCode extension developers.
This API is provided even in the Free version and can be re-used by free/opensource extensions free of charge, without purchasing license.

Main API functions:
```javascript
export interface IExternalAPIService {
    isWorkspaceScanned: boolean;
    onWorkspaceScanned: Function | undefined;
    getObjects(): Array<CollectorItemExternal>;
    getNextId(type: ALObjectType, projectNameOrFilePath: string): Promise<number>;
    getSymbolUri(type: ALObjectType, name: string, standardFormat: boolean): Uri | null;
    getALLanguageApiService(): IALLanguageApiService;
}
```

Complete type definitions are available on GitHub: https://github.com/dynasist/ALStudio/blob/master/extension.d.ts

### Properties

#### **Syntax**
```javascript
isWorkspaceScanned: boolean;
```

Indicates whether the initial workspace scanning has been finished.

#### **Syntax**
```javascript
onWorkspaceScanned: Function | undefined;
```

Event fired when the initial workspace scanning is finished. You can subscribe to this event by assigning a simple function to it.

Example:
```javascript
alStudioAPI.onWorkspaceScanned = () => {
    console.log('Workspace has been scanned!');
}
```

### Methods

#### **Syntax**
```javascript 
getObjects(): Array<CollectorItemExternal>;
```

Gets the complete set of objects collected from files and symbol packages. It containes Objects, EventPublishers and EventSubscribers as well.
This list is automatically maintained by AL Studio, calling *getObjects()* will always return the latest, updated set.

#### **Syntax**
```javascript
getALLanguageApiService(): IALLanguageApiService;
```

Gets a simplified API reference for *AL Language Extension* itself.

#### **Syntax**

```javascript
getSymbolUri(type: ALObjectType, name: string, standardFormat: boolean = false): Uri | null;
```

Gets generated preview URI for symbol objects. This can be used to manually show source code preview window of specific symbols.

#### **Syntax**

```javascript
getNextId(type: ALObjectType, projectNameOrFilePath: string): Promise<number>;
```

Gets the next available object ID for the given object type in the specified Application name or file path. 
`projectNameOrFilePath` can be an:
1. App name exactly how it is defined in `app.json`, e.g. `Base Application`
2. Absolute filepath of any object within an app folder
3. Absolute filepath of the app folder
4. Absolute filepath of the app.json file

In latter case, the proper `app.json` will be implicitly search for.

### Getting an AL Studio API reference in another VSCode extension:

```javascript
import { extensions } from 'vscode';

async function getAlStudioAPI() {
    let alStudio: Extension<any> = extensions.getExtension('dynasist.al-studio')!;
    if (alStudio) {
        if (!alStudio.isActive) {
            await alStudio.activate();
        }

        return alStudio.exports;
    }
}

```

---

## Known Issues
Issues to be fixed before first release:

-   Saving changes from Table/Page/Enum editors to their respective files may fail and is unstable.
-   **[Solved]** Table/Page/Enum editors are not updated on outside file changes.
-   AL Home:
     -   **[Solved]** Removing an entry from a Scope does not work.
     -   **[Solved]** Caching is too aggressive: object list is not updated.
-   Translation overview:
     -   Language files are not yet synchronized automatically.
 -   Table editor:
     -   Copy-paste fields does not work.
 -   Page editor:
     -   Displayed Page view is a close but not 100% match to Business Central.
     -   Drag&Drop between Page Parts is possible. It should be prevented.
     -   **[Solved]** Display of System parts and User Controls are not yet implemented.
 -   CLI Documentation Generation: "Public Only" flag does not work.

## Planned Features

After first release:
 -   Create Languages/Edit Translations
 -   Report DataSet editor
 -   Query Designer
 -   XmlPort Designer
 -   Advanced editors for Property Window
