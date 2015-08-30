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
 
 
USAGE: dobash [subcommand] [options] 

Available commands:

   list [droplet_id] [target] - Generic list attributes of a droplet (actions, kernels, snapshots, etc)
   
   listdroplets [droplet_id]  - List droplets: ID NAME PUBLIC_IP
   
   listkeys [droplet_id]      - List all SSH keys
   
   listips [droplet_id]       - List all ip addresses of given droplet id
   
   listmyimages [droplet_id]  - List personal backup images and snapshots
   
   getidbyname [droplet_name] - Retrieve a droplet id given the droplet name
   
   getname [droplet_id]       - Retrieve the name associated with a droplet id   
   
   help                       - Show this help message

   
   create    - Create a new droplet [name is the only required option]
   Example: $SELF create name=My.Cool.Droplet <region=nyc3> <size=1gb> <image=ubuntu-14-04-x64> <ssh_keys=null> <backups=false> <ipv6=false> <user_data=null> <private_networking=true>
               
   shutdown [droplet_id]
   
   poweroff [droplet_id]
   
   poweron  [droplet_id]
   
   snapshot [droplet_id]
   
   restore  [snapshot_id] [droplet_id]
   
   destroy  [droplet_id]
   
   
