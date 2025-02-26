# Git Demo Project

This is a demo project for learning the basics of Git version control and working with the LAMP stack for web deployment.

## Project Description

This repository is a simple demonstration of how Git can be used for version control. The steps taken in this project include initializing a Git repository, working with branches, and deploying a PHP application on a Linux server.

## Steps Completed

### Step 1: Install and Configure Git
- Installed Git on my system.
- Configured my Git username and email.
- Verified the installation by running `git --version`.

### Step 2: Work with a Git Repository
- Created a folder named `git-demo` and initialized Git inside it.
- Created a `README.md` file and added a description of the project.
- Added and committed the changes, then pushed the repository to GitHub.

### Step 3: Branching and Merging
- Created a new branch named `feature-branch`.
- Switched to the new branch and modified the `README.md` file (added more details).
- Added and committed the changes, then pushed the branch to GitHub.
- Merged `feature-branch` into the main branch.

## Deployment Steps for PHP Web Application on a Linux Server

To deploy a PHP web application on a Linux server, follow these steps:

1. **Install Apache Web Server**:
   - Run the following command to install Apache:
     ```bash
     sudo apt update
     sudo apt install apache2
     ```

2. **Install PHP**:
   - Install PHP and necessary modules:
     ```bash
     sudo apt install php libapache2-mod-php php-mysql
     ```

3. **Install MySQL**:
   - Install MySQL server:
     ```bash
     sudo apt install mysql-server
     ```
   - Secure the MySQL installation:
     ```bash
     sudo mysql_secure_installation
     ```

4. **Configure Apache**:
   - Create a virtual host configuration file for your website:
     ```bash
     sudo nano /etc/apache2/sites-available/your-site.conf
     ```
     Example configuration:
     ```apache
     <VirtualHost *:80>
         ServerAdmin webmaster@localhost
         DocumentRoot /var/www/html/your-application
         ErrorLog ${APACHE_LOG_DIR}/error.log
         CustomLog ${APACHE_LOG_DIR}/access.log combined
     </VirtualHost>
     ```
   - Enable the site and reload Apache:
     ```bash
     sudo a2ensite your-site.conf
     sudo systemctl reload apache2
     ```

5. **Deploy Your Application**:
   - Upload your PHP application files to `/var/www/html/your-application` directory.
   - Ensure the correct file and directory permissions:
     ```bash
     sudo chown -R www-data:www-data /var/www/html/your-application
     sudo chmod -R 755 /var/www/html/your-application
     ```

6. **Test the Deployment**:
   - Visit `http://your-server-ip` in your web browser to check if the PHP application is running successfully.

## Benefits of CI/CD (Continuous Integration & Continuous Deployment)

CI/CD pipelines help automate and streamline the development and deployment process. Here are the benefits:

- **Faster Development**: By automating testing and deployment, developers can release new features or bug fixes more quickly.
- **Consistency**: CI/CD ensures that the deployment process is consistent, reducing human errors.
- **Quality Assurance**: Automated tests run every time code is committed, ensuring that bugs are caught early in the development process.
- **Reliability**: With automated deployments, you can deploy code more frequently and confidently, knowing that the process is standardized.
- **Rollback Capability**: CI/CD pipelines allow you to quickly rollback to previous versions if a deployment causes issues.

## Git Commands Used

Here are the main Git commands I used for this project:

- `git init` - Initialize a new Git repository.
- `git add .` - Add all files to staging.
- `git commit -m "Your commit message"` - Commit the changes.
- `git branch feature-branch` - Create a new branch.
- `git checkout feature-branch` - Switch to the new branch.
- `git push origin feature-branch` - Push the new branch to GitHub.
- `git merge feature-branch` - Merge `feature-branch` into `main`.



