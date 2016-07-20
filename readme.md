# ansible-hiddenservice
Ansible to set up a Tor Hidden Service on DigitalOcean

# How to use
You need an API key from DigitalOcean in an environment variable called DO_API_KEY.
Now simply run `ansible-playbook instant-hiddenservice.yml` and wait for the script to complete. At the end
it will output the hidden service URL. 

The script creates a new droplet named _hiddenservice_ and installs nginx and tor on it.

If you want to change the default page being served by your HS, edit the file roles/webserver/templates/index.html.j2