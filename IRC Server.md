# IRC Server
### Background
IRC stands for Internet Relay Chat. An IRC Server is an internet chat room that allows one-on-one communication as well as group chats. You can also transfer data and share files. 
### Installation
I used a Raspberry Pi with Raspbian installed. To download the software to my Raspberry Pi I ran the following commands in the terminal:

sudo apt-get update
sudo apt-get install ircd-hybrid

### Configuration
To make this server my own I needed to configure it. To open the server settings it I ran the following commands:

sudo su
cd /etc/ircd-hybrid
nano ircd.conf

When I typed that command in I got a long list of code. I then had to configure the setting to be able to access my server later. 

##### Name
I changed the name of the sever to “RaspberryIrc”

##### Description
I changed the description of the server to “Free speech on a Pi”

##### Network Name
I changed the network name to “RaspPi3”

##### Apply changes
I got out of the server info and restarted the server by running the following command:

sudo /etc/init.d/ircd-hybrid restart

### Testing
I tested the server by downloading Pidgin to a computer with Windows and accessed the server through the name and description, and I was able to successfully send a text into the chat. 
