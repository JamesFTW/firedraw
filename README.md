# Fire Draw

![logo](https://i.imgur.com/d8abuTQ.jpg)

Members: James Andrews, Michael Swanson, Peter Le, Alonzo Contreras

Github: https://github.com/sfsu-csc-667-fall-2018/term-project-fire-squad-1

Welcome to Fire Draw! This is a parody of JackBox Games Drawful, all rights belong to JackBox.

### About
Players are presented with a word they must try to draw on the screen. The image is then shown to all players who attempt to guess the original word, with points awarded to players that select the original word and to players that have their response voted as the "correct" word.

You can play the game here:
firedraw.herokuapp.com

### Dependencies

Fire Draw uses a number of open source projects to work properly:

* [React.js](https://reactjs.org/) - used for client side rendering
* [node.js](https://nodejs.org/en/) - evented I/O for the backend
* [Express](https://expressjs.com/) - fast node.js network app framework
* [Canvas API](https://canvas.instructure.com/doc/api/) - used for drawing on the page
* [Socket.io](https://socket.io/) - framework used for in game and lobby chat
* [Passports](http://www.passportjs.org/) - authentication
* [React Router](https://reacttraining.com/react-router/) - for client-side routing
* [bcrypt](https://www.npmjs.com/package/bcrypt) - encrypting passwords

##  Development
### Install from source
In this section we will download and install the game to run locally on your computer. You will need to install several tools and run your own server to run the game. We will be using Heroku, Postgres, and AWS. You are more than welcome to use any tools you feel more comfortable with but do caution that you might not be able to follow along with this guide. That being said, lets begin:
  - First you will need to download the game from the github repo found here    
    https://github.com/sfsu-csc-667-fall-2018/term-project-fire-squad-1
  - Click the clone/download button
  
	 ![download button](https://i.imgur.com/9k2D3x8.png)
  - Upon doing so you will then click on copy link
  
	![copy button](https://i.imgur.com/iYcqLuy.png)
  - Press the copy link button in order to use the github command on the terminal, otherwise press Download ZIP to download it directly. If you do this skip the next step.
  - Open the terminal, you will then type git clone and  paste the link you copied from the repo
```sh
git clone https://github.com/sfsu-csc-667-fall-2018/term-project-fire-squad-1.git
```
  - NOTE: you will need to have git commands installed on your machine, you can find the documentation for downloading git here 
  
	  https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
  - While still in terminal, we will want to go into the folder
```sh
cd ~/term-project-fire-squad-1
```
- Now that we are in the root folder we will now create the environment to run the server
	- You will have to create your own postgres database on heroku
	
	https://devcenter.heroku.com/articles/heroku-postgresql
	- Then you will have to create your own aws server and have the following
		- access key id
		- secret key
		- session secret
	- Follow this documentation to build the server from aws
	
	https://docs.aws.amazon.com/efs/latest/ug/gs-step-one-create-ec2-resources.html
	
	this link will explain how to get the access keys and secret keys
	
	https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys
- Now that you have the following, open your text editor and write the following
```sh
HEROKU_POSTGRESQL_TEAL_URL='database url'
AWSAccessKeyId='key'
AWSSecretKey='key'
SESSION_SECRET='session'
```
- make sure to replace 'key/url' with the actual keys/url
- save it and name the file .env
-  you should now see this in your root folder
![root](https://i.imgur.com/Ku9q7ns.png)
- NOTE: to run the server you will need npm installed on your machine, if haven't done so, run the following command:
```sh
sudo apt install npm
```
- While still in root, we will want to install the independencies
```sh
npm install
```
- To run the server we will run the command
```sh
npm run start:dev
```
- Now that the server is running we will want to start the client
- Open a second terminal window and cd into client directory
```sh
 cd ~/term-project-fire-squad-1/client
 ```
 - We will also want to install the independencies on the client
```sh
npm install
```
- Now that the independencies are installed we can start the client
	- NOTE: make sure that the server is still running when we last ran 'npm run start:dev'
```sh
npm run start
```
- This will open a window on your browser with the login page
- Congrats you have a local game server on your computer!

### Architecture

