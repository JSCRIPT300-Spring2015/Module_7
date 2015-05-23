## Module_7 assignment

For this assignment, you're going to set up your class project repository following the structure detailed below. Once you have completed it, you are going to fork this repository, update the README.md with a link to your project repository, then initiate a pull request. __NOTE__: the fork of this repository is NOT your project repository. You are simply forking this repository so you can update the README.md file with a link to your project repository. You can view the [project_structure](https://github.com/JSCRIPT300-Spring2015/project_structure) repository to see (or even fork) the structure you need to use.

To set up your project repository (as a separate repository - not the fork of this assignment repository), add to it the following:

an Express server that serves up the following endpoints:

__GET__ /trucks

__GET__ /trucks/:id

in the root of your project you must provide the following files:

- a LICENSE file for your project - when you create your repository, you will have the option to select the license you feel is most appropriate for your project. I've been using the MIT license for all of the class assignments, but this is your choice for your project.
- a README.md file for your project - this is what will explain what your project is and any necessary documentation for your repository. Populating a README file is also an option you can check when creating your repository.
- package.json - this should have both a dependencies section for application dependencies
and a devDependencies section for grunt, grunt-contrib-jshint, and any additional plugins you wish to use later (we will briefly cover using minification and concatenation for the production versions of your js and css assets.)
- .gitignore file the prevents any node modules from being part of your github repository
- Gruntfile.js that defines a jshint task and makes it the default task. When it runs, it lints all of the .js files in your entire project, including the Gruntfile itself.

in an app directory, provide the following file:

- app.js - this is the main application file that instantiates your application, connects to mongodb, requires and uses any necessary middleware (note: only include body-parser if you intend to add POST or PUT routes to your application - they are not required for your project, so this middle-ware isn't required either) such as the middle-ware returned by express.static(). It is recommended you leverage the work you've already done in previous assignments for this.

Inside the app directory there will be a models directory and a routes directory. Inside of each, respectively, include the following files:

- truckModel.js - this defines the same foodTruckSchema as the Module_5 assignment, and exports the Truck model. It is recommended you leverage the work you've already done in previous assignments for this.
- truckRoutes.js - this defines the __GET__ /trucks and __GET__ /trucks/:id routes. __*Optionally*__ you can also define the __POST__ /trucks, __PUT__ /trucks/:id, and __DELETE__ /trucks/:id, but they aren't required for your project. NOTE: for a public application, exposing __POST__, __PUT__, and __DELETE__ routes can put your data at risk, so make sure you take care with implementing these routes if you choose to do so. It is recommended you leverage the work you've already done in previous assignments for this.

Inside the public directory, provide the following file:

index.html - this is the main file served up for visits to your root url. This file should include jquery.js, underscore.js, backbone.js, and your main.js - the main entry-point for your client-side application. This file doesn't need any implementation inside it yet, but it should be present inside the js directory.
Your index.html file can either link to CDN versions of the 3rd party libraries mentioned, or you can put copies of them inside the js/libs directory and point your script elements at those versions instead.

Inside the public directory there will be a js directory, a css directory, an img directory, and a libs directory. Inside the js directory will be a models directory, a collections directory, a views directory, a templates directory, and a routers directory.

Feel free to add onto this structure if desired. The listed files are the base requirements only. We will be populating the js/models, js/collections, js/views, and js/routers directories with files for your client-side application the next two weeks. Also feel free to start adding tests for your application as well. They are not required, but a tests directory has been supplied for your application to use for this purpose.

This assignment is due by Saturday, May 30th by 7pm. Once grading has been completed, a :+1: comment will be added to the pull request and the pull request will be closed.