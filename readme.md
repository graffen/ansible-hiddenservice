# ansible-hiddenservice
Ansible to set up a Tor Hidden Service on DigitalOcean

# What the script does

 * Creates a new DigitalOcean droplet
 * Runs apt-get update && apt-get upgrade on it
 * Installs and configures Tor for a Hidden Webservice
 * Installs Nginx and configures a web site to listen for connections from localhost
 * Disables server tokens in Nginx config
 * Outputs a summary at the end, giving you the HS URL. 
 
# How to use
You need an API key from DigitalOcean in an environment variable called DO_API_KEY.
Now simply run `ansible-playbook instant-hiddenservice.yml` and wait for the script to complete. At the end
it will output the hidden service URL. 

If you want to change the default page being served by your HS, edit the file roles/webserver/templates/index.html.j2