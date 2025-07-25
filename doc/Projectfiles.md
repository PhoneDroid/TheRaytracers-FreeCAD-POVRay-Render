# Explaining the files

Different files will be created if you start the export/rendering.
This is a graphic overview:
![Project Files](img/Projectfiles.svg)

## Project files

The following five files contain the rendering project. The main reason for splitting the render project into different files is readability. But ".ini" and "_user.inc" provide special features.

### .ini file

This is the central project file. Normally this file is used for POV-Ray to store some basic render settings like the size of the image. We make improper use of it by storing other project information for the workbench in this place. The .ini file can be processed by FreeCAD **and** POV-Ray. So you can render your project independent of FreeCAD by just typing "povray myRenderProject.ini" at the command line.

### .pov file

Here is the converted model stored.

### _textures.inc

Here are all textures defined, that you set in the texture tab.

### _meshes.inc

Because we don't support all objects, some objects need to be converted to meshes. They are stored in this extra file to avoid unreadable pov file.

### _user.inc

Here you can define your own stuff. This file will not be overwritten and it is your access to all the fantastic things of the POV-Ray world. You will find more information at [Power User](PowerUser.md).

## Result of the rendering

### .png

This is the rendered image.

### _FC-View.png

This is a screenshot of the view in FreeCAD but with the same dimensions as the rendered image. It will be directly exported by FreeCAD but only if you check the box in the "Settings" tab of the dialog.

## Other important files

### .FCStd

No need to mention that this is your FreCAD model. Name and directory of this file are independent of your render project. In case you want to create more than one rendering from your FreeCAD model we recommend to create a subfolder for each.

### .predefined.xml

This file contains the declarations of the textures that will be shown in the right list of the "texture" tab. You can modify this file to add own textures.
