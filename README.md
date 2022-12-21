# EKS-Challenge

Solution for Technical challenge assignment
Note: I have deleted the environment to lower my EKS bill please check shared screenshot
Questions
1.	This deployment is currently not working properly; can you figure out why.
Answer: 
•	Service port were wrong, Target Port changed from 80 to 8000.
•	Environment variables in configmap were incorrect added with correct values for each deployment. Please refer configMap.yaml
•	three Different values.yaml files 3 deployment added, Please refer 
values-ami.yaml , values-amigo.yaml & values-freund.yaml
2.	When querying different endpoints it should show each of the different services you created on the previous step:
o	http://<address>/de should show "Hello Freund"
o	http://<address>/es should show "Hello Amigo"
o	http://<address>/fr should show "Hello Ami"
Answer:
•	Created a AWS ALB ingress Controller for Context Path based routing, please refer below files
http://cpr-ingress-2036109007.us-west-2.elb.amazonaws.com/de/  
http://cpr-ingress-2036109007.us-west-2.elb.amazonaws.com/fr/  
http://cpr-ingress-2036109007.us-west-2.elb.amazonaws.com/es/
 
