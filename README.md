## Velo Local Dev
Velo Local Dev allows you to develop locally and code your Wix site as a team using any IDE. 

### Getting Started

Before reading this document, make sure you followed the steps in the Connect to Github section of the Editor, and successfully connected your [Wix site code to Github](). 

**Important:** 
Once you connect your Wix site to Github, you can only develop in an external IDE, and are no longer able to use the Code Panel and Properties & Events Panel. 
The Github repository contains your Wix site code, and a reference to an Editor Revision number representing a version of your Wix site with specific data, layout, and design.
Changes to the design and schema can only be done in either the Local Dev or online Editor. 
The online Editor is tied to the main branch, and continuously updates with the latest code in origin/main. 

### Setup 

To set up your local environment and start coding locally, run the following CLI commands in your terminal:

Clone your site 

  ```js
git clone <your-repository-url>
  ```

Navigate to your project directory

```js
cd <site-directory>
```

Set up your local environment to add the necessary dependencies, including node packages and a types folder necessary to support Velo auto-complete and error indications. Note that running this command may prompt you to log in to Wix. 

```js
npx velo init
```
After successfully running these commands, you can now start developing in your IDE. 

### Test Your Local Code Changes
Run the following command to test your local code with the latest Editor changes. A new tab opens in your browser with the Editor in Local Dev Mode. 

```js
npm run editor –latest
```


While the command is running and the tab is open, the Editor in Local Dev Mode continuously runs your local code files. As you make changes to your local code, the Editor in Local Dev Mode updates with your changes. 
### Test Editor Changes with Local Code
You may want to test changes in the Editor with your local code. Because changes in the Editor may be frequent, the Editor in Local Dev Mode includes versioning called Editor Revisions. As you’re developing locally, when you and your teammates make design changes in the Editor, you can click Create Revision to create a new version of the site with your changes. Revisions are also periodically created. You can see the revision number indicated by Editor Revision: #. There is a velo.config.json file in your local code that refers to a specific Editor Revision number. When a new revision is created, your local code files are automatically updated to reflect the newly created revision. This includes the velo.config.json file, and all the other files necessary for supporting autocomplete and autocorrect for the components that were edited in the new revision. For example, in this revision, if someone adds a new page to the Editor using the Add Panel, the page is automatically added to your local code files. Additionally, in this revision, if someone adds a new element to the Editor, the element is automatically added to the types folder in your local code files.

Note: If the Editor Revision number is higher than the current Editor Revision number in the velo.config.json file, run the `npm run editor –latest` command above and the velo.config.json file will update to the latest Editor Revision number along with all the other files necessary for supporting autocomplete and autocorrect for the components that were edited in the latest revision.



### Preview Your Site
To preview your site with your latest local code changes and the latest Editor Revision, check that the command `npm run editor –latest` above is still running, and the tab with the Editor in Local Dev Mode is still open, and click Preview.

### Changes to the Main Branch
Before you push your local code changes to Github, check the main branch for updates made by your teammates. Run the Git command, `git pull` to pull any updates from the main branch, such as a new page into your code before pushing your local code changes. 

### Publish Changes

To publish your local code changes, do the following: 
Push your local code changes to Github by running the Git command, `git push`. 
In the Github tab of the Velo Sidebar, you can see your site’s Github repository and the main branch. Note that the Editor is tied to the main branch, and updates with the latest code change pushed to origin/main. Clicking Preview opens a preview of your site with the last merged code in the Main branch and the latest UI changes. 
If you aren’t working on the Main branch, open a Pull Request and merge your local code changes to the Main branch on Github.
      1.   Click Publish in the Editor. Note that clicking Publish in the Editor publishes the latest Editor Revision, along with the latest code changes in the main branch. 

### Learn More

See our [Help Center Documentation]() to learn more.




