## Field

Field is an open-source software project initiated by OpenEndedGroup, for the creation of their digital artworks. It is an environment for writing code to rapidly and experimentally assemble and explore algorithmic systems. It is _visual_, it is _hybrid_, it is _code-based_. We think that it has something to offer a diverse range of programmers and artists. It is developed and tested on Mac OS X (primarily) and Ubuntu 12 + Nvidia proprietary drivers.

*Our main documentation website is here: http://OpenEndedGroup.com/field*

### Building

To build Field:

	git clone git@github.com:OpenEndedGroup/Field.git
	cd Field
	ant

That will build the core of Field. Individual plugins have additional targets inside the `build.xml` file. If want to build them all (and have both Max/MSP and Processing 2.0x installed) then `ant extras_all`

### Running --- Mac OS X

This repository is _inside_ a Mac OS X Application structure. That is, if you name this repository `field.app` then you'll have a double-clickable Mac app. To run from the command line, run 

	defaults write com.openendedgroup.Field use16 1
	Contents/MacOS/field_mac64.sh -field.scratch nameOfFileToOpen.field

To use an OpenJDK 1.7 VM place the .jdk bundle inside Contents/Plugins and:
	
	defaults delete com.openendedgroup.Field use16 

### Running --- Linux

To run:

	Contents/Linux/field_linux64.sh -field.scratch nameOfFileToOpen.field


