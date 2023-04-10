SWE645 : Component based Software Development
Assignment 1
Name : Vaishnavi Gururaj
G Number : G01399296
Email id : vgururaj@gmu.edu


Part 1 : Homepage creation
Link : https://assign1swe645.s3.amazonaws.com/index.html
I created web pages using html and css along with bootstrap. I downloaded the compiled ready-to-use css and js bootstrap files and provided the bootstrap.min.css(at the top), bootstrap.min.js(end of the file so that the content loads faster), popper.js etc dependency links in my html. This was done because the requirement was to use an external style sheet and the bootstrap.min.css file that has been uploaded satisfies the requirement as it is essentially a style sheet that I have uploaded.
I created an AWS account and created a S3 bucket by enabling the Static Web Hosting option. I uploaded my files into my bucket and the link given loaded my index file.
Giving https://assign1swe645.s3.amazonaws.com/error.html any random http://assign1swe645.s3-website-us-east-1.amazonaws.com/sdfs should let you view the error file. If it doesn't work for random inputs, refreshing the bucket helps.

Part 2 : Survey Form creation
Link : https://ec2-18-224-183-137.us-east-2.compute.amazonaws.com/assignment1/
I created a survey form similar to the above given steps and exported them into a assignment1.war file. I created an EC2 t2-micro instance as it was free-tier-eligible with a Tomcat image on it. I downloaded the keys as I had enabled the public key security option. I used the commands : 
scp -i assign1swe645.pem assignment1.war bitnami@ec2-18-224-183-137.us-east-2.compute-1.amazonaws.com:stack/apache-tomcat/webapps 
Ssh -i “assign1swe645.pem” bitnami@ec2-18-224-183-137.us-east-2.compute.amazonaws.com
I went into the directory “webapps” directory to check if my war file is in the right place after moving it into stack/apache-tomcat/webapps. Then, I went into stack/apache-tomcat/bin and used ./startup.sh and ./shutdown.sh commands as needed. The war file is included in the root directory of the zip folder.

The zip folder contains an index.html file, error.html file, form.html file and assignment1.war file and a bootstrap folder which included bootstrap styles and an image folder that includes three images used in different files.