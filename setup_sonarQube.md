# Sonarqube Setup

SonarQube is an open-source static testing analysis software, it is used by developers to manage source code quality and consistency

## Installation steps

1. Download SonarQube [latest verions](https://www.sonarqube.org/downloads/)
   ```sh
   cd /opt
   wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
   ```
2. extract packages

   ```sh
   unzip /opt/sonarqube-9.9.8.100196.zip
   ```

3. Change ownership to the user and Switch to Linux binaries directory to start service
   ```bash
   chown -R <sonar_user>:<sonar_user_group> /opt/sonarqube-9.9.8.100196
   cd /opt/sonarqube-x.x/bin/linux-x86-64
   ./sonar.sh start
   ```
4. Connect to the SonarQube server through the browser. It uses port 9000.  
   `Note`: Port should be opened in the Security group

   ```bash
   http://<Public-IP>:9000
   ```

   ## 🧹 CleanUp

   1. Stop SonarQube server

   ```sh
   cd /opt/sonarqube-9.9.8.100196/bin/linux-x86-64
   ./sonar.sh stop
   ```

   2. Terminate EC2 instance incase if you setup only for this lab.
