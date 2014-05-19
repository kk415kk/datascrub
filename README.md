datascrub
=========

Series of scripts to scrub edX dumps into a more queryable format for research.

instructions
---
There are two ways of running this script:  
1. If all the course export .tar.gz files are in one folder, simply run the command:  
    `./generate_modulestore path/allCourseExports`  
2. If you want to specify one or more paths to various course export .tar.gz files, run with the parameter -m:  
	`./generate_modulestore -m path/courseExport1.zip path/courseExport2.zip ...`  

The outputted modulestore file will be in the same folder as the parsing script, named "modulestore.json".

To update the script without pulling the entire Github repo, simply run the command:
<br>`./generate_modulestore -u` or `./generate_modulestore --update`

updates
---
v0.05b (5/9/14): Fixed a bug where course exports have missing folders. Added a script self-update feature as well as logging.<br>
v0.02b (5/1/14): Fixed a bug involving how course exports store information (chapters and sequentials can store modules)<br>
v0.01b (4/30/14): Added support for for .tar.gz files so no extraction is necessary. Also added support for multiple extractions in one run. Fixed bug regarding bad JSON output format.<br>
v0.01a (4/26/14): Initial alpha version of script, capable of parsing one extracted course export folder.<br>

roadmap
---
* adding a "prettified" json parameter to be passed in (currently has to be modified in script)
* updating "data" fields of modules dynamically (known types: html, problem, video)
* ~~adding support to automatically extract .tar.gz files for course exports~~ - supported as of version 0.01b
* ~~adding support for multiple course exports~~ - supported as of version 0.01b

bug tracker
---

