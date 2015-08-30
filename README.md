# dobash
Dobash - Bash CLI for the DigitalOcean API

Dobash has two dependencies...

   jq: Install from here: https://stedolan.github.io/jq/

   Curl: from your package manager (ie, "apt-get install curl" "or yum install curl")

The Dobash interface is by no means complete. It provides rudimentary functions to retrieve information about droplets and perform certain actions on droplets.

Functions Provided

Actions...
    create, destroy, poweroff, poweron, snapshot, restore

Information...
    list, listdroplets, listkeys, listips, listmyimages 
    getidbyname, getname
    
type "dobash help" for usage information
 
 
