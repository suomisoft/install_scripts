# socialwebcloud_install_scripts
Server Setup and Ansible Configuration Guide
This guide will help you set up an Ubuntu virtual server on Linode, access it, install Ansible, clone a repository, and run an Ansible playbook.

Prerequisites
A Linode account
A registered domain name (optional but recommended)
Steps
1. Create an Ubuntu Virtual Server on Linode
Log in to Linode:

Visit Linode.com and log in to your account.
Create a New Linode:

Click the “Create Linode” button.
Select Ubuntu as the distribution and choose your preferred version.
Choose a plan that meets your needs.
Pick a data center region close to your location for better performance.
(Optional) Configure additional settings such as backups or VLAN if required.
Assign a Domain Name (Optional):

If you have a registered domain, configure the DNS settings to point to your Linode server’s IP address.
You can manage DNS settings in the Linode dashboard or through your domain registrar’s website.
Complete the Linode Setup:

Click “Create Linode” to finalize the setup.
Note the public IP address assigned to your Linode.
2. Get Access to the Server
Using SSH
Open an SSH Client:

On Windows, use PuTTY. On macOS or Linux, use the terminal.
Connect to Your Linode:

Open PuTTY (Windows) or your terminal (macOS/Linux).
Enter the IP address of your Linode server.
Use the default SSH port (22) for the connection.
Login:

Enter the username (root or the username you created during setup).
Enter the password you set during the Linode setup process.
Note: For enhanced security, consider using SSH keys and disabling password authentication.

3. Install Ansible on the Virtual Server
Update the Package Index:

Run the following command:
bash
Copy code
sudo apt update
Install Ansible:

Follow the Ansible Installation Guide for detailed instructions.
Typically, you can install Ansible with:
bash
Copy code
sudo apt install ansible
Verify Installation:

Check the installation by running:
bash
Copy code
ansible --version
You should see version information for Ansible.
4. Clone the Repository
Clone the Repository:

Use the following command to clone the repository:
bash
Copy code
git clone https://github.com/suomisoft/install_scripts/
Navigate to the Repository Directory:

Change to the directory of the cloned repository:
bash
Copy code
cd install_scripts
5. Run the Ansible Playbook
Execute the Playbook:

Run the following command to start the Ansible playbook:
bash
Copy code
ansible-playbook social_web_cloud.yml
Follow the Prompts:

Answer any prompts provided by the playbook to complete the configuration.

