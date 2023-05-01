# Azure Devops for Testers Course

I would like to express my sincere gratitude to [Rahul Shetty](https://www.udemy.com/user/rahul445/) for their excellent
instruction and for sharing their knowledge during [this](https://www.udemy.com/course/azure-devops-fundamental/) course.

## What is Azure Devops?

* Azure DevOps Server is a Microsoft product that provides version control, reporting, requirements mangement, project 
management, automated builds, testing and release management capabilities.
* It covers the entire applications lifecycle, and enables DevOps capabilities.

## Deployment Basics - What are CI/CD Pipelines?

### What are Application Servers?
An application/Web server is a server specifically designed to run applications (or) it is server to host applications.

It handles Http request and send response calls over Http protocol.

### What are Hosted Servers?
Hosted Servers are nothing but physical machines where application/Web/Databases servers are hosted (e.g. xxx.xxx.xxx.xx:8080)

Application server can start at any port in Hosted Server and can be accessed through HostedServerIpAddress: portNumber

#### Apache TomCat Example

1. Go to [Apache TomCat Official Page](https://tomcat.apache.org/) and download the version that fits your operating system.
2. Once you have extracted the zip, open de `bin` folder and click on `startup.bat`
> **Note**
> If you get an error because port 8080 is in use, please follow [this](https://stackoverflow.com/questions/39632667/how-do-i-kill-the-process-currently-using-a-port-on-localhost-in-windows) tutorial to fix it.
3. Build your project and paste the `.war` generated into `webapps` folder.
  
  (e.g. Go to `D:\apache-tomcat-10.1.7-windows-x64\apache-tomcat-10.1.7\webapps` and put the file, for example `webapp.war`)

4. Open your browser and type in the URL: `localhost:8080/webapp`

### Continuos Integration (CI):
Continuos Integrations (CI) is the process of automating the build and testing of code every time a team member commits changes to version control.

### Continuos Delivery (CD):
Continuos Delivery (CD) is the process to build, test, configure and deploy from a build to a prodcution environment.

![image](https://user-images.githubusercontent.com/60171460/232179273-930f9958-a9c8-4b0f-b7c0-ad75be2b7250.png)

## Azure Pipelines

### Buidl Pipelines

These pipelines Jobs clone the code from assigned repositories and build the project based on instructions provided in yaml file.

Typically we use `Build Pipelines` to publish Artifacts of the project.

### Release Pipeline

These pipelines are generally used to deploy the build artifacts into agent machines.

### Create Release

This component help us to build end to end pipeline (connecting build and release pipelines) for CI/CD implementation
