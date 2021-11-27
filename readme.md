aws cloudformation create-stack --stack-name development --template-body file://cloudformation.yaml --profile example
aws cloudformation delete-stack --stack-name development --profile example

ansible jenkins -i ./inventory/ec2 -m ping

ansible-playbook -i ./inventory/ec2 ./playbooks/setup_jenkins.yaml


1. Create an KeyPair in AWS Console
2. Change example in cloudformation.yaml
3. Put your public key in cloudformation.yaml
4. Make sure you have access to ec2 from your local machine
5. Change IP in inventory/ec2