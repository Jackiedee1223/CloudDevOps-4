# Continuous Delivery of on AWS Cloud
<h2>Scenario</h2>
<p>
In our Cloud DevOps Project, we address the challenges associated with the traditional software development lifecycle, where product development teams often grapple with manual and time-consuming processes. The focus is on Continuous Delivery (CD) as a practice to streamline the deployment and testing phases, leveraging the capabilities of AWS Cloud to propel the development pipeline into an agile and efficient paradigm. In a typical product development setting, developers frequently contribute code changes that necessitate Build & Test cycles. The deployment process, traditionally handled by Operations teams, often becomes a bottleneck. Manual deployment is time-consuming, and the lack of Ops knowledge among developers and testers creates dependencies on dedicated Ops professionals. The need for constant CI/CD server maintenance adds to operational overhead.

In the Agile Software Development Life Cycle (SDLC), frequent code changes demand a faster and more efficient deployment mechanism. The reliance on manual deployment processes results in prolonged turnaround times and an increased need for operational expertise. The scenario often requires organizations to hire Ops professionals or outsource these tasks, leading to significant dependencies on Ops teams and a burden on CI/CD server maintenance. To address these challenges, our solution involves embracing Platform as a Service (PaaS) and Software as a Service (SaaS) cloud services, creating disposable environments, and automating the entire CI/CD process. The goal is to execute the BUILD, TEST, Deploy, and TEST again for every code commit. By implementing CD practices, we aim to achieve short Mean Time to Recovery (MTTR), agility, fault isolation, and minimal operational interventions.

In our pursuit of an optimal Continuous Delivery pipeline, we leverage a suite of AWS services catering to each phase of the CD pipeline. CodeCommit, CodeArtifact, CodeBuild, CodeDeploy, and CodePipeline form the backbone of our automated deployment and testing process. Additionally, SonarCloud and Checkstyle contribute to code analysis and quality checks, ensuring a high standard of software development. Our objectives include minimizing or eliminating operational overhead, achieving a short MTTR, enabling a fast turnaround on feature changes, and minimizing disruptions in the development lifecycle.

By transitioning to Continuous Delivery on the AWS Cloud, our project seeks to revolutionize the development pipeline. Through the adoption of cloud-native practices and the integration of powerful AWS services, we aim to create an environment where software changes are swiftly and reliably delivered, fostering a culture of agility, efficiency, and minimal disruption.
</p>

<h2>Architecture of AWS Services</h2>
 <img src="https://github.com/Jackiedee1223/image-repos/blob/main/CloudDevOps-4.png">

<h2>Flow of Execution</h2>

1.	Create Key pair for Beanstalk instance login: Generate a key pair that will be used for secure login to Elastic Beanstalk instance.
2. Create Security Group for Amazon ElastiCache, RDS, and ActiveMQ: Define security groups to control inbound and outbound traffic for ElastiCache, RDS, and ActiveMQ instances.	 
3.	Create RDS, Amazon ElastiCache, and Amazon ActiveMQ: Set up relational database (RDS), caching with ElastiCache, and the message broker with ActiveMQ.
4.	Create Elastic Beanstalk Environment: Deploy and manage the application in an Elastic Beanstalk environment, allowing automatic scaling and easy application management.
5. Update SG of backend to allow traffic from Bean SG: Adjust security group rules to permit traffic from Elastic Beanstalk security group to the backend services.	
6.	Update SG of backend to allow internal traffic: Configure security groups to enable internal communication between components.
7.	Launch EC2 instance for DB initializing: Start an EC2 instance dedicated to initializing and configuring RDS database.
8. Login to the instance and initialize RDS DB: Access the EC2 instance to execute the necessary scripts or commands to initialize RDS database.	
9.	Change health check on Beanstalk to login: Adjust the health check settings on Elastic Beanstalk to ensure it checks the login status or relevant indicators.
10.	Add 443 https Listener to ELB: Enhance security by configuring a secure HTTPS listener on Elastic Load Balancer (ELB).
11. Build Artifact with Backend Information: Compile an artifact containing the necessary information for the backend services.
12. Deploy Artifact to Beanstalk: Use Elastic Beanstalk to deploy the compiled artifact, making the application available.
13. Create CDN with SSL Cert: Establish a Content Delivery Network (CDN) and configure it with an SSL certificate for enhanced performance and security.
14. Update Entry in GoDaddy DNS Zones: Update the DNS settings in GoDaddy account to point to the newly created CDN and ensure proper domain resolution.
15. Test the URL: Conduct thorough testing to verify that the application is accessible and functioning correctly through the updated URL.




<h2>Validation & Summarization</h2>
<h4>Security Group & Key Pairs</h4>
<h4>EC2 Instances</h4>
<h4>Build and Deploy Artifacts</h4>
<h4>Load Balancer & DNS</h4>
<h4>Auto Scaling Group</h4>













<h2>Reference</h2>
<p>Learning from <b>GURUTECH NETWORKS</b> </p>
