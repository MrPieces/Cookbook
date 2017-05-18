Installing ArangoDB unattended under Windows
============================================

Problem
-------
The Available NSIS based installer requires user interaction; This may be unwanted for unattended install i.e. via Chocolatey. 

Solution
--------
The NSIS installer now offers a ["Silent Mode"](http://nsis.sourceforge.net/Docs/Chapter3.html) which allows you to run it non interactive
and specify all choices available in the UI via commandline Arguments.

The options are as all other NSIS options specified in the form of `/OPTIONNAME=value`.

#Supported options

*For Installation*:

 - PASSWORD - Set the database password. Newer versions will also try to evaluate a PASSWORD environment variable
 
 - INSTDIR - Installation directory. A directory where you have access to. 
 - INSTALLTYPE - one of the three:
    - Service - launch the arangodb service via the Windows Services
    - AllUsers - copy it into the directory for all users
    - SingleUser - copy it into the home of this user
 - DESKTOPICON - [0/1] whether to create Icons on the desktop to reference arangosh and the webinterface
 - Specify one of the three:
   - NOPATH - [0/1] don't alter the PATH environment at all
   - ALLPATH - [0/1] add it to the path for all users
   - CURPATH - [0/1] add it to the path of the currently logged in users
 - STORAGE_ENGINE - [auto/mmfiles/rocksdb] which storage engine to use (arangodb 3.2 onwards) 

*For Uninstallation*:
 - PURGE_DB - [0/1] if set to 1 the database files ArangoDB created during its lifetime will be removed too.

#Generic Options derived from NSIS

 - S - silent - don't open the UI during installation
