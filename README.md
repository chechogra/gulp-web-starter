#Gulp Web Starter Project Tutorial
This tutorial will make the assumption that you have never used a frontend workflow tool before and will walk through every step required to get up and running with gulp. We use WebStorm but you can choose any other IDE.

###Setup your project
 * Create a git repo on github (you will need it to create the package.json)
 * Create an empty project in webstorm and name it i.e **gulp-web-starter**
 * Please make sure you have installed *node, npm* and *bower (globally)* in your computer.
 
 ###Setup your module
 * Run `npm init`
 * Remove *main* from the package.json (we don´t need it for now). It should look like this:
```json
        {
      "name": "gulp-web-starter",
      "version": "1.0.0",
      "description": "Gulp Starter Project",
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "repository": {
        "type": "git",
        "url": "git+https://github.com/chechogra/gulp-web-starter.git"
      },
      "keywords": [
        "Gulp",
        "starter",
        "project"
      ],
      "author": "Sergio Granada <chechogra@gmail.com>",
      "license": "ISC",
      "bugs": {
        "url": "https://github.com/chechogra/gulp-web-starter/issues"
      },
      "homepage": "https://github.com/chechogra/gulp-web-starter#readme"
    }
```
###Setup Git
* `git init` (to initialize git repo)
* `git remote add origin https://github.com/yourgithubuser/gulp-web-starter.git`  (to bind the github repo to our local repo)
* Use the WebStorm built in plugin to create **.gitignore** files with the following keywords: (*JetBrains, Node, Sass, Linux, OSX, Windows, Bower*)
* push your changes

###Setup IDE code styling rules 
* Configure the editor rules for code styling. Create in the root folder a file called **.editorconfig** with the following content:
```txt
    # EditorConfig helps developers define and maintain consistent
    # coding styles between different editors and IDEs
    # editorconfig.org

    root = true


    [*]

    # Change these settings to your own preference
    indent_style = space
    indent_size = 2

    # We recommend you to keep these unchanged
    end_of_line = lf
    charset = utf-8
    trim_trailing_whitespace = true
    insert_final_newline = true

    [*.md]
    trim_trailing_whitespace = false
```
* Make sure the **editorconfig plugin** is installed (If not please download it and install it from webstorm or directly from http://editorconfig.org)

###Setup Bower
* Run `bower init`. After Running the command, modify the file to look like this:
```json
{
  "name": "gulp-web-starter",
  "version": "1.0.0",
  "description": "Gulp Starter Project",
  "authors": [
    "Sergio Granada <chechogra@gmail.com>"
  ],
  "license": "ISC",
  "keywords": [
    "Gulp",
    "starter",
    "project"
  ],
  "homepage": "https://github.com/chechogra/gulp-web-starter",
  "appPath": "app"
}
```
* Create in the root folder a file called **.bowerrc** to select the folder that bower is going to use:
```json
{
  "directory": "bower_components"
}
```

* Let's test our bower configuration by downloading our first component. Please run `bower install jquery --save` (the *--save* includes the dependency in the *.bower.json* file)

###Setup folder structure
* Create an html5 file called **index.html** under */app folder*.
* Create the following project structure as shown in the image (plase use the "mark directory as" utility in webstorm to distinguis resource folders, excluded folders and source content folders):

    ![Folder structure](https://lh3.googleusercontent.com/RS4NkTvzLRWrS4dqoJJck52rVi2jM6y90OTgh4X5Oz4RSb5waPf8vG6l1frPXPKo88c0DnLzK3K_hwB1_q1XUuDWAtu2sBM0413O7M1Bj04_1kmI58XCNdPcJY7aeWZjRRyT2AH1VGlpfUVNv7IpZSNvc4m3Sb2TjyrmbgGNOC7WDX4PJd8lLloMPvzAn7mlgvJ5UaDKSwGtfHE_ZuqnhLsuII-pzl_zTD1GrKIZ80yF1E7Uu061bVwHMUsDWHngT8RjK9LyvI2XX9YfkgCsF5koLETnLxD8OJ7tl4imGAw70n2TOzZnZ9dIu5eWqhZAXH4gvw6dfLzxC0_v_muB2SaYR-mUw4i7urfiGjpI6AIdAEBkjoCuICJ1egXznmDYPS7iSg5Xnh4_h7KhqNAhWKpDcry9CBk94jRasR-SueU_XTWQpEmYh9_mbb8Lh7OfGG5CQPjxnjqNCxW4bICE1GlDSBA-3vaXElJBh7eDb7FYVMmwkXFydYGL7PCa48eI5YGgz3Jzpk8Nle32eZtyRYQt2ufVwmQrCDUe_iBhVh2XY36YOVTrtfEg3I-xP7PmALs=w554-h648-no)

###Setup Gulp
* Let's install gulp by running `npm install gulp --save-dev` (the *--save-dev* includes the dependency in the *package.json* file)
* Create a js file called **gulpfile.js** under the root folder.

