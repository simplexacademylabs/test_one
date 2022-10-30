# Steps

# Requirements installation
eksctl,
kubectl,
awscli,
helm,

You need to configure awscli with your own access key and secret key (https://docs.aws.amazon.com/cli/latest/userguide/getting-started-quickstart.html)

# AWS EKS Setup
Setup kubectl
a. Download kubectl version 1.20
b. Grant execution permissions to kubectl executable
c. Move kubectl onto /usr/local/bin
d. Test that your kubectl installation was successful

curl -o kubectl https://amazon-eks.s3.us-east-1.amazonaws.com/1.19.6/2021-01-05/bin/linux/amd64/kubectl
chmod +x ./kubectl
mv ./kubectl /usr/local/bin 
kubectl version --short --client

# Setup eksctl
a. Download and extract the latest release
b. Move the extracted binary to /usr/local/bin
c. Test that your eksclt installation was successful

curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv /tmp/eksctl /usr/local/bin
eksctl version

# Setup AWS CLI
#curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
#curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

# Setup helm

#curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
#chmod 700 get_helm.sh
#./get_helm.sh

# configure awscli with your own access key and secret key

Access key ID  AKIAWRMZT4EKXAB6ZMJB

Secret access key   xTNgy8+sPDKypR7rm9SBfMrFF9PnSdXJebBtOCDc

aws configure (provide the credentials)

# Create EKS Cluster

#eksctl create cluster --name test-cluster --region us-east-1

Wait for the command to finish









