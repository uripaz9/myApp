# Blocks Local Development

Work locally and code your Wix site using any IDE. 

## Getting Started

Before reading this document, make sure you followed the steps in the Github onboarding section of the Editor, and successfully connected your Wix site to Github. 

## Setup 

To start coding locally, you need to clone your site, navigate to your site file’s directory, and initialize the velo environment into your local environment. 

Open your IDE and run the following CLI commands:

       git clone <your-repository-url>
       cd <site-directory>
       npx velo init

After running these commands, you can now start developing in your IDE. 

## Basic Usage

In the Github section of the Velo Sidebar you can see your site’s Github repository and the main branch. Note that the Editor is tied to the main branch. To learn more about how you can work with other branches, click here. 
Each time you push your local code to Github, the code will be automatically reflected in the Editor under Commit History.
When you publish your site, the latest code version from your main branch is published, and you can see the changes on your live site. 

## Preview your Local Changes

There are 2 ways to preview your local changes: 


**Using Wix Preview**


Run the following CLI command to open your site in preview mode and view your local code changes. Note that your local code changes and any updates in the Editor such as changes in the UI are automatically reflected in the preview tab. 


       npx velo open-preview


**Using a test site**

Run the following CLI command to open a test site with your local code changes. Note that your local code changes and any updates in the Editor such as changes in the UI are automatically reflected on the test site. 



       npx velo open-test-site


## Fetch Changes

Making changes to the UI on your Wix site, such as changing the name of a $w() element can affect your code. To make sure that your Wix site elements and local code are in sync, run the following CLI command in your IDE to continuously fetch real time changes to your local environment. 

       npx velo get-ui-changes --watch
       

## Publish Changes

To publish your code changes, push your local code changes to Github, and then publish your Wix site. You’ll then see the latest code version from the main branch on your live site. 


## Learn More

See our [Help Center Documentation]() to learn more.

