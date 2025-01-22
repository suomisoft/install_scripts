# socialwebcloud_install_scripts
This guide will walk you through setting up an Ubuntu virtual server on linux web hosting, accessing it, installing Ansible, cloning a repository, and running an Ansible playbook.

## Prerequisites

- A linux web hosting account
- A registered domain name (optional but recommended)

## Steps

### 1. Create an Ubuntu Virtual Server on linux web hosting

1. **Log in to linux web hosting:**
   - Visit your linux web hosting provider and log in to your account.

2. **Create a New linux server:**
   - Select **Ubuntu** as the distribution and choose the version you prefer.
   - Choose a plan that suits your needs.
   - Select a data center region close to your location for better performance.
   - (Optional) Configure additional settings such as backups or VLAN if needed.

3. **Assign a Domain Name (Optional):**
   - If you have a registered domain name, configure DNS settings to point to your linux web hosting server’s IP address.
   - Manage DNS settings in the linux web hosting dashboard or through your domain registrar’s website.

4. **Complete the linux web hosting setup:**
   - Note the public IP address assigned to your linux server.

### 2. Get Access to the Server

#### Using SSH

1. **Open an SSH Client:**
   - On Windows, use [PuTTY](https://www.putty.org). On macOS or Linux, use the terminal.

2. **Connect to Your linux web server:**
   - Open PuTTY (Windows) or your terminal (macOS/Linux).
   - Enter the IP address of your linux web server.
   - Use the default SSH port (22) for the connection.

3. **Login:**
   - Enter the username (`root` or the username you specified during setup).
   - Enter the password created during the linux web hosting setup process.

   **Note:** For enhanced security, consider setting up SSH keys and disabling password authentication.

### 3. Install Ansible on the Virtual Server

1. **Update the Package Index:**
   - Run the following command:
     ```bash
     sudo apt update
     ```

2. **Install Ansible:**
   - Follow the [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) for detailed instructions.
   - Typically, you can install Ansible with:
     ```bash
     sudo apt install ansible
     ```

3. **Verify Installation:**
   - Check the installation by running:
     ```bash
     ansible --version
     ```
   - You should see the version information for Ansible.

### 4. Clone the Repository

1. **Clone the Repository:**
   - Use the following command to clone the repository:
     ```bash
     git clone https://github.com/suomisoft/install_scripts/
     ```

2. **Navigate to the Repository Directory:**
   - Change to the directory of the cloned repository:
     ```bash
     cd install_scripts
     ```

### 5. Run the Ansible Playbook

1. **Execute the Playbook:**
   - Run the following command to start the Ansible playbook:
     ```bash
     ansible-playbook social_web_cloud.yml
     ```

2. **Follow the Prompts:**
   - Answer any prompts provided by the playbook to complete the configuration.
