# Pinnacle_DVH_Export

## Purpose
When Pinnacle DVHs were saved as text file, the data is Differential DVHs rather than Cumulative DVHs as what they displayed in Pinnacle. This script will export Differential DVHs and the convert them to Cumulative DVHs. 

## Method
This project is written with Pinnacle Script, awk and Python 2.7.9. From Pinnacle Tabular DVH, the script saves the DVHs, dose of max, mean and min and volume for selected ROIs and Trial as csv files. Awk read these files and generate Cumulative DVHs into MRN.csv. At the end of procedure, Python cleans the temparory files and read for next run.

## Requirements
* Multiple ROIs can be selected. No space in ROI names DVH selected is allowed.
* To distiguish which trial is exported, make sure only one trial is selected.
* Input interger Bin Size only.
* Minimum Bin Size is 1cGy (Lower Bin Size more accurate but spnd longer time). 

## Instruction of use
* Extract source zip file and put the folder into Pinnacle "/usr/local/adacnew/PinnacleSiteData/Scripts/HotScripts/Physics/".
* Make sure this folder and sub-folder have write permission for users.
* Run the initial script "start.Script" under the path "/usr/local/adacnew/PinnacleSiteData/Scripts/HotScripts/Physics/JL_DVH_Export_v2.4/".
* The procedure is finihsed when the script window closed.
* The final DVHs will be saved as MRN.csv under "/home/p3rtp/RadCalc/DVH/".
