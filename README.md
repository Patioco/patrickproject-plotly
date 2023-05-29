# deploy-to-eks-using-github-actions
1. Create an EKS Cluster in VS Code using this command:

eksctl create cluster --name patrickproject --region us-east-1 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2

2. Then create and initialize git in the project folder. Then create .github subfolder and then create workflow subfolder inside .github subfolder 
3. Create a file with .yml extension and write the workflow code
4. Create a github repository to push the project folder to. 
5. In the settings section of the github repo, create secrets to input your cloud account (AWS) credentials info
        Go to settings of repo
        click on secrets and variables
6. Create a container registry in AWS and link to workflow to automatically push your image built by Dockerfile to AWS
7. Configure and deploy the built container to EKS and expose app to LoadBalancer service
8. Test application by getting the dns name and going to a web browser

9. Clean up cluster by running 'eksctl delete cluster --name patrickproject'
