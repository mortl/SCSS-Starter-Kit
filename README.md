# DevTips-Starter-Kit Gulp Version

Use this as a simple structure for a simple start to a simple site.

Visit [DevTipsStarterKit.com/](http://devtipsstarterkit.com) for more info.

![Watch the video on youtube](https://github.com/DevTips/DevTips-Starter-Kit/blob/master/assets/img/starter-kit-cover.jpg?raw=true)

## Requirements
This project have some requeriments you need to meet in order to compile it. First of all you need NodeJS in order to run javascript on the console, you can go to the [NodeJS](http://nodejs.rg) site and follow trough the installation process. After you get the `node` command on the console, you need to install Gulp and Bower globally with the following command.

```
node install -g gulp bower
```

Gulp is the one that will run all the task of compilation, watchers and others. Bower will get the dependencies for the client side like jQuery. Those are the only requeriments to run this project.

## Install
In order to start using the project you need to clone it to your pc. You can download the the zip version from [here](https://github.com/mriverodorta/DevTips-Starter-Kit/archive/Gulp-Starter-Kit.zip) or clone the project with the git command.
```
git clone -b Gulp-Starter-Kit https://github.com/mriverodorta/DevTips-Starter-Kit.git new-project
```
After you have it on you pc, you need to go in the console to the project folder and execute the following command to gather all the dependencies.
```
npm install && bower install
```
After the proccess finish you will have all you need to start coding.

## How to use
To start using it, the only thing you need to do is open the project on you code editor of choice and code. To compile and live preview all your changes you have some command that will help you. Here are the list of commands you should know.

Every command have to be executed on the root directory of the project using the gulp command like `gulp clean` or `gulp build`

* **start**: Compile and watch for changes (For development)
* **clean**: Removes all the compiled files on ./build
* **js**: Compile the JavaScript files
* **html**: Copy over the HTML files to ./build 
* **sass**: Compile the SCSS styles
* **images**: Copy the newer to the build folder
* **favicon**: Copy the favicon to the build folder
* **vendors**: Copy the vendors to the build folder
* **build**: Build the project
* **watch**: Watch for any changes on the each section
* **help**: Print this message
* **browsersync**: Start the browsersync server

If you are in the development proccess, the `gulp start` command is the best option for you. Go to the folder project in the console and execute `gulp start`, it will compile the project and start server that will refresh every time you change something in the code. The command will be waiting for changes and will tell you how to access the project from local and public url. Every browser that point to that url will be auto refreshed. As an extra feature for testing purpose any interaction on one browser will be reflected on any others. Try it on a phone, tablet and pc at the same time .

## Structure
The project have a very simple and flexible structure. If the default place for any file or directory needs to be moved, be sure to update the new position on the config file.

```
├───build -> All the compiled files will be placed here (Distribuction)
│   ├───assets -> Compiled Assets
│   ├───index.html -> Compiled Jade files
│   ├───vendors -> Project dependencies
├───source -> Source files for the project
│   ├───assets -> Assets for the project
│   │   ├───img -> Images
│   │   └───js -> Scripts
│   ├───sass  -> Sass styles
│   │   └───main.scss -> Main file in where all other sass files should be included.
│   ├───vendors -> Vendors folder for all the dependencies (Managed by Bower)
│   └───views -> Templates directory for html files
│   │   └───index.html
├───.bowerrc -> Define where the dependencies will be installed
├───bower.json -> Bower configuration file for manage project dependencies
├───package.json -> NodeJS configuration file for manage node dependencies
├───gulpfile.js -> Gulp Tasks
├───config.js -> Project configuration
```
All the files in the build folder will be auto-generated by the different tasks when compile the project. Be sure to not modify any file manually in the build folder because changes will be replaced on the compile process.

## Configuration
This project have some nice configuration options to meet all you needs. To configure you need to edit the `config.js` file and change any value you need. Every aspect of this configuration is described in the file so that you know the options.

## Updated for SCSS and HTML
This version has been modified to work with HTML and SCSS instead of Jade/Sass.
This is just a personal preference of mine, I might add to this project as well.
