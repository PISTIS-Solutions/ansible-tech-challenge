## Ansible-Tech-Challenge

Before running the Ansible playbooks, ensure the following prerequisites are met:
- Ansible is installed on the control node.
- Python is installed on the control node.
- boto/boto3 is installed on the control node.
- AWS CLI and credentials are configured on the control node.
- Necessary IAM permissions are granted for creating EC2 instances, modifying security groups, and accessing other AWS resources.

## Project Structure
The project structure includes the following files and directories:
- **site.yaml**: The main Ansible playbook that orchestrates the execution of other playbooks and roles.
- **roles/**: Directory containing Ansible roles for specific tasks such as creating security groups, launching EC2 instances, and deploying web servers.
  - **security-group.yaml**: Ansible playbook for creating AWS security groups.
  - **ec2-instance.yaml**: Ansible playbook for launching EC2 instances.
  - **webserver.yaml**: Ansible playbook for deploying the web server application.

## Execution Steps
Follow these steps to execute the Ansible project:

1. **Clone the Repository**: Clone the Ansible project repository to the control node.

   ```bash
   git clone <repository_url>
   ```

2. **Navigate to Project Directory**: Change directory to the root of the Ansible project.

   ```bash
   cd <project_directory>
   ```

3. **Update Variables**: Update variables in the main playbook (`site.yaml`) and role files (`roles`) as per the environment and requirements.

4. **Execute the Playbook**: Run the main playbook (`site.yaml`) using the `ansible-playbook` command.

   ```bash
   ansible-playbook -i inventory/dev playbook/site.yaml
   ```

5. **Monitor Execution**: Monitor the execution of the playbook for any errors or warnings. Ensure that all tasks complete successfully.

6. **Verify Deployment**: Verify that the EC2 instance is created, security groups are configured, and the web server application is deployed as expected.

By following the steps outlined in this documentation, you can automate the deployment of AWS resources and web server applications using Ansible playbooks and roles.
Feel free to reach out for any assistance or troubleshooting during the execution of the Ansible project.

---
This documentation provides a comprehensive guide for executing the Ansible project. Adjustments can be made based on specific project requirements and environment configurations.