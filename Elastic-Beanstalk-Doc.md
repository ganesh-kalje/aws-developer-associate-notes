# Elastic Beanstalk
- AWS Elastic Beanstalk is a Platform as a Service (PaaS) offering from AWS that simplifies the process of deploying, managing, and scaling web applications and services.
- You can deploy applications written in Java, .NET, Node.js, Python, PHP, Ruby, Go, Docker, Static files (HTML/CSS/JS).
- AWS Elastic Beanstalk itself is free, but you pay for the AWS resources it provisions to run your application.
- resources created or configured via .ebextensions are tied to the Elastic Beanstalk environment, and they are deleted when the environment is terminated.
- Under the hood, AWS Elastic Beanstalk uses AWS CloudFormation to provision and manage the infrastructure for your application.
-  a lifecycle policy refers to the rules that manage application versions stored in Amazon S3. These policies help you automatically delete old versions to reduce storage costs and keep your environment clean.

## Elastic Beanstalk automates:
- Provisioning of infrastructure (like EC2, Load Balancers, Auto Scaling)
- Deployment of your application code
- Monitoring and logging
- Scaling based on traffic
- Health checks and environment management

## core components that make up an AWS Elastic Beanstalk application
- Application: The top-level container for your project.Can have multiple versions and environments. example : mywebapplication
- Application Version: A specific build or release of your application.Uploaded as a ZIP or WAR file in S3, You can deploy different versions to different environments.
- Environment: A collection of AWS resources (EC2, ELB, etc.) running a specific version of your app.
    - Web Server Environment (for HTTP/S apps)
    - Worker Environment (for background jobs via SQS)
- Environment Configuration: Defines settings for the environment: Instance type, Scaling policies, Environment variables, Platform version, Load balancer settings. Can be saved as a configuration template for reuse.
- Configuration Template: A reusable blueprint of environment settings.Useful for creating consistent environments across stages (dev, test, prod).
- Platform: You can choose a managed platform or a custom platform.
- Saved Configurations (.ebextensions): YAML or JSON files placed in your app source bundle. Used to customize environment setup: Install packages, Configure software, Set permissions, Run scripts. Example: .ebextensions/myconfig.config. In AWS Elastic Beanstalk, almost all configuration options you set via the Management Console UI — such as environment variables, software settings, instance types, scaling policies, and more — can be defined as code using configuration files placed in the .ebextensions/ directory of your application source bundle.
- Logs & Monitoring
- Deployment Methods
  - All at Once: Deploys the new version to all instances simultaneously. Fast but causes downtime.
  - Rolling: Deploys to a batch of instances at a time.Minimizes downtime.
  - Rolling with Additional Batch: Adds a temporary batch of instances during deployment.Ensures full capacity is maintained.
  - Immutable: Launches a new set of instances with the new version.Swaps them in only if healthy.
  - Blue/Green Deployment: Create a clone of the environment (green). Deploy to green, test, then swap CNAME with blue (production). Zero downtime and rollback-friendly.
 



  

