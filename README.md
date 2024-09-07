mongo_prune_js.js retained from archive.org for my own reference/retention after apparent deletion from unifi KB/forums.

How to. . . . . 

ssh root@192.168.1.1 (udm ip)

sudo -i

//make the file

nano mongo_prune_js.js

//copy in txt from the file mongo_prune_js.js above

//Close and save the file

//Perform a test run. To run a "dry run" issue the following commands:

sed -i 's/dryrun=false/dryrun=true/g' /tmp/mongo_prune_js.js

mongo --port 27117 < /tmp/mongo_prune_js.js


//Run the script. This will run the script without "dry run":

sed -i 's/dryrun=true/dryrun=false/g' /tmp/mongo_prune_js.js

mongo --port 27117 < /tmp/mongo_prune_js.js
