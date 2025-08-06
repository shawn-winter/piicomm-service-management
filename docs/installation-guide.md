# PiiComm Service Management System Installation Guide

Welcome to the installation guide for the PiiComm Service Management System. This document provides a comprehensive step-by-step process to install and configure the system. Whether you are a technical or non-technical user, this guide is designed to be easy to follow.

## Table of Contents

1. [System Requirements](#system-requirements)
2. [Prerequisites and Dependencies](#prerequisites-and-dependencies)
3. [Step-by-step Installation Process](#step-by-step-installation-process)
4. [Configuration Options](#configuration-options)
5. [Environment Setup](#environment-setup)
6. [Database Setup and Migration](#database-setup-and-migration)
7. [Troubleshooting Common Installation Issues](#troubleshooting-common-installation-issues)
8. [Verification Steps](#verification-steps)

## System Requirements

Before installing the PiiComm Service Management System, ensure your system meets the following requirements:

- **Operating System**: Windows 10 or later, macOS 10.14 or later, Ubuntu 18.04 LTS or later
- **Processor**: Intel Core i5 or equivalent
- **Memory**: 8 GB RAM minimum
- **Hard Disk**: 10 GB of available space
- **Network**: Broadband Internet connection

## Prerequisites and Dependencies

Ensure that the following software and services are installed and running on your system:

- **Java Development Kit (JDK)**: Version 11 or later
- **Apache Tomcat**: Version 9.0 or later
- **MySQL Server**: Version 5.7 or later
- **Node.js**: Version 14.x or later
- **npm**: Version 6.x or later (comes with Node.js)
- **Git**: Latest version

## Step-by-step Installation Process

Follow these steps to install the PiiComm Service Management System:

### 1. Download the Software

- Visit the official PiiComm website or access the secured download link provided by your system administrator.
- Download the latest version of the PiiComm Service Management System package.

### 2. Install Java Development Kit

- Download JDK from the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
- Follow the installation instructions for your operating system.

### 3. Install Apache Tomcat

- Download Apache Tomcat from the [official website](https://tomcat.apache.org/).
- Unzip the downloaded file and place it in your desired directory.
- Set the `CATALINA_HOME` environment variable to point to the Tomcat installation directory.

### 4. Setup MySQL Database

- Install MySQL Server from the [MySQL website](https://dev.mysql.com/downloads/mysql/).
- Create a database for PiiComm using the command line or MySQL Workbench.
  ```sql
  CREATE DATABASE piicomm_db;
  ```

### 5. Install Node.js and npm

- Download and install Node.js from the [official website](https://nodejs.org/).
- Verify the installation by running `node -v` and `npm -v` in the command line.

### 6. Clone the Repository

- Open a terminal or command prompt.
- Clone the repository:
  ```bash
  git clone https://github.com/piicomm/piicomm-service-management.git
  ```

### 7. Install Dependencies

- Navigate to the project directory:
  ```bash
  cd piicomm-service-management
  ```
- Install the necessary Node.js packages:
  ```bash
  npm install
  ```

## Configuration Options

- **Database Configuration**: Modify the `config/database.js` file to include your MySQL database credentials.
- **Port Configuration**: Adjust the port settings in `config/server.js` if the default port is in use.

## Environment Setup

1. **Set Environment Variables**:
   - `DATABASE_URL`: URL of the MySQL database.
   - `NODE_ENV`: Set to `production` or `development`.

2. **Configure Apache Tomcat**:
   - Deploy the WAR file by placing it in the `webapps` directory of your Tomcat installation.

## Database Setup and Migration

- Run database migrations using the provided migration scripts:
  ```bash
  npm run migrate
  ```

## Troubleshooting Common Installation Issues

- **Java Not Found**: Ensure the JDK bin directory is added to your system's PATH variable.
- **Port Conflicts**: Check if the default ports (8080 for Tomcat, 3306 for MySQL) are in use by other applications.
- **Database Connection Errors**: Verify the database URL, username, and password in your configuration file.

## Verification Steps

1. **Start the Application**:
   - Run the application using the command:
     ```bash
     npm start
     ```

2. **Access the Application**:
   - Open a web browser and navigate to `http://localhost:8080`.
   - Log in using the default credentials provided by your system administrator.

3. **Check Logs**:
   - Monitor the application logs for any errors or warnings.

This comprehensive guide should help you successfully install and configure the PiiComm Service Management System. If you encounter any issues not covered in this guide, please contact the PiiComm support team for further assistance.