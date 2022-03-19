## Table of contents

* [Before Getting Started]()
* [Setup]()
* [Editor X Revisions]()
* [Dev Editor]()
* [Preview Your Site]()
* [Go to Production]()
* Commands:
  * [<code>velo dev</code>]()
  * [<code>velo install-package</code>]()
  * [<code>velo live-preview</code>]()
  * [<code>velo deploy-preview</code>]()
  * [<code>velo publish</code>]()
* [Work with your team]()
* [Community]()
* [Learn More]()

## Before Getting Started

* Make sure you successfully connected your site to Github in the Online Editor. 
* After connecting to GitHub, you’ll only be able to edit code in the external IDE. Code in the Online Editor will be in read-only mode.
* The online Editor is tied to origin/main branch. The code is automatically updated upon every push to origin/main

## Setup 

To set up your local environment and start coding locally, run the following CLI commands in your terminal:

1. Clone your site 

  ```js
git clone <your-repository-url>
  ```

2. Navigate to your project directory

```js
cd <site-directory>
```

3. Run the init command to add the necessary dependencies, including node packages, Velo CLI and the types folder necessary to support Velo auto-complete and error indications. Note that running this command may prompt you to log in to Wix. 

```js
npx velo init
```
Now you can start developing in your IDE. 

## Editor X Revisions
The repository contains the site's code and a reference to an Editor X revision in the velo.config.json file. Editor X revision represents the state of your site except the code: design, schemas and applications. While designing in Editor X, both Online & Dev, revisions are periodically created. In the Dev Editor you also have a ‘Sync Changes’ button, which creates new revisions and updates it in your local code.

## Dev Editor 

To make editor changes while editing code locally open the Dev Editor by running 

  ```js
velo dev
  ``` 

Dev Editor runs your local code with the latest Editor X revision from the Online Editor, and allows you to make editor changes while editing code. Note that you will be working in concurrent mode with other users - each editor change that you make will be reflected to all other team members and vice versa.

After making the needed changes (design/schema/ids) in the Dev Editor, you have to click on the ‘sync changes’ button in the editor top bar, so that your local code will point to an Editor X Revision that contains your latest editor changes.
‘sync changes’  creates a new revision and updates your local code files with the newly created revision number, as well as, type files that correspond to the new design.

Hot reload - While ‘velo dev’ command is running, each time you edit code in your preferred IDE, the Dev Editor automatically updates with these changes.

## Preview Your Site 

When developing locally, you have several options to preview and test your local changes:

__Live preview__ - Open a temporary version of your application or site in a production environment, with a hot reload mechanism, which automatically syncs any code change done in your local IDE.

  ```js
velo live-preview
  ``` 
__Deploy preview__ - Create a new shareable version of your application or site in a production environment. This version will be based on your local code and the Editor X Revision stated in velo.config.json file.

  ```js
velo deploy-preview
  ``` 

__Preview mode in Dev Editor__ - by entering the preview mode in Dev Editor you can see a preview of your site with your most current code and the latest Editor X Revision, interact with your site and debug your site’s code.


## Go to Production 

To publish your local code changes, do the following: 
Push your local code changes to origin/main by running the Git command, `git push`. 
Note that the Editor is tied to the main branch, and updates with the latest code change pushed to origin/main.
Run ‘velo publish’ CLI command to publish the latest commit in origin master, and the editor revision stated as part of this commit. Alternatively, you can click Publish in the Online Editor. Note that clicking Publish in the Online Editor publishes the latest Editor X Revision, along with the latest code changes in the origin/main branch. 

  ```js
velo publish
  ``` 

## Work with your team

To allow teammates to access your GitHub repository, edit code, and make changes to your Editor X site, you’ll need to both:
1. Add them as contributors in the Editor as Admin role
1. Invite them as collaborators on your repository in GitHub.

[Learn more about working with your team]()

## Community

[Discord]()

[Twitter]()

## Learn More

See our [Help Center Documentation]().

Watch a [Velo Local video tutorial]().





