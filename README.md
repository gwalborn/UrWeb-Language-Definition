Ur/Web
=======================

A set of Sublime Text 2 resources for Ur/Web. 

**If you had previously installed this package into your "Packages/User", you 
should consider reinstalling as described below to get future updates.**

# Included:

- Language definition for Ur/Web. Provides syntax highlighting in Sublime Text 2 
  and TextMate
- Snippets for common SML constructions: 'let', 'case', 'fun', 'fn', 
  'structure', etc
- Example theme "Son of Obsidian" that works with the Ur/Web language definiton
- Build system: will run urweb agains the project file within Sublime

# Installation:


To install, clone the git repository directly inside your
Sublime "Packages" directory. Due to the unfortunate naming of the git repo,
you will need to clone into a specifically named directory for the build 
system to work:

  git clone https://github.com/gwalborn/UrWeb-Language-Definition.git "SML (Standard ML)"

This way, you'll be able to "git pull" to update 
the package, and Sublime will see the changes immediately. You can use the 
Preferences>Browse Packages menu within Sublime to get to the Packages 
directory.

Otherwise, clone elsewhere and copy the files into a folder called 
"UrWeb" in the Packages directory.

# Features:

Syntax highlighing should work automatically with ".ur" and ".urs" files.
The .tmLanguage file should also work with TextMate to provide syntax highlighting.

Snippets will be available for all of the above file types. A full list can be 
found through the Tools>Snippets command. To use a snippet, start typing the 
name and press tab when the autocomplete window suggests the snippet. Currently 
included snippets are: 'case', 'datatype', 'fn', 'fun', 'functor', 'if', 'let', 
'signature', 'structure', and 'val'.

The example theme will be available under Preferences>Color Scheme. The example 
theme is an example of how to create a theme that matches SML. Most existing 
themes should work as this package uses a common naming scheme. This example 
.thTheme should also work with TextMate.

The build system will use the "urweb" command to compile the project with the
same basename as the file being edited. The build system can be started with
F7 or Control/Command+B.

On Linux, the build system will be able to locate urweb if it is available on your
PATH variable.

The build system captures error output with a regular expression, so double
clicking on an error in the output window will take you to the file and line
on which the error occured. Alternatively, use F4 and Shift+F4 to cycle through
errors.

# Troubleshooting

First, try closing all files, quitting Sublime, deleting the .cache files in the 
"UrWeb" directory under "Packages", and starting Sublime. Then reopen any files.

Finally, consider opening an issue on GitHub.

# Development:

Feel free to fork and contribute to this package. Any additions are 
appreciated.

.JSON-* files can be used to generate the .tm* files and vice versa, if you 
prefer to work with JSON. You will need the "AAAPackageDev" package for the 
JSON build to work. Note that this package uses the .tm* files and excludes 
JSON files, so be sure to build the .tm files and don't commit the JSON files.

Also be sure not to commit .cache files.

Originally written by Sean James, while taking 15210 at Carnegie Mellon.
Modified for UrWeb by Gary Walborn.

