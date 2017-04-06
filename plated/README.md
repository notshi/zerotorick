# Plated-Example


Plated is a node app, please make sure that node is available and that
the node dependencies have been installed using plated/upgrade.



The following scripts may be run from this projects root directory.

	plated/upgrade

This will install or upgrade plated using npm. It must be done at least 
once for the other scripts to work and can be run later to upgrade to 
the latest version.


	plated/build

Build the static website, once.


	plated/watch

Watch the plated/source directory and continuously build the static 
website when files are changed.


	plated/serv

Start a simple static server locally, visit 
http://0.0.0.0:8000/plated-example/ in your browser to view your 
site.


	plated/start

Run plated/watch and plated/serv simultaneously. This is the main 
script you should run to build and view your website locally whilst you 
edit it.


	plated/publish

Builds and then does a git add/commit/pull/push of all files to publish 
your pages to github. You may want to do this manually for more 
control.


	plated/pull

Pull the latest changes direct from the plated-example repository and 
attempt to ignore possible conflicts outside of this plated directory. 
Hopefully this will pick up small bug fixes in these scripts without 
breaking anything else.


	plated/settings

This contains settings used by all the other scripts and should not be 
run directly.

The website is generated into /docs from files found in /plated/source. The 
docs folder is used for publishing using github pages. Select 
master branch /docs folder as the source of your github pages under 
project configuration. Now you can build and git commit changes to 
publish to github pages.

If you want to publish this project using a different repository name 
be sure to adjust PLATED_ROOT=/plated-example in the plated/settings file from 
/plated-example to the new github name. If publishing to your main 
github page eg xriss.github.io then this should be set to / only.

    This is the root directory that your site is published to on github.

If you want to build into a different local directory then alter 
PLATED_OUTPUT=../docs in the plated/settings file to point somewhere else. 

    DANGER THE OUTPUT DIRECTORY WILL BE DELETED ON BUILD


# How to plated^

Here is a step by step guide to use this project as a starter for a github hosted website.

1. Visit https://github.com/new/import, 
paste `https://github.com/xriss/plated-example` into the URL and 
create a name for your new repository. Click **Begin import**.

    ![plated-eg](https://cloud.githubusercontent.com/assets/1515961/21818265/07abc360-d75f-11e6-8260-bf842eb2f7aa.png)

2. Edit the plated/settings **file** in your new project and change 
/plated-example to /your-project-name or if you are creating a 
yourname.github.io user or organisation site then change it to /

    ![settings](https://cloud.githubusercontent.com/assets/1515961/21817287/57385988-d75b-11e6-8a61-ac33fd259e78.png)
    
3. Goto the settings page for your new project and change the git hub
pages source to use the master branch /docs folder.

4. You can now use your new project as described at the start of this 
readme to create your own website on github pages. Be sure to run the 
plated/upgrade script first to install the node required dependencies.


Alternatively an easy way to pull all of the files from this project 
into an existing project is

`git pull git@github.com:xriss/plated-example --allow-unrelated-histories`

But beware of merge conflicts, where both projects contain the same 
file, you will probably conflict with this README.md file which can 
obviously just be replaced with your own version. Make sure you have 
node_modules listed in your .gitignore file.

	git pull git@github.com:xriss/plated-example

Can also be used to update the plated/* scripts later on.


Visit https://github.com/xriss/plated for plated documentation.
