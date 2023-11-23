# Web Deployment Script
This Bash script is designed to streamline the setup process for a web project on an Nginx server. 
It supports Debian-based systems (such as Ubuntu,Debian) and Red Hat-based systems (such as Fedora and CentOS).

## Features

- **Installation and Configuration:**
  - Installs and configures the Nginx web server if it is not installed already.
  - Sets up a new site with customizable server name.

- **Source Code Deployment:**
  - Pulls the source code from a specified GitHub repository.
  - Copies the files and folders to the designated site directory.

- **System Update:**
  - Updates the system package information based on the detected Linux distribution.

- **Logging and Error Handling:**
  - Redirects standard output and error to `/dev/null` during system updates.
  - Logs errors to a file (`log_error.txt`) for reference.

## Prerequisites

- The script is designed for Linux servers, supporting Debian-based and Red Hat-based distributions.
- Ensure you have appropriate permissions to run system commands using `sudo`.
- Provide a valid GitHub repository URL for deploying the web application.

## Usage

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/prabinkc2046/NginxAutomator.git
  ```
Navigate to the Script Directory:

```bash
cd NginxAutomator
```

```bash
sudo ./deploy_it.sh <site_name> <github_repo> <source_code_dir_name> <server_name_or_ip>
```
Replace placeholders (<...>) with actual values:

site_name: Name of the site to be created (e.g., mywebsite).
github_repo: GitHub repository URL containing the source code.
source_code_dir_name: Name of the directory containing the source code.
server_name_or_ip: Domain name or IP address for the server.

Example
```bash
sudo ./deploy_it.sh mywebsite https://github.com/prabinkc2046/web.git code example.com
```

This example installs and configures Nginx, creates a site named mywebsite, and deploys the code from the specified GitHub repository.

Author: Prabin K C
Contact: pkmiracle36@gmail.com
LinkedIn: https://www.linkedin.com/in/prabin-kc/
