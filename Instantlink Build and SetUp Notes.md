# INSTANTLINK BUILD AND SETUP NOTES

## FETCH THE LATEST CODE FROM GIT
Command:
git fetch
Explanation:
Downloads the latest changes from the remote repository without merging them.

## SWITCH TO A SPECIFIC BRANCH
Command:
git checkout 25.0.0
Explanation:
Changes to the branch named 25.0.0 to work on that version.

## CLEAN AND BUILD THE PROJECT, FORCE UPDATES
Command:
mvn clean install -U
Explanation:
Deletes previous build files, rebuilds the project, and downloads updated dependencies.

## UPDATE SYSTEM PACKAGE LIST
Command:
sudo apt update
Explanation:
Refreshes the list of available software packages.

## INSTALL REQUIRED PACKAGES
Command:
sudo apt install perl ksh cpio ncompress -y
Explanation:
Installs the necessary tools needed for building the project.

## BUILD PROJECT SKIPPING TESTS USING CUSTOM SETTINGS
Command:
mvn clean -DskipTests -s settings.xml && mvn install -DskipTests -s settings.xml
Explanation:
Cleans and builds the project without running tests, using a specific settings file.

## CREATE ALIASES FOR EASIER MAVEN COMMANDS
Command:
echo 'alias mvnc="mvn clean -DskipTests -s settings.xml"' >> ~/.bashrc
echo 'alias mvni="mvn install -DskipTests -s settings.xml"' >> ~/.bashrc
Explanation:
Adds shortcuts to run Maven clean and install commands with less typing.

## VIEW BUILD LOG FILE
Command:
less /home/suhasr/Desktop/instantlink/instantlink-install-obfuscated-jars/target/ZKM_log.txt
Explanation:
Opens the build log file so you can scroll through and inspect it.

## SEARCH THE LOG FOR ERRORS
Command:
grep -i error /home/suhasr/Desktop/instantlink/instantlink-install-obfuscated-jars/target/ZKM_log.txt
Explanation:
Searches the log file for any errors, ignoring case sensitivity.


