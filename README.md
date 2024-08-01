# Deploying-Node-Js-application-on-Aws
I deployed node js application on Aws

Go to AWS console and create an Iam user and attach policies directly to that iam user by giving adminstartor full access and EC2 full access.

Login to aws console using iam and create an ec2 instance on iam role

And connect to ec2 instance using 

ssh -i .pem ubuntu@public ip

After connecting to an ec2 instance do sudo apt update

Now install node js by using command 
sudo apt install node js
And do 
sudo apt install npm
Go to the specific application directory and do cd in it
Do ls to check whether all the files are there or not
Now create environment variables by creating environment file using touch command -> touch .env
Do ls -a to check list of all files.
To edit the env file use vim env
And give this in env file
DOMAIN= ""
PORT=3000
STATIC_DIR="./client"

PUBLISHABLE_KEY=""
SECRET_KEY=""
And save the file using :wq!

Do npm install
And do npm run start 

And access the application by doing http://public ip of ec2:3000
And also make sure to edit inbound security rules by opening tcp port with 3000 and access the app in the browser.

