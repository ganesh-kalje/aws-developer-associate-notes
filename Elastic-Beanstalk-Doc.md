# Elastic Beanstalk
- AWS Elastic Beanstalk is a Platform as a Service (PaaS) offering from AWS that simplifies the process of deploying, managing, and scaling web applications and services.
- You can deploy applications written in Java, .NET, Node.js, Python, PHP, Ruby, Go, Docker, Static files (HTML/CSS/JS).
- AWS Elastic Beanstalk itself is free, but you pay for the AWS resources it provisions to run your application.

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
- Saved Configurations (.ebextensions): YAML or JSON files placed in your app source bundle. Used to customize environment setup: Install packages, Configure software, Set permissions, Run scripts. Example: .ebextensions/myconfig.config
- Logs & Monitoring
- Deployment Methods
  

