# Ansible Playbook

This is an example of designing a simple ansible playbook for setting up a web server inan EC2.

## Prerequesties
As soon as you have Python installed, run the following command to install ansible 

`pip install --user ansible`

## Usage

1. You should have a key-pair created in your AWS Console. Follow [these instructions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair) to generate your key pair and save copy to your computer under `udacity.pem`

2. Create a new EC2 instance in your AWS account. Assign the `udacity` key pair to it and open up port 3000 for incomming traffic to be able to use the web server.

3. Put the IP address of your EC2 instance (hostname) into the inventory file.

4. Run your playbook using the following command
 
    `ansible-playbook main.yml -i inventory --private-key /path/to/udacity.pem`

5. Navigate to the hostname:3000 to verify your server working :)