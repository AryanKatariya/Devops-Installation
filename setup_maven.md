# Install & configure Maven build tool on Jenkins

#### Prerequisites

1. Jenkins server

#### Install Maven on Jenkins

Download maven packages https://maven.apache.org/download.cgi onto Jenkins server. In this case I am using /opt/maven as my installation directory - Link : https://maven.apache.org/download.cgi

```sh
  # Creating maven directory under /opt
  mkdir /opt/maven
  cd /opt/maven
  # downloading maven version 3.9.8
  wget https://dlcdn.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.tar.gz
  unzip /opt/maven/apache-maven-3.9.8-bin.zip
```

Setup M2_HOME and M2 paths in .bash_profile of user and add these to path variable

```sh
  vi ~/.bash_profile
  M2_HOME=/opt/maven/apache-maven-3.9.8
  M2=$M2_HOME/bin
  PAHT=<Existing_PATH>:$M2_HOME:$M2
```

#### Check point

logoff and login to check maven version
Check maven version

```sh
  mvn –version
```
