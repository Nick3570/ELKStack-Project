# ELKStack-Project
Used to deploy and configure ELK Stack to a network
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![image](https://user-images.githubusercontent.com/89492982/145691200-976330c3-b620-4291-b431-19eea4920e72.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the yml file may be used to install only certain pieces of it, such as Filebeat.

Filebeat yml:
https://github.com/Nick3570/ELKStack-Project/blob/7bb09a98bf5ae25143c57dd835cb3b2a22672358/filebeat.yml

Metricbeat yml:
https://github.com/Nick3570/ELKStack-Project/blob/7bb09a98bf5ae25143c57dd835cb3b2a22672358/metricbeat.yml

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting congestion to the network.

Load balancers protect the availability to a network by distributing traffic across multiple servers to reduce load. The advantage of a Jump Box is being able to maintain configuration files for an entire network and be able to distribute them all easily while also being able to have a way to connect to machines on a network that don't have a public IP address.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the network and system logs.

Filebeat watches for changes to system logs.
Metricbeat records statistics and metrics for services running on the server.

The configuration details of each machine may be found below.


| Name                | Function        | IP Address (Private/Public) | Operating System |
|---------------------|-----------------|-----------------------------|------------------|
| JumpBox Provisioner | Gateway         | 10.0.0.4/20.115.14.30       | Linux            |
| Web1                | Web Server      | 10.0.0.5                    | Linux            |
| Web2                | Web Server      | 10.0.0.6                    | Linux            |
| Web3                | Web Server      | 10.0.0.7                    | Linux            |
| Load Balancer       | Load Balancer   | 20.121.7.62                 |                  |
| ElkStack            | ELKStack Server | 10.1.0.4/40.83.132.151      | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box machine and the ELKStack machine can accept connections from the Internet. Access to these machines is only allowed from the following IP addresses:
- 32.210.210.56

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
10.0.0.5
10.0.0.6
10.0.0.7

We have installed the following Beats on these machines:
filebeat and metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
