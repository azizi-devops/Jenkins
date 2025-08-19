# Prerequisites
###
- JDK 17 or 21
- Maven 3.9
- MySQL 8
####
# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch
# Database
Here,we used Mysql DB 
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql

#####################################################################################################################################################

# 🚀 DevOps CI/CD Pipeline on AWS

This project outlines a comprehensive CI/CD pipeline using **AWS**, **Jenkins**, **Nexus**, and **SonarQube** to automate build, test, and deployment processes.

---

## 📸 Jenkins Dashboard

![Jenkins Dashboard](images/jenkins-dashboard.png)

---

## 🛠️ AWS Setup

- **Login to AWS Console**
- **Create Key Pair** for EC2 authentication
- **Configure Security Groups** for Jenkins, Nexus, and SonarQube
- **Launch EC2 Instances**:
  - Jenkins: Ubuntu, t2.small, 15GB
  - Nexus: Amazon Linux 2023, t2.medium
  - SonarQube: Ubuntu, t2.medium

---

## ⚙️ Jenkins Configuration

- Install plugins:
  - Maven Integration
  - GitHub Integration
  - Nexus Artifact Uploader
  - SonarQube Scanner
  - Slack Notification
  - Build Timestamp
- Access Jenkins on port `8080`

---

## 📦 Nexus Repository Setup

- Access Nexus on port `8081`
- Create repositories:
  1. `vprofile-release` (hosted)
  2. `vprofile-snapshot` (hosted)
  3. `vpro-maven-central` (proxy)
  4. `vprofile-group` (group)

---

## 🔍 SonarQube Integration

- Launch and configure SonarQube
- Integrate with Jenkins for code quality analysis

---

## 🧬 GitHub Integration

- Create GitHub repo
- Generate SSH key and configure `~/.ssh/config`
- Clone using custom host alias:
  ```bash
  git clone git@github.com-X:azizi-devops/vprofile-project.git



