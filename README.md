# AWS-EKS---2048-app

![image](https://github.com/anujatsamuel/AWS-EKS---2048-app/assets/138687534/bce9b8c7-aa34-49b5-b611-c64fc65405dd)

Prerequsites :

Install the AWS CLI:

Download and install the AWS CLI on your local machine. You can find installation instructions for various operating systems here.
Configuring AWS CLI Credentials:

Open a terminal or command prompt and run the following command:
aws configure
Enter the access key ID and secret access key of the IAM user you created earlier.
Choose a default region and output format for AWS CLI commands.

Install kubectl:

Install kubectl on your local machine. Instructions can be found here.
Configuring kubectl for EKS:

Once kubectl is installed, you need to configure it to work with your EKS cluster.
In the AWS Management Console, go to the EKS service and select your cluster.
Click on the "Config" button and follow the instructions to update your kubeconfig file. Alternatively, you can use the AWS CLI to update the kubeconfig file:
aws eks update-kubeconfig --name your-cluster-name
Verify the configuration by running a kubectl command against your EKS cluster:
kubectl get nodes

Install eksctl:

Well, unlike AWS CLI, eksctl is not available to install using the default Ubuntu’s base repositories, therefore, we need to download it from its GitHub repository. Here is the command to do so:

curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
Move the extracted binary to the /usr/local/bin directory using the following command:

sudo mv /tmp/eksctl /usr/local/bin
Step 3: Check Eksctl Version
After completing the installation, to confirm the eksctl tool is on our system, let’s use its command to check the version.

eksctl version



