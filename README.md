# terraform-jenkins-eks

## Project Architecture

<img width="945" height="635" alt="image" src="https://github.com/user-attachments/assets/c9902588-f7a4-477a-9d93-5d8cd096f5c2" />

## Tools used 
  1. GitHub
  2. Jenkins
  3. Terraform
  4. Helm
  5. Amazon EKS

# Installation Steps
## Jenkins

### Download Jenkins:
Go to the official Jenkins website and download the latest stable Jenkins WAR (web application archive) file for your system.

### Open Command Prompt:
On a Windows laptop, open Command Prompt or PowerShell to run the installation commands.

### Start Jenkins:
Move to the folder where the Jenkins WAR file was downloaded. Then run the following command:

```bash
java -jar jenkins.war
```
This command launches Jenkins and it will start running on the default port 8080.

### Access Jenkins in Browser:
Open any web browser and enter the following address:

```bash
http://localhost:8080
```
When accessing Jenkins for the first time, the setup page will ask you to unlock Jenkins using an administrator password.

### Retrieve the Administrator Password:
The password is stored in a file on your system. Jenkins will display the exact path on the screen. Usually, it is located at:

```bash
C:\Users\<your-username>\.jenkins\secrets\initialAdminPassword
```
Open this file, copy the password, and paste it into the Jenkins setup page.

### Complete the Setup Process:
After unlocking Jenkins, the setup wizard will begin. You can choose to install the recommended plugins or manually select plugins according to your requirements. Once the plugins are installed, create an admin user account for Jenkins.

### Configure Jenkins:
After the installation is complete, you can start configuring Jenkins for your projects. This may include creating build jobs, installing additional plugins, and modifying system settings based on your development needs.

## Terraform

Installing Terraform on Windows

This guide explains how to install Terraform on a Windows laptop using the official Terraform release from HashiCorp.

### Prerequisites

Before installing Terraform, make sure your Windows system has internet access and that you have permission to install software.

### Download Terraform

Open your web browser.

Go to the official Terraform download page:
https://developer.hashicorp.com/terraform/downloads
Download the Windows (AMD64) ZIP file.

### Extract the Terraform File

Locate the downloaded ZIP file in your Downloads folder.  
Right-click the ZIP file and select Extract All.  
After extraction, you will see the terraform.exe file.  

### Move Terraform to a System Folder

To run Terraform from any command prompt location:

Create a folder such as:  
C:\terraform  
Move terraform.exe into this folder.  

### Add Terraform to the System PATH

Open Start Menu and search for Environment Variables.  
Click Edit the system environment variables.  
In the System Properties window, click Environment Variables.  
Under System Variables, find and select Path, then click Edit.  
Click New and add:  
C:\terraform  
Click OK to save the changes. 

### Verify the Installation

To confirm Terraform is installed correctly:

Open Command Prompt or PowerShell.

Run the following command:  
```bash
terraform -version
```
If Terraform is installed successfully, the terminal will display the Terraform version number.

## Installing Helm on Windows

This guide explains how to install Helm on a Windows laptop and verify that it is working correctly.

### Open Command Prompt or PowerShell

On a Windows system, open Command Prompt or PowerShell to run the required commands. You can find these by searching in the Start Menu.

### Download Helm

Open a web browser and visit the official Helm releases page:
https://github.com/helm/helm/releases

Download the latest Windows amd64 ZIP file.

### Extract the Helm File

Go to your Downloads folder where the ZIP file was saved.

Right-click the file and select Extract All.

Inside the extracted folder, locate the file named:

helm.exe
### Move Helm to a System Folder

To run Helm commands from any directory:

Create a folder such as:

```bash
C:\helm
```
Move helm.exe into this folder.

### Add Helm to the System PATH

Open the Start Menu and search for Environment Variables.  
Click Edit the system environment variables.  
Select Environment Variables.  
Under System Variables, select Path and click Edit.  

Click New and add:

C:\helm

Click OK to save the changes.

### Verify Helm Installation

To confirm Helm has been installed correctly:

Open Command Prompt or PowerShell.

Run the command:

```bash
helm version
```
If Helm is installed successfully, the terminal will display the Helm version information.

### Post-Installation Steps

### Connect Helm to Kubernetes:
Helm works with Kubernetes clusters. Make sure your Kubernetes cluster is configured and accessible through kubectl before using Helm.

### About Helm Initialization:
In earlier versions of Helm (Helm 2), the server-side component called Tiller had to be installed. However, starting from Helm 3, Tiller is no longer required, so no initialization step is needed.

### Configure Helm:
Once Helm is installed and your Kubernetes cluster is configured, you can begin using Helm to deploy and manage Kubernetes applications. For additional setup details, refer to the official Helm documentation.
