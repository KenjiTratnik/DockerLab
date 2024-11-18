
## Important Information
- IP address: 164.92.93.161
- Password: TulsaTime@1865edu

## Docker Compose Lab: Wordpress

## Purpose
- The purpose of this documentation is to guide you through the setup of the application Wordpress through docker. Wordpress being a “free and open source blogging tool and a content management system (CMS) based on PHP and MySQL, which runs on a web hosting service” per this Website. 

## Process
For simplicity and clarity any text in between [] is text that should be input into the command line

- Open up WSL
- To start this project I SSH’d into a host IP address with the command [ ssh root@164.92.93.161 ] and press enter
- A request for a password should show up, if not check if the IP you imputed is correct, the password is ‘TulsaTime@1865edu’ input that and press enter
- Once we are inside the host IP we then create a new directory, in this case I named it wordpress-docker which I recommend for simplicity, with the command [ mkdir wordpress-docker ] and enter that directory with [ cd wordpress-docker ]
- Once inside the directory we want to check if docker and docker-composed are downloaded that can be done the command [ docker -- version ] and [ docker-compose --version ] 
	- If they are not installed type into the console the following [ sudo apt install -y docker.io ] and [ sudo systemctl enable –now docker ] to install and enable docker to download Docker Compose type, or copy and paste, the following 
	- [ sudo curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep tag_name | cut -d '"' -f 4)/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose ] and [sudo chmod +x /usr/local/bin/docker-compose ]
- Once we confirm that docker and docker-compose are installed we then create the file ‘docker-compose.yml’ with the command [ nano docker-compose.yml ] 
- In your browser of choice look up ‘wordpress docker hub’ and click the first Link
- Scroll down the page until you see the title “... via docker-compose⁠ or docker stack deploy⁠”
- Copy the code starting with version: ‘3.1’ and paste it to nano
- Press [ Ctrl + x ] then [ y ] then press enter to save and exit the file
- Input the following command into the command line to start wordpress [ docker-compose up -d ] and let application download
- Once the download is finished we then go back to our local browser and input http://164.62.63.161:8080 into your searchbar
- Using my personal process as the example here; The following page should be showing

**DOESN'T SHOW HERE BUT A PDF FILE IS AVAILABLE IN THE REPOSITORY**

- Select “English (United States)”, unless you prefer another language.
- You then can now setup your wordpress account and start using Wordpress for yourself
- Once you are done with the process return to the command line and type the following [ docker-compose down ] to stop the process
- And if you want to leave the host IP type [ exit ] into the command line and it will return you to your personal ip host
