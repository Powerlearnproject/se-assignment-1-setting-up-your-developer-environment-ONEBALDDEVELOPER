# Comprehensive Developer Environment Setup Documentation

## TABLE OF CONTENTS

1. Windows 11 Installation
2. IDE Installation
3. Version Control System Setup
4. Programming Languages and Runtimes Installation
5. Package Managers Installation
6. Database Installlation and Configuration
7. Development Environments and Virtualization Setup
8. Code Editor Extensions Installation

### Introduction

This document provides a comprehensive guide to setting up a developer environment on a Windows 11 machine. It covers the installation, configuration and troubleshooting common issues encountered.

### 1. Select Your Operating System (OS)

**Preferred OS:** Windows 11

**Steps to Install Windows 11:**

1. **Download the Media Creation Tool:**
   - Visit the [Windows 11 download page](https://www.microsoft.com/software-download/windows11).
   - Download the Media Creation Tool.

2. **Create a Bootable USB Drive or ISO File:**
   - Run the Media Creation Tool.
   - Follow the prompts to create a bootable USB drive (minimum 8GB) or ISO file.

3. **Install Windows 11:**
   - Insert the USB drive into the computer.
   - Restart the computer.
   - Access the boot menu (usually by continuously hitting F2, F12, or Del).
   - Select the USB drive as the boot device and press Enter.
   - Follow the installation prompts to complete the installation of Windows 11.

4. **Update Windows:**
   - Run Windows Update to update drivers and other supporting software.

### 2. Install a Text Editor or Integrated Development Environment (IDE)

**Preferred IDE:** Visual Studio Code (VS Code)

**Steps to Install Visual Studio Code:**

1. **Download the VS Code Installer:**
   - Visit the [VS Code download page](https://code.visualstudio.com/Download).
   - Download the installer for your operating system.

2. **Install VS Code:**
   - Run the installer.
   - Follow the prompts to install VS Code.
   - Select the installation path for the files.
   - Once installed, launch VS Code.
   - Explore its features and extensions.

### 3. Set Up Version Control System

**Preferred Version Control System:** Git with GitHub

**Steps to Install and Configure Git:**

1. **Download the Git Installer:**
   - Visit the [Git download page](https://git-scm.com/downloads).
   - Download the installer for your operating system.

2. **Install Git:**
   - Run the installer.
   - Follow the prompts to install Git.

3. **Configure Git:**
   - Open the Git Bash terminal.
   - Set up your Git configuration:

     ```sh
     git config --global user.name "Your Name"
     git config --global user.email "your.email@example.com"
     ```

4. **Create a GitHub Account and Repository:**
   - Visit [GitHub](https://github.com) and create an account.
   - Create a new repository for your project.

5. **Initialize a Git Repository:**

   ```sh
   git init
   ```

6. **Make Your First Commit:**

   ```sh
   vim README.md to open the vim edit environment
   Add content to README.md using 'I' to insert content, then save and exit using 'W', 'Q'
   cat README.md to check the contents of README.md file
   git add README.md
   git commit -m "First commit"
   git branch -M main
   git remote add origin 'link to github repository'
   git push -u origin main
   ```

7. **Link Local Repository to GitHub Repository:**

   ```sh
   git remote add origin https://github.com/yourusername/yourrepository.git
   ```

8. **Push Changes to GitHub:**

   ```sh
   git push -u origin master
   ```

### 4. Install Necessary Programming Languages and Runtimes

**Preferred Programming Language:** Python

**Steps to Install Python:**

1. **Download the Python Installer:**
   - Visit the [Python download page](https://www.python.org/downloads/).
   - Download the installer for your operating system.

2. **Install Python:**
   - Run the installer.
   - Follow the prompts to install Python.
   - Select the option to add Python to your PATH.

3. **Verify the Python Installation:**
   - Open a terminal or command prompt.
   - Run the command:

     ```sh
     python --version
     ```

4. **Install Necessary Packages and Libraries:**
   - Use pip to install required packages:

     ```sh
     pip install numpy
     ```

5. **Install Necessary Tools:**

   ```sh
   pip install build
   ```

### 5. Install Package Managers

**Preferred Package Manager:** pip (Python)

**Steps to Verify and Use pip:**

1. **Verify pip Installation:**
   - Pip is installed by default with Python.
   - Run the command:

     ```sh
     pip --version
     ```

2. **Install Necessary Packages:**

   ```sh
   pip install numpy
   ```

3. **Install Necessary Tools:**

   ```sh
   pip install build
   ```

4. **Install Other Package Managers if Required:**
   - For example, install npm (Node.js):

     ```sh
     npm install -g npm
     ```

5. **Install Packages Using npm:**

   ```sh
   npm install package-name
   ```

### 6. Configure a Database (MySQL)

**Preferred Database:** MySQL

**Steps to Install and Configure MySQL:**

1. **Download the MySQL Installer:**
   - Visit the [MySQL download page](https://dev.mysql.com/downloads/windows/installer/5.7.html).
   - Download the installer.

2. **Install MySQL:**
   - Run the installer.
   - Follow the prompts to install MySQL.
   - Select the option to install the MySQL Server and other necessary components.
   - Set a root password during installation.

3. **Verify MySQL Installation:**
   - Open the MySQL Command-Line Tool.
   - Run the command:

     ```sh
     mysql --version
     ```

4. **Create a New Database and User:**

   ```sql
   CREATE DATABASE database_name;
   CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
   GRANT ALL PRIVILEGES ON database_name.* TO 'username'@'localhost';
   ```

5. **Configure Project to Connect to MySQL:**
   - Install the MySQL connector library:

     ```sh
     pip install mysql-connector-python
     ```

6. **Establish Connection in Code:**

   ```python
   import mysql.connector

   conn = mysql.connector.connect(
       host="localhost",
       user="username",
       password="password",
       database="database_name"
   )
   ```

7. **Perform Database Operations and Close Connection:**

   ```python
   cursor = conn.cursor()
   cursor.execute("SELECT * FROM table_name")
   conn.close()
   ```

### 7. Set Up Development Environments and Virtualization (Optional)

**Preferred Tool:** Docker

**Steps to Set Up Docker:**

1. **Install Docker:**
   - Visit the [Docker download page](https://www.docker.com/products/docker-desktop).
   - Download and install Docker Desktop for your operating system.

2. **Pull Docker Image for Your Project:**

   ```sh
   docker pull python:3.9
   ```

3. **Create a Docker Container:**

   ```sh
   docker run -it python:3.9
   ```

4. **Install Dependencies in the Container:**

   ```sh
   pip install numpy
   ```

5. **Configure Project to Use Docker:**
   - Use Docker volumes to persist data:

     ```sh
     docker run -it -v /path/to/your/project:/app python:3.9
     ```

6. **Share Docker Container:**
   - Push Docker image to Docker Hub:

     ```sh
     docker tag your-image yourusername/yourrepository
     docker push yourusername/yourrepository
     ```

7. **Alternative to Docker:**
   - Install VirtualBox:
     - Visit the [VirtualBox download page](https://www.virtualbox.org/).
     - Download and install VirtualBox for your operating system.

### 8. Explore Extensions and Plugins

**Preferred IDE:** Visual Studio Code (VS Code)

**Steps to Explore Extensions and Plugins:**

1. **Open VS Code and Navigate to Extensions Panel:**
   - Click the Extensions icon in the left sidebar.

2. **Browse Extensions Marketplace:**
   - Discover available extensions, plugins, and add-ons for your project.

3. **Search for Specific Extensions:**
   - For example, search for Python, Java, or C++ extensions.

4. **Read Reviews and Ratings:**
   - Determine the best extensions for your project.

5. **Install Necessary Extensions:**
   - For example, install the Python Extension Pack, Java Extension Pack, or C++ Extension Pack.

6. **Configure Installed Extensions:**
   - Customize according to project requirements.

7. **Explore Other IDEs and Text Editors:**
   - For example, IntelliJ IDEA, Eclipse, or Sublime Text.

8. **Install Plugins for Version Control Systems:**
   - Integrate Git with your IDE or text editor.

### Troubleshooting Steps Encountered

- **Issue:** Unable to access boot menu during Windows 11 installation.
  - **Solution:** Research websites for supportivre documentation for the correct key to access the boot menu and follow the processes presented.

- **Issue:** Git not recognized after installation.
  - **Solution:** Ensure the Git binary(bin) is added to the system PATH during installation.

- **Issue:** Python not recognized after installation.
  - **Solution:** Verify that the "Add Python bin to PATH" option was selected during installation. If not, manually add Python to the system PATH.

- **Issue:** MySQL service not starting.
  - **Solution:** Check the MySQL configuration file for errors. Ensure there are no conflicting services using the same port.

### NOTE!!!: It is recommended to visit YouTube, Stackoverflow or prompt GPT for more support and detailed explanation
