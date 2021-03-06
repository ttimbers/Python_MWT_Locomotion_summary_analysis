# Summary analysis of Locomotion experiments on the Multi-worm Tracker
The aim of this project is to create software that can be used after running
a 600s basal locomotion experiment using the Multi-worm tracker (Swierczek et al., 2011)
to generate summary figures and statistics for that experiment. 

This script also backs up experiment .zip files to a webdav server specified by the
user. 

## Figures it generates
* Speed versus time over experiment duration
* Radial and boxplot pathlength figures from 530-590s
* Spontaneous reversals/minute box plot (averaged over 470-590s)
* Body size box plots (area, length and width)

## Statistics reported
* Mean initial speed (averaged over 30-45s) for each strain, and ANCOVA comparing to wild-type
* Mean final speed (averaged over 575-590s) for each strain, and ANCOVA comparing to wild-type
* Mean pathlength measured over 530-590s for each strain, and ANCOVA comparing to wild-type
* Mean number of spontaneous reversals/minute (averaged over 470-590s) for each strain, and ANCOVA comparing to wild-type
* Mean area, length and width for each strain, and ANCOVA comparing to wild-type

## How to use it

* Set working directory to project's root directory

* Call locomotion_driver.sh from the Bash Shell

* locomotion_driver.sh requires the following arguments from the user: webdav server URL,
path on webdav where .zip folders should be saved, the path to chore.jar 
(offline analys program Choreography), and the gigabytes of memory to be used to run 
Choreography. See example below:

~~~
bash bin/locomotion_driver.sh https://webdav.server/location folder_to_backup_to 
/Users/this_user/Chore.jar 16
~~~

* This code is not working yet. More instructions to come as code is developed further.

