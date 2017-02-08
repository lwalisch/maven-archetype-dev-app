# Maven Archetype: Executable Development App

This archetype can be used to create a simple development java app which can be executed very simple from the command line using the command `mvn -Pexecute`

## Prerequisites
- Git
- Apache Maven, refer to http://maven.apache.org/install.html for installation
- For Windows: A Bash emulation tool like Git Bash

## Installation 
Download this repository and move into the root directory:
```
git clone git@gitlab.com:LukasWalisch/mvn-archetype-executable-dev-app.git
cd mvn-archetype-executable-dev-app
```
Now the archetype has to be installed on the local maven repository using the command
```
mvn install
```
After that you are able to create a project from this archetype. To leave your computer clean after the installation, delete the downloaded repository using:
```
cd ..
rm -rf mvn-archetype-executable-dev-app
```

## Generate a new Project out of the archetype
After the installation is complete, the archetype is in your machines local maven repository. From now on you can generate as many new projects as you want out of this archetype.

Move to the directory where you want to create the new project and type
```             
mvn archetype:generate -DarchetypeGroupId=lwalisch.mvn-archetypes \
-DarchetypeArtifactId=executable-dev-app \
-DgroupId=<your group id> \
-DartifactId=<your artifact id> \
-Dpackage=test \
-DinteractiveMode=false \
-DarchetypeVersion=1.0
```
Make sure to change the values for DgroupId and DartefactId and Dpackage that it looks somehow like the example below:


### Example:
```
mvn archetype:generate -DarchetypeGroupId=lwalisch.mvn-archetypes \
-DarchetypeArtifactId=executable-dev-app \
-DgroupId=lwalisch.test \
-DartifactId=my-project \
-Dpackage=test \
-DinteractiveMode=false \
-DarchetypeVersion=1.0
```
## Run
to run the created project move into the directory and execute the command:

```
mvn -Pexecute
```

