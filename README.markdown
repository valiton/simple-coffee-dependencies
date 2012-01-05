simple-coffee-dependencies
==========================

What is this for?
-----------------

intention of this utility-script is to help you managing the Coffee-Files in your application.

How does this work?
-------------------

the script loops over all your specified files and concatenates them. before concatenating it replaces
all of your requires with the contents of the required file. this is done recursively, which means that
you can chain requires as much as you want. Just take a quick look at the example.

What do i need to use this script?
----------------------------------

to make this script work you need to have:

*	[node.js](http://nodejs.org) 
*	[CoffeeScript](http://jashkenas.github.com/coffee-script/) (of course)
*	[underscore.js](http://documentcloud.github.com/underscore/) (a nice little library)

if you have [node.js](http://nodejs.org) and [npm](http://npmjs.org/) already installed just install [CoffeeScript](http://jashkenas.github.com/coffee-script/) and [underscore.js](http://documentcloud.github.com/underscore/)
via [npm](http://npmjs.org/):

    $ npm install coffee-script
	$ npm install underscore

How can i use it?
-----------------

### How To Include in Your Coffee-Files

    #= require filename.coffee
    #= require folder/another_filename.coffee

### Shell Build Command

run this script in your shell with the following 2 parameters

* -I	(specifies a directory to include)
* -F	(basic files to be included)

you can include as much files and directories as you want, but you **must** at least specify 1 file (-F)
the script automatically includes the directories where your specified files are in

### Example
    $ coffee simple-coffee-dependencies -I folder1 -I folder2/subfolder -F first_file.coffee -F folder3/another_file.coffee > output.coffee