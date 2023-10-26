# apache-php-setup
Real time AWS Three Tier architecture using the aws EC2 + RDS + ALB + ACM + WAF ​

Step performed :- 
1] VPC :- 

       - Create a new VPC
       - Create a two subnet 1 is private and another is public 
       - Create a nat gateway for the private ec2 connectivity
       - Create a two route table for 1 is private & another is public
       - Attach public route to the public subnet & Private route to the private subnet
       - Create a 2 security group for public ec2 instance & Private ec2 instance

2] EC2 :- 
      
       - Create a one private server and private subnet & private security group to it 
       - Create a one public server and attach the public subnet & security group to it
       - Create a connectivity between public & private server 
       - Login to the private server and install the php & apache web server 
       - Configure the apache & set up the configration file for our website


3] RDS :-
       
       - Create a RDS BD mysql instance as a database
       - Connectivity between the RDS and the ec2 server 
       - Create a database in the rds server


3] ALB :- 
       
       - Create a one application load balancer 
       - Create a target group & add the private server to it.
       - Add the alb rule for the website URL 

4] ACM :- 

       - Create a acm ssl certificate & attach it to the load balancer 


5] Route 53 :- 
       
       - Add the recoed for our domain

6] WAF :- 
        
        - Create a web application firewall & add the numbe of rules to our website protection
        - Attche our application load balncer to th firewall
