Video link :- https://drive.google.com/file/d/1GztPfBwM-O1E75tdjbpJd54NFmq_DyYL/view?usp=sharing

# AWS-with-appache-webserver
in this task i have hosted my website on aws ec2 instance using apache http webserver 

## Step Should be followed In AWS 
 - zip the website folder right click on it select winzip or 7 zip to archive 
 - Now go to AWS console management 
 - Go to service s3 bucket create bucket with any name set as default 
 - Now Make the bucket public 
 - Now set VPC if VPC is configured No need to make new one You can create new one 
 - Go to ec2 Machine launch Instance select machine .In my case i have chose Redhat8 </br>
   you can use any machine you want 
 - <b>Key:- Name  Value:- (any name) </b>
 - In security Group add rule:- select Http 
 - <b> Now Launch the Instance </b>
 - Genrate new Key pair <b>(With any name)</b> Download the pem key 
 ## step inside putty
 - Now Download Puty https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html latest version 
 - After installation Putty you will go to Putty gen key In your system . Now Load that key you have </br>
   downloaded Save as private Key and extention must be .ppk 
 - Open Putty <b> now paste your public IP of that Instance you have Created </b> in putty Hostname 
 - Lefthand side you will se SSH <b> go to SSH than Auth  Select Auth now load your ppk key that You have saved </b> 
 - Go to Session page lefthand side select Session page now open accept session
 - Login as ec2-user  <b> (Here we dont need password because we have Downloaded SSH Key and inserted in Putty) </b> 
 
 ## Step Inside Putty machine 
 - Now we successfully Connected to our VM 
 - <b>sudo su</b> (super power user root user) 
 - <b>yum update -y</b> (update your machine package)
 - <b>yum install httpd -y</b> (Installing apache in the system)
 - <b>pwd </b>(show path)
 - <b>cd /var/www/html </b> (path for where your Webpage are been saved)
 - <b>ls</b> (view content inside linux)
 - <b> wget (now go to s3 bucket click on zip copy object URL paste here)</b>
 - <b>ls </b>
 - <b>unzip xyz.zip</b> (unzip that file )
 - <b>ls</b>
 - <b>cd xyz </b> (inside that folder)
 - <b>ls</b> 
 - <b>mv * /var/www/html </b>(move all the content on this location)
 - <b>cd .. </b>(back from single directory)
 - <b>ls</b> (You will see yopur content of webpage here)
 - <b>systemctl status httpd</b> (view your service status)
 - <b>systemctl start httpd</b> (start your service)
 - <b>systemctl status httpd </b>
 Final step :- Go to aws instance copy your public ip and paste client side browser </br> Eg:- Chrome,Edge,Safari,Firefox (any browser and any where in the world can see your website)
 
